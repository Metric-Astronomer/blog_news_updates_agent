# Blog Insight Finder

## Overview

**Blog Insight Finder** is an AI-driven agent that widens the lens on any single blog post.
Provide a PDF of the article and the agent will:

1. **Extract core arguments.** It parses the thesis, supporting claims, evidence, and key take-aways.
2. **Generate smart search queries** from those arguments.
3. **Run web searches** (via the built-in Google Search tool) to locate **ten or more** other posts covering the same or closely related ideas.
4. **Return a concise list**  — *title • author / publication • one-line context • URL* — so you can explore the broader conversation instantly.

## Agent Details

| Feature              | Description                   |
| -------------------- | ----------------------------- |
| **Interaction Type** | Conversational                |
| **Complexity**       | Easy                          |
| **Agent Type**       | Multi-Agent                   |
| **Components**       | Tools: built-in Google Search |
| **Vertical**         | Content / Research            |

### Agent architecture

The underlying architecture (agents, tool calls, and message flow) is unchanged; only the prompt logic now targets blog-insight tasks rather than academic citation mining.

<img src="academic-researcher.png" alt="workflow diagram" width="800"/>

---

## Setup and Installation

All installation, configuration, and deployment steps remain identical to the original instructions. Follow the **Prerequisites**, **Installation**, and **Configuration** sections exactly as before.

---

## Running the Agent

Launch with either interface:

```bash
adk run academic_research
# or
adk web
```

### Example Interaction

```
user  ▶ Hi, what can you do?
agent ▶ Hello! Provide a blog post as a PDF and I'll:
         • pull out its main arguments
         • find at least ten other articles discussing the same ideas
         • send you a summary list with links.
         Please drop in the PDF when you're ready.

user  ▶ blog_post.pdf  (attached)
agent ▶ Got it — extracting core arguments…
         Searching the web for related discussions…

agent ▶ **Core arguments**  
         – Generative-AI tools flatten creativity by standardising style.  
         – True differentiation now depends on hard-earned domain insight, not merely text generation.  
         – Platforms will capture value; individual creators must niche down or collaborate.  

         **Related articles (10)**  
         1. “Is AI Killing Originality?” · *The Verge* · Explores homogenisation in AI-assisted writing · <https://www.theverge.com/...>  
         2. “Why Your GPT Blog Sounds Like Everyone Else’s” · *Medium (Better Programming)* · Practical examples of style convergence · <https://medium.com/...>  
         …8 more entries…
```

---

## Tests, Deployment, and Customisation

All commands (`pytest`, deployment scripts, etc.) continue to work without modification because no function names or variables were changed.

You can still extend the agent (e.g., swap Google Search for another search tool) exactly as described in the original **Customisation** section.
