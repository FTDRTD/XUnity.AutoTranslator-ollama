# XUnity.AutoTranslator-ollama
# Game Translation Service

This is a game translation service based on Flask and the Ollama API, designed for XUnity.AutoTranslator to translate Japanese text in games into Simplified Chinese using Ollama. The service supports multiple prompts and dictionary replacements to ensure accurate and fluent translation results.

## Features

- **Multiple Prompt Support**: Supports multiple prompts and dynamically switches prompts based on translation quality.
- **Dictionary Replacement**: Supports custom dictionaries for vocabulary replacement to improve translation accuracy.
- **Multithreaded Processing**: Uses multithreading to handle translation requests concurrently and improve response speed.
- **Error Handling**: Supports API request timeout retries and error handling.
- **Special Character Handling**: Automatically processes special characters and punctuation to ensure the integrity of the translation result.

## Installation and Setup

### 1. Install Dependencies

Make sure you have Python 3.7 or higher installed. Then, install the required dependencies using the following command:

```bash
pip install Flask gevent requests
```

### 2. Configure API

Configure the Ollama API endpoint and model name in the code.

### 3. Run the Service

Once the service is running, you can visit http://127.0.0.1:4000/ in your browser to view the welcome page. You can also access the translation endpoint at http://127.0.0.1:4000/translate?text=your_text to perform translations.

## Contributing
Welcome contributions! Please submit issues or pull requests via GitHub.

## Acknowledgments
Thanks to the following open-source projects and tools:
```
Flask
Gevent
Requests
Ollama
```