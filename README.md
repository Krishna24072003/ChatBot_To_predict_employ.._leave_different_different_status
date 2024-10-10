# Sphinx based ChatBot
Sphinx based  ChatBot is an interactive chatbot designed to assist users in applying for leave requests. It leverages the LangChain and Ollama libraries to utilize machine learning models for generating responses based on user input related to leave applications.
The bot supports conversation history and provides contextual responses based on previous interactions.
## Project Structure
1.main Python file(code)
2.**generated_conversations.txt**: A text file containing conversation data for the chatbot.

**Create a virtual environment:**
python -m venv venv
source venv/bin/activate

**Install the required packages:**
pip install -r requirements.txt
**Set up environment variables:**
LANGCHAIN_API_KEY=your_langchain_api_key
LANGCHAIN_PROJECT=your_langchain_project

**
Requirements**
Create a requirements.txt file with the following content:
langchain
langchain-core
langchain-community
python-dotenv
ipykernel


Main Methods
load_training_data(file_path):

Loads training data from a specified text file.
Input: file_path (string) - The path to the training data file.
Output: A list of documents loaded from the file.

split_text(text):

Splits the input text into manageable chunks for processing.
Input: text (string) - The text to be split.
Output: A list of text chunks.


create_embeddings(text_chunks):

Creates embeddings for the text chunks using an embedding model.
Input: text_chunks (list) - List of text chunks to embed.
Output: A vector store containing the embeddings.

sphinx_chat_bot(vector_store):

Initiates the chatbot interaction with the user.
Input: vector_store (FAISS) - The vector store for similarity search.
Output: User interaction through console input.

**Example Conversation Flow**

User inputs their leave type.
The bot prompts for the number of leave days.
The bot generates a final confirmation message based on the input.

Here’s a concise summary of your Sphinx ChatBot project:

---

### Sphinx based 
 ChatBot Summary

**Overview**:  
Sphinx ChatBot is an interactive chatbot designed to assist users in applying for leave requests. It utilizes the LangChain and Ollama libraries to generate contextual responses based on user inputs related to leave applications.

**Key Features**:
- **User Interaction**: The bot engages users in a dialogue to gather leave application details.
- **Contextual Responses**: It leverages machine learning models to provide relevant answers based on conversation history.
- **Flexibility**: Users can exit the conversation at any time by typing "exit" or "quit."

**Main Components**:
1. **Data Loading**: Loads training data from a text file to inform the chatbot’s responses.
2. **Text Processing**: Splits long texts into manageable chunks for efficient processing.
3. **Embedding Creation**: Converts text chunks into vector embeddings for similarity searching.
4. **Chatbot Logic**: Guides users through the leave application process, prompting for necessary details like leave type and duration.

**Installation and Usage**:
- The project requires Python and several libraries, which can be installed via a `requirements.txt` file.
- Users need to set up environment variables for API keys and configuration.
- The chatbot can be executed from the main script, providing a console interface for user interaction.

**Exiting the Chatbot**: Users can terminate the session by entering "exit" or "quit," and the bot will respond with a farewell message.


