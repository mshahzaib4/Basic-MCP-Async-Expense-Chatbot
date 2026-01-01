async_expense_chatbot/
├── main.py                  # Entry point, runs the chatbot
├── requirements.txt         # Python dependencies (langchain, langgraph, openai, sqlalchemy, etc.)
├── .env                     # Environment variables (API keys, DB connection string)
├── README.md                # Project description and instructions
├── chat/
│   ├── __init__.py
│   ├── graph_builder.py     # build_graph() and LangGraph node setup
│   ├── nodes.py             # Chat node and tool routing nodes
│   └── state.py             # TypedDict for ChatState
├── tools/
│   ├── __init__.py
│   ├── expense_tool.py      # MCP or DB wrapper to fetch/store expenses
│   └── arithmetic_tool.py   # MCP tool wrapper for calculations (optional)
├── database/
│   ├── __init__.py
│   ├── db_setup.py          # SQLAlchemy setup, engine, session
│   └── models.py            # Expense table model (date, category, amount, description)
├── tests/
│   ├── test_chat.py         # Test chatbot responses
│   ├── test_tools.py        # Test tool calls independently
│   └── test_db.py           # Test database load/store
└── utils/
    ├── __init__.py
    └── helpers.py           # Helpers (date parsing, formatting, validation)