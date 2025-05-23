

# Visual-Agentic-AI

**Multi-agent Supervisor using LangGraph**

## 1. Scenario

With the rapid development of large language models (LLMs), deploying systems capable of reasoning, decision-making, and coordinated action is becoming a trend in building intelligent AI applications. However, relying solely on a single agent often leads to several limitations, such as:

* **Tool overload**: the model must select the correct tool from dozens of options.
* **Context overload**: it's difficult to manage intermediate steps in complex tasks.
* **Lack of specialization**: a single agent cannot effectively handle planning, searching, data processing, programming, etc., all at once.

To address these challenges, the **multi-agent architecture** is proposed as a viable solution: breaking the system into independent agents, each responsible for a specific task. These agents can communicate with each other or be coordinated by a **supervisory entity (supervisor)**.

## 2. How to do it

In this section, we will use the **LangGraph** library to build an agent system based on the **Supervisor architecture**.

**LangGraph** is a framework built on top of **LangChain**, allowing the modeling of LLM task processes as **stateful graphs** with loops. One of the powerful structures supported by LangGraph is the **multi-agent supervisor architecture**—where one agent plays the role of the **supervisor**, coordinating specialized sub-agents to accomplish a task.

This architecture reflects the decentralization model seen in real-world organizations: the **supervisor** acts like a manager, while the **sub-agents** are domain experts (e.g., for information retrieval, data analysis, planning).

### In this setup:

* **Supervisor**: The central agent responsible for coordinating task execution and interacting with other agents.

* **Two primary action agents**:

  * **Research Agent**
  * **Vision Agent**
    These agents interact directly with the Supervisor Agent.

* All agents are designed based on the **ReAct Agent** architecture.

### ReAct Agent operates based on a combination of:

* **Reasoning**: The model thinks through the problem, analyzes the situation, and plans the next actions.
* **Acting**: The model performs actions based on its reasoning, gathers new information, and continues the process.


