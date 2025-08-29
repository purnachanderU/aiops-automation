Dockerfile Generator
A GenAI-powered tool that generates optimized Dockerfiles based on programming language input. This tool leverages Ollama with the Llama3 model to create Dockerfiles following industry best practices.

📋 Prerequisites
Installing Ollama
Linux:

bash
curl -fsSL https://ollama.com/install.sh | sh
macOS:

bash
brew install ollama
Windows:
Download and install from ollama.com

Setup Ollama
Start the Ollama service:

bash
ollama serve
Pull the required model:

bash
ollama pull llama3
🚀 Project Setup
Create Virtual Environment

bash
python3 -m venv venv
source venv/bin/activate  # Linux/macOS
# or
.\venv\Scripts\activate  # Windows
Install Dependencies

bash
pip install -r requirements.txt
Run the Application

bash
python generate_dockerfile.py
💡 How It Works
Provide a programming language as input (e.g., python, node, java, nginx)

The tool connects to your local Ollama API

Generates an optimized Dockerfile following best practices for the specified language

Returns clean Dockerfile content ready for use

📝 Example Usage
bash
python generate_dockerfile.py
Enter the programming language: python

# Generated output:
# FROM python:3.9-slim
# WORKDIR /app
# COPY requirements.txt .
# RUN pip install -r requirements.txt
# COPY . .
# CMD ["python", "app.py"]
🏆 Troubleshooting
Ensure Ollama service is running before executing the script

Verify the model is downloaded using ollama list

Check your connection to the local Ollama API (default: http://localhost:11434)

For other programming languages, the tool will adapt best practices accordingly

Supported Languages
The tool supports various programming languages including:

Python

Node.js

Java

Go

Ruby

Nginx

And more....etc

Simply enter the language name when prompted, and the tool will generate an appropriate Dockerfile.
