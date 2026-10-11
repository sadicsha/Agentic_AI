# N8N Multi-Agent Chatbot

An AI-powered web research and reporting chatbot built using **n8n, Google Gemini, and Tavily Search**. The project uses two AI agents working together to research user questions and generate clear, structured answers with relevant source URLs.

##  Project Overview

Finding reliable information online often requires searching multiple websites, reading articles, comparing facts, and summarizing the findings. This project simplifies that process through a multi-agent workflow.

The chatbot accepts a question from the user, searches the web for relevant information, and generates a structured report in simple language.

##  Objectives

- Automate web research using AI agents.
- Retrieve relevant information using Tavily Search.
- Summarize research findings using Google Gemini.
- Generate clear and organized reports.
- Include source URLs to help users explore the original information.
- Demonstrate collaboration between multiple AI agents using n8n.

##  Technologies Used

| Technology | Purpose |
|---|---|
| n8n | Creates and manages the automation workflow |
| Google Gemini | Powers the AI agents and generates responses |
| Tavily Search | Retrieves relevant web search results |
| AI Agents | Perform research and analysis as separate tasks |
| Chat Trigger | Receives questions from users through the chat interface |

##  How It Works

The project follows a simple workflow:

**User Question → AI Agent 1 → AI Agent 2 → Final Answer**

### Agent 1: Researcher

The first AI agent understands the user's question and uses Tavily Search to find relevant information from the web. It collects key findings, supporting evidence, and source URLs where available.

### Agent 2: Analyst and Reporter

The second AI agent receives the original question and the research produced by Agent 1. It reviews the findings and prepares a structured response with an executive summary, key points, examples, sources, and limitations.

### Final Output

The chatbot displays the final response in the n8n chat interface in a readable and organized format.

##  Example Use Case

**User Question:**

"What are the benefits of using artificial intelligence in education? Give me three examples with reliable source URLs and summarize them in simple language."

The chatbot researches the topic and organizes its response around applications such as:

1. Personalized learning for students.
2. Reducing repetitive administrative work for teachers.
3. Improving accessibility through translation, captions, and speech-related tools.

The response aims to explain each application clearly and provide sources for further reading.

##  Key Features

- Natural-language question answering.
- Automated web research.
- Two-agent research and reporting workflow.
- AI-generated summaries in simple language.
- Source URL collection.
- Structured responses with key findings and limitations.
- Visual workflow built using n8n.

##  Workflow Components

The workflow contains:

1. **When Chat Message Received** — accepts the user's question.
2. **AI Agent 1** — performs research.
3. **Google Gemini Chat Model** — generates the research response.
4. **Search in Tavily** — retrieves relevant web results.
5. **AI Agent 2** — analyzes and summarizes the research.
6. **Google Gemini Chat Model** — generates the final report.

The original question and the first agent's output are passed to the second agent so that it can analyze the research instead of asking the user to provide it again.

##  Setup Requirements

To recreate the workflow, you need:

- An n8n instance.
- A Google Gemini API key.
- A Tavily API key.
- Google Gemini and Tavily credentials configured in n8n.

### Setup Steps

1. Open n8n and create a new workflow.
2. Add a **When Chat Message Received** trigger.
3. Add AI Agent 1 and connect it to the chat trigger.
4. Connect a Google Gemini Chat Model to AI Agent 1.
5. Add Tavily Search as a tool for AI Agent 1.
6. Add AI Agent 2 after AI Agent 1.
7. Connect a Google Gemini Chat Model to AI Agent 2.
8. Configure Agent 1's instructions for research and Agent 2's instructions for analysis and reporting.
9. Configure Agent 2 to receive both the original question and Agent 1's research output.
10. Save the workflow and test it with different questions.

**Important:** Keep your API keys private. Configure them through n8n credentials rather than publishing them in your workflow screenshots, README, or source files.

##  Limitations

- Search results may be incomplete or outdated.
- AI-generated responses can contain incorrect information.
- A source URL does not automatically prove that a claim is correct.
- Source links should be opened and checked for relevance.
- Temporary model-service errors may interrupt workflow execution.

##  Future Improvements

- Add automatic source URL validation.
- Improve fact-checking and evidence matching.
- Add retry handling for temporary model failures.
- Export final reports as PDF or Word documents.
- Add additional specialist agents for comparison, fact-checking, or recommendations.
- Improve error handling and workflow monitoring.

##  Learning Outcomes

This project demonstrates practical experience with:

- AI agent workflows.
- Workflow automation using n8n.
- Large language models using Google Gemini.
- Web research using Tavily Search.
- Passing information between AI agents.
- Prompt engineering and structured report generation.
- Identifying limitations in AI-generated research.

##  Author

**Sadicsha Khandait**

MBA – Data Science and Data Analytics

##  Conclusion

The N8N Multi-Agent Chatbot demonstrates how multiple AI agents can work together to automate web research and reporting. By combining Tavily Search with Google Gemini and n8n, the project transforms user questions into organized responses while emphasizing the importance of checking sources and verifying information.

---

*This project is intended for learning and demonstration purposes. AI-generated findings should be verified before being used for important decisions.*
