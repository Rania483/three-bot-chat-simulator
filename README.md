# three-bot-chat-simulator

## Overview

`3botChats.ipynb` is a Jupyter Notebook that demonstrates a multi-agent conversational system simulating a humorous, adversarial classroom scenario. It features interaction between three AI-powered personas:
- **Teacher** (via OpenAI's GPT)
- **Alex** (a student via Google's Gemini)
- **Charlie** (a student via Anthropic's Claude)

## Scenario

The notebook sets up a fictional classroom where:
- The **teacher** is angry and frustrated.
- **Alex** and **Charlie** are portrayed as students who don't understand anything.

The agents carry an ongoing conversation, each responding in character per their defined system role. The dialogue proceeds in turns, mimicking a three-way chat.

## Key Features

- **API Integration:** Uses OpenAI, Anthropic, and Google Gemini model APIs.
- **Custom Persona Definition:** Each bot is given a distinct personality and role via the `system` prompt.
- **Conversation Management:** The entire chat history is tracked and passed to each model for context.
- **Iterative Dialogue:** The notebook iteratively generates dialogue for each participant over multiple turns.

## Usage

1. **Prerequisites:**
    - Python environment with Jupyter Notebook
    - API keys for OpenAI, Anthropic, and Google Gemini
    - `.env` file with the following keys:
                OPENAI_API_KEY=your-openai-key
        ANTHROPIC_API_KEY=your-anthropic-key
        GOOGLE_API_KEY=your-google-key
        ```

2. **Run the Notebook:**
    - Open `3botChats.ipynb` in Jupyter.
    - Execute cells sequentially.
    - The conversation will be displayed in Markdown format.
    
3. **Workflow:**
    - The notebook loads API keys and sets up the bot models.
    - Initializes the conversation with a greeting from each participant.
    - Uses functions (`call_gpt`, `call_gemini`, `call_claude`) to generate responses.
    - The `chat_models` function manages the chat loop and displays each response.

## Main Functions

- `call_gpt(conversation)`: Gets teacher's next response.
- `call_gemini(conversation)`: Gets Alex's next response.
- `call_claude(conversation)`: Gets Charlie's next response.
- `chat_models(conversation)`: Runs and displays the multi-turn dialogue between all bots.

## Customization

- **Change the personalities** by modifying the `system` strings.
- **Adjust number of turns** in the `chat_models` loop.
- **Expand participants** by adding more functions and roles.

## Example Output

The output is a humorous, role-played chat conversation rendered in Markdown, e.g.:


teacher : Hi everybody
Alex: Hello dad!
Charlie: hello mom!
...

## Notes

- Models and API endpoints must match your credentials and may require updates for newer versions.
- This notebook is intended for educational, testing, and demonstration purposes.


For any questions or feedback, please contact the notebook author.
