# Bob the Builder

**Bob the Builder** is a **conversational AI agent** designed to transform natural language prompts into working projects. Built with [LangGraph](https://www.langchain.com/langgraph). for robust workflow management and leveraging **GroqCloud** for high-speed code generation, it can create a wide range of simple web apps and APIs, from to-do lists to FastAPI services.


## LangGraph Workflow - Agent Architecture

- **Planner Agent** → Understands your request and creates a detailed plan.  
- **Architect Agent** → Breaks the plan into concrete engineering tasks, with explicit context for each file.  
- **Coder Agent(s)** → Implement tasks, write directly into files, and use developer-like workflows.  



##  Setup & Installation

### Prerequisites
- [uv](https://github.com/astral-sh/uv) installed  
- A [Groq API key](https://console.groq.com/)  

### Steps
1. **Create a virtual environment**
   ```bash
   uv venv
   source .venv/bin/activate
   
2. **Install dependencies**

   ```bash
   uv pip install -r pyproject.toml

3. **Set environment variables**

   * Copy `.sample_env` → `.env`
   * Add your Groq API key and other values

4. **Run the application**

   ```bash
   python main.py
   ````

##  Example Prompts

You can ask the agent system to build:

* “Create a to-do list application using HTML, CSS, and JavaScript.”
* “Build a calculator web app.”
* “Generate a blog API in FastAPI with a SQLite database.”


##  Tech Stack

* **Python** 
* **LangGraph** (agent orchestration)


##  Agent Flow

```
flowchart TD
    User([User Request]) --> Planner[Planner Agent]
    Planner --> Architect[Architect Agent]
    Architect --> Coder[Coder Agent(s)]
    Coder --> Files[Generated Project Files]
```

---

##  Contributing

Contributions are welcome!

* Open issues for bugs or feature requests
* Submit pull requests with improvements

```





