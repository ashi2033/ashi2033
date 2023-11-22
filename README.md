import requests

telegram_token = 6971045195:AAFC2IWlVywqH2hc-1oDmFhD-Je1cUDJ0RU
chatgpt_token = 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

def get_chatgpt_response(message):
    url = 'https://api.openai.com/v1/chat/completions'
    headers = {
        'Authorization': f'Bearer {chatgpt_token}',
        'Content-Type': 'application/json'
    }
    data = {
        'messages': [{'role': 'user', 'content': message}]
    }
    response = requests.post(url, json=data, headers=headers)
    return response.json()['choices'][0]['message']['content']

<!---
ashi2033/ashi2033 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
