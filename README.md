# Memory framework for LLMs 

This is an OpenAI inspired open-source memory framework for LLMs.



## Features

- Stores user input as memories for future reference
- Retrieves relevant memories based on user queries
- Classifies user input to determine if it should be stored as a memory
- Generates contextual responses using retrieved memories and chat history
- Utilizes an LLM for memory creation and response generation
- Integrates with Supabase and pgvector for efficient memory storage and retrieval

## Installation

1. Clone the repository:

```bash
git clone https://github.com/pr0x7/memory-framework-for-LLMs.git
cd reminisc
```

2. Install the required dependencies:

```bash
pip install -r requirements.txt
```

3. Set up environment variables:
   - Create a `.env` file in the project root directory.
   - Add the following variables to the `.env` file:

```
OPENAI_API_KEY=
SUPABASE_URL=
SUPABASE_KEY=
```
## Usage

To start Reminisc:

1. Run the FastAPI server:

```bash
fastapi dev main.py
```

2. In a separate terminal, run the Streamlit app:

```bash
streamlit run app.py
```

You can now interact with the assistant by entering your messages in the Streamlit app. The assistant will generate responses based on the stored memories and the current conversation context.


## Configuration

You can modify the configuration settings in the `reminisc/config/config.py` file. The available settings include:

- `CLASSIFIER_MODEL_NAME`: The OpenAI model used for classifying user input (default: "gpt-3.5-turbo").
- `MEMORY_CREATOR_MODEL_NAME`: The OpenAI model used for creating memories from user input (default: "gpt-3.5-turbo").

