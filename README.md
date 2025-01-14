# AI Agents with Langraph: Exploring Agentic AI

![image](https://github.com/user-attachments/assets/2df725a4-ec76-41d4-8ace-68f189cd79ab)


This project delves into building and exploring **Agentic AI** using Langraph, OpenAI, and Tavily (a fast internet search API provider). Through various tools and methodologies, the project aims to push the boundaries of AI autonomy, persistence, and usability in real-world scenarios.

---

## Features Explored

1. **ReAct Agent**  
   A combination of reasoning and acting, enabling agents to solve complex tasks by integrating decision-making with action.

2. **Agentic Search Tools**  
   Leveraging Tavily for fast, accurate internet searches, enabling agents to retrieve real-time information.

3. **Persistence and Streaming**  
   Persistent memory for agents, coupled with streaming capabilities, allows agents to maintain context over time and respond dynamically.

4. **Human in the Loop**  
   Facilitating human interventions to guide, correct, or collaborate with agents when needed.

5. **Essay Writer**
   A specialized agent designed to draft essays, leveraging Langraph’s robust text generation capabilities.

   ![image](https://github.com/user-attachments/assets/0b2a02cf-979c-4d89-9522-796bbbb04330)

---

## Prerequisites

To replicate or build upon this project, ensure the following are set up:

- **API Keys**: Access to OpenAI and Tavily APIs.
- **Python Environment**: Version 3.8 or higher.
- **Dependencies**: Install required libraries:
  ```bash
  pip install langraph openai tavily
  ```

---

## Architecture Overview

The project revolves around **Langraph**, a powerful tool for building, orchestrating, and visualizing AI agents. Key components include:

- **OpenAI GPT Models**: For generating, reasoning, and decision-making.
- **Tavily API**: For fast and efficient internet search capabilities.
- **Langraph Framework**: To manage the flow, memory, and tools for AI agents.
- **Persistence**: Using storage solutions to save agent states and conversations.

---

## Getting Started

### Step 1: Clone the Repository
```bash
git clone https://github.com/your-repo-name/ai-agents-langraph.git
cd ai-agents-langraph
```

### Step 2: Set Up Environment Variables
Create a `.env` file with your API keys:
```
OPENAI_API_KEY=your_openai_api_key
TAVILY_API_KEY=your_tavily_api_key
```

### Step 3: Install Dependencies
```bash
pip install -r requirements.txt
```

---

## How It Works

### 1. **ReAct Agent**  
Agents use Langraph to combine reasoning (Re) and acting (Act) in an iterative process to solve complex tasks.  
Example:
```python
from langraph import ReActAgent
agent = ReActAgent(model="gpt-4")
response = agent.run("Plan a 3-day trip to Tokyo.")
```

### 2. **Agentic Search Tools**  
Agents use Tavily for fast, real-time internet searches to augment their knowledge.  
Example:
```python
from tavily import SearchAPI
search = SearchAPI(api_key="your_tavily_api_key")
results = search.query("Latest trends in AI")
```

### 3. **Persistence and Streaming**  
Store and stream agent conversations for enhanced interactivity and memory.  
Example:
```python
from langraph.memory import PersistentMemory
memory = PersistentMemory("conversation.db")
memory.store("User asked about climate change policies.")
```

### 4. **Human in the Loop**  
Integrate human interventions at critical decision points to refine agent actions.  
Example:
```python
decision = agent.human_intervention(prompt="Should the agent proceed with these steps?")
```

### 5. **Essay Writer**  
A specialized agent that drafts essays based on prompts and guidelines.  
Example:
```python
response = agent.run("Write a 1000-word essay on the impact of AI in education.")
```

---

## Use Cases

- **Autonomous Research Agents**: For businesses, researchers, and students.
- **Real-Time Decision Support**: Providing actionable insights with minimal latency.
- **Collaborative Tools**: Assisting humans in creative and analytical tasks.

---

## Future Enhancements

- Incorporating more advanced search APIs for richer data retrieval.
- Enhancing the persistence layer for multi-agent systems.
- Integrating voice input/output for a more natural interaction experience.

