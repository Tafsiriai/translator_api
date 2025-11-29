# 📘 API Overview

#### What the API Does

The translate_text API allows users to translate text from one supported language to another, specifically Kenyan languages such as Kikuyu, Kamba, Luo, Somali, and Swahili.

#### Use Cases

- Building multilingual chatbots or voice assistants.

- Translating educational or health content for local audiences.

- Enabling users to understand content in their native Kenyan or East African languages.

####  Authentication

Install the Python client if not already installed:

```
pip install gradio_client
```

There is no explicit authentication required for basic access to the API hosted on `https://app.tafsiri.ai/`. (If API keys or tokens are later required, we'll document that here).

## 🔧 API Endpoint: `/translate_text`

####  HTTP Method (Python Usage Example)

This API is accessed via a Python client call using the gradio_client.

```
from gradio_client import Client

client = Client("https://app.tafsiri.ai/")
result = client.predict(
    text="Hello!!",
    source_lang="English",
    target_lang="Kikuyu",
    api_name="/translate_text"
)
print(result)

```

### Parameters

| Name         | Type | Required | Description                                                                 |
|--------------|------|----------|-----------------------------------------------------------------------------|
| `text`       | str  | ✅       | The input sentence or phrase to be translated.                             |
| `source_lang`| str  | ✅       | The source language. One of: `'English'`, `'Luo'`, `'Kamba'`, `'Kikuyu'`, `'Somali'`, `'Swahili'`, etc. |
| `target_lang`| str  | ✅       | The target language to translate into. Same options as `source_lang`.      |

### Supported Languages
```
English, Kamba, Kikuyu, Luo, Somali, Swahili,'Amharic', 'Bengali', 'French', 'Ganda', 'German', 'Igbo', 'Kikongo', 'Kinyarwanda', 'Lingala', 'Portuguese', 'Rundi', 'Urdu'

```
### To be Supported Languages
```
Kalenjin (coming soon),
Kimeru (coming soon), 
Kisii/Gusii (coming soon),
Luhya (coming soon),
Maasai (coming soon),
Sheng (coming soon),
Turkana (coming soon)
```
⚠️ Languages marked "coming soon" are not yet available.

## Response

Returns a single str:

- The translated text output.

Example:

```
Nĩ wega mũno!
```

🤝 Contributing

Contributions are welcome! Please open an issue or pull request for improvements or additional features.
