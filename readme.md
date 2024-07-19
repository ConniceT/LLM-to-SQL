# LLM-Powered Chatbot for SQL and NoSQL Databases

This project demonstrates how to build a chatbot powered by a Language Learning Model (LLM) that can interact with both SQL and NoSQL databases. The chatbot converts natural language queries into database queries, retrieves the relevant information, and displays it to the user. The implementation uses OpenAI's LLM, LangChain, and Streamlit for the user interface.

## Features

- **Natural Language Processing**: Converts user input into SQL and NoSQL queries.
- **Multi-Database Support**: Interacts with both MySQL (SQL) and MongoDB (NoSQL) databases.
- **Interactive UI**: Provides a user-friendly interface using Streamlit.
- **Real-time Results**: Retrieves and displays results from the database queries in real-time.

## Requirements

- Python 3.8+
- Streamlit
- LangChain
- OpenAI API key
- MySQL database
- MongoDB database

## Installation

1. **Clone the repository**:
    ```sh
    git clone https://github.com/yourusername/llm-database-chatbot.git
    cd llm-database-chatbot
    ```

2. **Install the dependencies**:
    ```sh
    pip install streamlit langchain openai pymysql pymongo
    ```
    can also achieve this with requirment.txt 

3. **Set up environment variables**:
    Create a `.env` file in the root directory and add your OpenAI API key and database credentials:
    ```sh
    OPENAI_API_KEY=your_openai_api_key
    MYSQL_HOST=your_mysql_host
    MYSQL_USER=your_mysql_user
    MYSQL_PASSWORD=your_mysql_password
    MYSQL_DB=your_mysql_db
    MONGODB_URI=mongodb://your_mongodb_host:your_mongodb_port
    MONGODB_DB=your_mongodb_db
    ```

## Usage

1. **Start the Streamlit application**:
    ```sh
    streamlit run app.py
    ```

2. **Interact with the chatbot**:
    - Select the database type (SQL or NoSQL) from the dropdown menu.
    - Enter your query in natural language in the text area.
    - Click the "Execute" button to see the results.

## Project Structure

```sh
llm-database-chatbot/
├── app.py                 # Main application script
├── requirements.txt       # Python dependencies
└── README.md              # Project documentation



Example Queries
SQL (MySQL)
Natural Language: "Show me the list of all employees in the marketing department."
Generated SQL Query: SELECT * FROM employees WHERE department = 'marketing';
NoSQL (MongoDB)
Natural Language: "Find all products with a price greater than $50."
Generated MongoDB Query:
python
Copy code
{
    "collection": "products",
    "filter": {"price": {"$gt": 50}}
}
Contributing
Contributions are welcome! Please feel free to submit a Pull Request.

License
This project is licensed under the MIT License - see the LICENSE file for details.

Acknowledgements
OpenAI for providing the LLM API.
LangChain for the language model integration.
Streamlit for the interactive UI framework.