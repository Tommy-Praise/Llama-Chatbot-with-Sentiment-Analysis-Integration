# Llama-Chatbot-with-Sentiment-Analysis-Integration
This project implements an AI assistant chatbot using the Llama 2 model from Hugging Face, enhanced with sentiment analysis to modify its responses based on the user's emotional tone. The chatbot dynamically responds to user queries by checking a predefined QA dataset or generating answers using the Llama 2 model, while adjusting its responses based on sentiment.

**Features**

**Sentiment Analysis**: The chatbot analyzes user sentiment (positive, negative, neutral) and adjusts its responses accordingly.

**Llama 2 for Text Generation:** Uses the Llama 2 model from Hugging Face to generate intelligent and context-aware responses.

**Dynamic Learning:** If a question is not found in the predefined QA dataset, the chatbot generates an answer and stores it in the dataset for future use.

**Gradio Interface:** A simple and intuitive web interface for interacting with the chatbot.


**Tech Stack**

**Hugging Face Transformers:** For Llama 2 model and sentiment analysis pipeline.

**Pandas:** For managing the QA dataset.

**Gradio:** For building the user interface.

**Google Colab:** Recommended platform for running this project.


**Installation**
To get started, install the required libraries:


pip install -q accelerate protobuf sentencepiece torch git+https://github.com/huggingface/transformers huggingface_hub
pip install -q gradio


**Running the Chatbot**

Authenticate with Hugging Face:

You will need a Hugging Face access token to load the Llama 2 model. You can add your token to the login() function in the code.


**Run the Chatbot:**
The chatbot will load a QA dataset (or create one if it doesn't exist) and launch the Gradio interface where you can interact with it.


**Sentiment-Driven Responses:**
As you ask questions, the chatbot will detect your sentiment (positive, negative, neutral) and adjust its responses to match the tone.


Example Usage
Positive Sentiment:

User: "What is the name of Julius Magellan's dog?"
Chatbot: "The name of Julius Magellan's dog is Sparky"
Negative Sentiment:

**User:** "Why do I always forget names?"

**Chatbot:** "I'm sorry you're feeling that way. Julius Magellan's dog is called Sparky"


**How It Works**

Sentiment Analysis:

The user's input is passed through a sentiment analysis pipeline to classify it as positive, negative, or neutral.


**Answer Generation:**

If the question exists in the QA dataset, the chatbot retrieves and responds with the stored answer.
If not, the Llama 2 model generates an answer, which is stored in the QA dataset for future use.

**Response Adjustment:**
The response is modified based on the detected sentiment. For example, positive sentiments may lead to cheerful responses, while negative sentiments will trigger empathetic responses.


**Future Enhancements**

**Fine-tuning:** Improving the Llama 2 model to suit assistant-like conversations better.

**Extended Context Memory:** Allowing the chatbot to retain longer conversation histories for improved contextual understanding.

**Custom Prompt Engineering: ** Improving prompt quality for better task-specific responses.

**Advanced Gradio UI:** A more dynamic and user-friendly interface with conversation-style options and real-time sentiment visualizations.


**License**

This project is open-source and licensed under the MIT License.

