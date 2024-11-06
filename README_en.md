# XUnity.AutoTranslator-ollama

[中文版](README.md)

## Introduction
This is a game translation service based on Flask and the Ollama API. It allows XUnity.AutoTranslator to call Ollama for translating Japanese game texts into Simplified Chinese. The service supports multiple prompts and dictionary replacements to ensure translation accuracy and fluency.

## Features

- **Multiple Prompts Support**: Supports multiple prompts that dynamically switch based on the quality of translation results.
- **Dictionary Replacement**: Allows using a custom dictionary for vocabulary replacement to improve translation accuracy.
- **Multithreaded Processing**: Utilizes multithreading to handle translation requests concurrently, improving response speed.
- **Error Handling**: Supports API request retries and error handling in case of failure.
- **Special Character Handling**: Automatically handles special characters and punctuation to ensure the integrity of the translation.

## Installation and Setup

### 1. Install Dependencies

Make sure you have Python 3.7 or higher installed. Then, use the following command to install the required dependencies:

```bash
pip install Flask gevent requests
```

### 2. Configure API
Configure the Ollama endpoint and model name in the code.

### 3. Run the Service
After starting the service, you can access the welcome page at http://127.0.0.1:4000/ in your browser, and use http://127.0.0.1:4000/translate?text=your_text to translate text.

### 4. Configure XUnity.AutoTranslator
Modify the following entries in the AutoTranslatorConfig.ini configuration file:

```
[Service]
Endpoint=CustomTranslate
FallbackEndpoint=
--------------
[Custom]
Url=http://127.0.0.1:4000/translate
```

### 5. Run the Game and Test Translation

## Contributing
Contributions are welcome! Please submit issues or pull requests via GitHub.

## Acknowledgements
Thanks to the following open-source projects and tools for their support:
```
Flask
Gevent
Requests
Ollama
```