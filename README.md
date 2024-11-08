# XUnity.AutoTranslator-ollama基于as176590811/XUnity.AutoTranslator-chatgpt进行修改
[English Version](README_en.md)

## 简介
这是一个基于 Flask 和 Ollama API 的游戏翻译服务，使XUnity.AutoTranslator可以调用ollama来对于游戏中的日语文本翻译成简体中文。该服务支持多种提示词和字典替换，以确保翻译结果的准确性和流畅性。

## 功能特性

- **多提示词支持**：支持多个提示词，根据翻译结果的质量动态切换提示词。
- **字典替换**：支持使用自定义字典进行词汇替换，以提高翻译的准确性。
- **多线程处理**：使用多线程并发处理翻译请求，提高响应速度。
- **错误处理**：支持 API 请求超时重试和错误处理。
- **特殊字符处理**：自动处理特殊字符和标点符号，确保翻译结果的完整性。

## 安装与运行

### 1. 安装依赖

首先，确保你已经安装了 Python 3.7 或更高版本。然后，使用以下命令安装所需的依赖库：

```bash
pip install Flask gevent requests keyboard
```

### 2. 配置 API

在代码中配置 Ollama相应的地址和模型名称

### 3. 运行服务

服务启动后，你可以在浏览器中访问 http://127.0.0.1:4000/ 查看欢迎页面，并通过 http://127.0.0.1:4000/translate?text=你的文本 进行翻译。

### 4. 配置 XUnity.AutoTranslator

在AutoTranslatorConfig.ini配置文件中修改以下内容：

```
[Service]
Endpoint=CustomTranslate
FallbackEndpoint=
--------------
[Custom]
Url=http://127.0.0.1:4000/translate
```
### 5.运行游戏，测试是否正常翻译

## 贡献

欢迎贡献代码和提出改进建议！请通过 GitHub 提交 Issue 或 Pull Request。

## 鸣谢

感谢as176590811/XUnity.AutoTranslator-chatgpt源代码支持

感谢以下开源项目和工具的支持：
```
Flask
Gevent
Requests
Ollama
keyboard
```
