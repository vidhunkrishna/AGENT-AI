# AGENT-AI
# Agent AI Skill Sprint Challenges

This repository contains my solutions for the **Agent AI Skill Sprint**. Throughout these challenges, I explored building AI agents using the Strands framework, starting with a local Ollama model and then moving to Amazon Bedrock. Each challenge introduces a new concept such as tool calling, memory, and MCP integration.

---

## Challenge 1 – First AI Agent

The first challenge was to build a basic AI assistant using **Strands** with a locally running **Ollama** model.

I connected the agent to my local Ollama server (`localhost:11434`) and used the **Llama 3.2** model to generate responses.

**Concepts Covered**

* Creating a Strands Agent
* Connecting to Ollama
* Running a local LLM
* Using system prompts

---

## Challenge 2 – Tool Calling

In this challenge, I built an agent that can call Python functions as tools instead of answering everything directly.

I implemented three tools:

* Calculator (using `strands_tools`)
* Weather Tool (returns a mock weather response)
* Age Calculator (calculates age from a given birth date)

The agent automatically chooses which tool to use based on the user's prompt.

**Concepts Covered**

* Custom tool creation using `@tool`
* Tool selection
* Amazon Bedrock integration
* Function calling

---

## Challenge 3 – Memory Agent

For this challenge, I added a simple memory system using a local JSON file.

The program stores information such as the user's name and favourite food in `memory.json`. Whenever the user asks what the assistant knows about them, it reads the stored values and displays them.

This helped me understand how persistent memory works without using a database.

**Concepts Covered**

* Reading and writing JSON files
* File handling in Python
* Persistent memory
* Interactive command-line applications

---

## Challenge 4 – Full AI Assistant

This challenge combines the previous concepts into one assistant.

The agent can:

* Perform calculations
* Provide weather information
* Calculate age
* Respond to general questions using Amazon Bedrock

Unlike the previous challenges, this version runs continuously until the user exits the application.

**Concepts Covered**

* Multiple tool integration
* Interactive chat loop
* Agent-based workflows

---

## Challenge 5 – AWS Learning Assistant

In the final challenge, I integrated the **AWS Documentation MCP Server** with the Strands Agent.

Instead of manually writing AWS knowledge into the application, the agent retrieves information directly through MCP and answers AWS-related questions.

This was my first experience working with the **Model Context Protocol (MCP)**.

**Concepts Covered**

* MCP Client
* AWS Documentation MCP Server
* Amazon Bedrock
* Tool discovery using `list_tools_sync()`

---

## Technologies Used

* Python 3.11
* Strands Agents Framework
* Ollama
* Llama 3.2
* Amazon Bedrock (Nova Pro)
* AWS CLI
* AWS Documentation MCP Server
* Model Context Protocol (MCP)

---

## Project Structure

```text
AgentAI-SkillSprint/
│
├── challenge-1-first-agent/
├── challenge-2-tools/
├── challenge-3-memory/
│   └── memory.json
├── challenge-4-full-agent/
├── challenge-5-mcp/
├── requirements.txt
└── README.md
```

---

## Setup

Clone the repository:

```bash
git clone https://github.com/your-username/AgentAI-SkillSprint.git
cd AgentAI-SkillSprint
```

Create a virtual environment:

```bash
python -m venv venv
```

Activate it:

**Windows**

```bash
venv\Scripts\activate
```

**Linux/macOS**

```bash
source venv/bin/activate
```

Install the required packages:

```bash
pip install -r requirements.txt
```

---

## Ollama Setup (Challenge 1)

Install Ollama and pull the model:

```bash
ollama pull llama3.2
```

Start the Ollama server:

```bash
ollama serve
```

---

## AWS Setup (Challenges 2–5)

Configure AWS CLI:

```bash
aws configure
```

Verify the configuration:

```bash
aws sts get-caller-identity
```

Make sure your AWS account has access to **Amazon Bedrock** and the **Nova Pro** model.

---

## Running the Challenges

Challenge 1

```bash
cd challenge-1-first-agent
python starter.py
```

Challenge 2

```bash
cd challenge-2-tools
python starter.py
```

Challenge 3

```bash
cd challenge-3-memory
python starter.py
```

Challenge 4

```bash
cd challenge-4-full-agent
python starter.py
```

Challenge 5

```bash
cd challenge-5-mcp
python starter.py
```

---

## What I Learned

Working through these challenges helped me understand how modern AI agents are built. I learned how to connect local models with Ollama, use Amazon Bedrock for cloud-based inference, create custom tools, implement simple persistent memory, and integrate external knowledge using the Model Context Protocol (MCP). It also gave me practical experience with Python, AWS CLI, and agent-based application development.

---

## License

This repository was created as part of the Agent AI Skill Sprint for learning and practice.
