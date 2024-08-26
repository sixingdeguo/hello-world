    def _save_checkpoint(self, args, tag, client_states):
        # call remote critic
        if self.critic_train_remote:
            ref = self.critic.save_checkpoint.remote(tag)
        self.strategy.save_ckpt(
            self.actor.model,
            os.path.join(args.ckpt_path, "_actor"),
            tag,
            args.max_ckpt_num,
            args.max_ckpt_mem,
            client_states,
        )
        # wait
        if self.critic_train_remote:
            ray.get(ref)


    
    # load checkpoint
    self.consumed_samples = 0
    ckpt_path = os.path.join(args.ckpt_path, "_actor")
    if args.load_checkpoint and os.path.exists(ckpt_path):
        _, states = strategy.load_ckpt(self.actor.model, ckpt_path)
        self.consumed_samples = states["consumed_samples"]
        strategy.print(f"Loaded the checkpoint: {ckpt_path}, consumed_samples: {self.consumed_samples}")


    # broadcast checkpoint
    ckpt_path = os.path.join(args.ckpt_path, "_actor")
    if args.load_checkpoint and os.path.exists(ckpt_path) and not vllm_engines is None:
        torch.distributed.barrier()
        trainer._broadcast_to_vllm()
