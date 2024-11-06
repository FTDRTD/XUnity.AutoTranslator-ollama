# XUnity.AutoTranslator-Ollama Based on as176590811/XUnity.AutoTranslator-ChatGPT

[中文版](README_zh.md)

## Introduction
This is a game translation service based on Flask and the Ollama API, allowing XUnity.AutoTranslator to call Ollama for translating Japanese text in games into Simplified Chinese. The service supports multiple prompt words and dictionary replacements to ensure translation accuracy and fluency.

## Features

- **Multiple Prompt Support**: Supports multiple prompts, dynamically switching prompts based on the translation result quality.
- **Dictionary Replacement**: Allows the use of a custom dictionary for word replacements to improve translation accuracy.
- **Multithreading**: Uses multithreading for concurrent translation requests, improving response speed.
- **Error Handling**: Supports API request timeout retries and error handling.
- **Special Character Handling**: Automatically handles special characters and punctuation marks, ensuring the completeness of the translation result.

## Installation and Running

### 1. Install Dependencies

Make sure you have Python 3.7 or higher installed. Then, use the following command to install the required dependencies:

```bash
pip install Flask gevent requests keyboard
```

### 2. Configure API
Configure the Ollama API URL and model name in the code.

### 3. Run the Service
After starting the service, you can visit http://127.0.0.1:4000/ in your browser to view the welcome page, and use http://127.0.0.1:4000/translate?text=your_text to perform translations.

### 4. Configure XUnity.AutoTranslator
Modify the following settings in the AutoTranslatorConfig.ini configuration file:
```
[Service]
Endpoint=CustomTranslate
FallbackEndpoint=
--------------
[Custom]
Url=http://127.0.0.1:4000/translate
```

### 5. Run the Game and Test Translation
Test the game to ensure translations are working correctly.

## Contributing
Feel free to contribute code or suggest improvements! Please submit issues or pull requests through GitHub.

## Acknowledgements
Special thanks to the following open-source projects and tools:
```
Flask
Gevent
Requests
Ollama
keyboard
```
Also, thanks to as176590811/XUnity.AutoTranslator-chatgpt for the source code support.