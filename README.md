import requests

url = "http://localhost:5000/get_reward"
data = {
    "query": ["This is a test sentence.", "Here is another example."]
}

response = requests.post(url, json=data)

print(response.json())
