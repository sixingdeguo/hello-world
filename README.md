
emo_result=emo_classification_model.emo_classify(gen_kwargs['messages'][-1]['content'], emo_cls_model_config_list[0]['user_prompt'], mode_dict['do_sample_cls'])

class ClassificationModel_Emo(ChatModel):
    def __init__(self, cls_model_config):
        self.cls_model_config = cls_model_config

    def emo_classify(self, chat_input, user_prompt, do_sample_cls, st_args=None):
        cls_prompt = user_prompt.format(chat_input=chat_input)

        if st_args and st_args[0].session_state.show_level > 2:
            st_args[1]['分类详情'] += f'### 情感分类模型Prompt：\n{special_replace(cls_prompt)}\n'

        if self.cls_model_config['deploy_mode'] == 'vllm':
            chat_response = get_openai_response(self.cls_model_config, cls_prompt, 16, do_sample_cls)
            class_response = ''
            for resp in chat_response:
                if resp.dict()['choices'][0]['text'] is None:
                    continue
                class_response += resp.choices[0].text
        elif self.cls_model_config['deploy_mode'] == 'POST':
            post_messages = [{"role": "user", "content": cls_prompt}]
            class_response = get_post_response(post_messages, self.cls_model_config['service_port'], emo_cls = True)
        else:
            cls_input_ids = self.cls_model_config['model'].tokenizer([cls_prompt], return_tensors='pt').input_ids.to(
                self.cls_model_config['model'].model.device)
            cls_generated_ids = self.cls_model_config['model'].model.generate(input_ids=cls_input_ids, max_new_tokens=8,
                                                                              do_sample=do_sample_cls, eos_token_id=[2])
            class_response = \
                self.cls_model_config['model'].tokenizer.batch_decode(cls_generated_ids[:, cls_input_ids.shape[1]:],
                                                                      skip_special_tokens=True)[0]

        if st_args and st_args[0].session_state.show_level > 1:
            st_args[1]['模型结果'] += f'### 情感积极程度分数：\n{class_response}\n'

        emo_score = 0
        try:
            emo_score = float(class_response)
        except:
            emo_score = 0
        return emo_score
