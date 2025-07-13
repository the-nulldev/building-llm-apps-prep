# Building LLM Apps: Preparing for Production

## Table of Contents

- [Introduction](#introduction)
- [Learning Outcomes](#learning-outcomes)
- [Project Structure](#project-structure)
- [Tasks](#tasks)
    - Task One — Prompt Management and Versioning
    - Task Two — Chat History Management
    - Task Three — NeMo Guardrails
    - Task Four — Managing API Keys and Budgets via LiteLLM Proxy.
- [Deliverables](#deliverables)
- [Useful Resources](#useful-resources)
- [Contributing](#contributing)

## Introduction

In the `first part` of this series, we established a crucial foundation: a complete evaluation pipeline. We now have the tools and metrics to understand our application's performance, identify hallucinations, and measure the quality of its responses. We know what makes our smartphone info bot “good,” but a successful application needs more than just good performance—it needs to be reliable, safe, and efficient in a live environment.

A prototype application often has hidden issues. Its prompts might be hard-coded, making them difficult to update or A/B test. It might slow down or become costly with repeated similar queries. Without proper safeguards, it could be tricked into going off-topic or responding in an inappropriate manner. As the conversation history grows, it can lose context or exceed token limits, which breaks the user experience. These are the challenges you’ll face when moving from a proof-of-concept to a production-ready system.

In this project, we will tackle these challenges head-on. We will upgrade the core architecture of our chatbot to enhance its robustness and resilience. We'll replace static prompts with a versioned management system, implement intelligent chat history management, ensure cost efficiency, and build a safety net around our LLM with programmable guardrails.

By focusing on these production-oriented patterns, we are building a resilient application that will be ready for scalable deployment in the final part of the series.

---

## **Learning Outcomes**

By the end of this project, you will have transformed the functional chatbot prototype into a production-ready application. You'll implement key operational patterns that ensure reliability and control. This project will equip you with the skills to build LLM applications that are robust, secure, and efficient—ready to handle real-world deployment challenges.

---

## **Project Structure**

Here are the main directories and files in this repo:

```markdown
├── images/
│   ├── litellm_dashboard.png
│   ├── system_ui.png
│   ├── qdrant_free_cluster.png
│   ├── redis_dashboard.png
│   ├── langfuse_dashboard.png
│   └── ecr_push_commands.png
├── tasks/
│   ├── task_1.md
│   ├── task_2.md
│   ├── task_3.md
│   ├── task_4.md
│   └── task_5.md
├── .env.sample
├── .gitignore
├── CONTRIBUTING.md
├── main.py
├── README.md
└── requirements.txt
```

## **Tasks**

The project is divided into various tasks that you need to complete. The tasks are located in the tasks folder of the repository. Each task includes all the necessary objectives, suggested development steps, deliverables, and useful resources. Here's a quick primer on each task:

- **Task One — Prompt management and versioning:** Implement version control for prompts, allowing for easier updates, tracking, and experimentation without changing application code.
- **Task Two — Chat history management:** Design robust strategies for managing chat history, ensuring the chatbot can handle long, context-rich conversations without failure.
- **Task Three — Managing API Keys and Budgets via LiteLLM Proxy:** Use LiteLLM to manage your API keys, set budgets per user per key, enforce rate limits, and more.
- **Task Four — LLM safety and security:** Implement programmable safeguards using NVIDIA's NeMo Guardrails to control the chatbot's conversational boundaries, prevent topical deviations, and ensure it responds safely and appropriately.
- **Task Five — (Extra challenge) Caching using the LiteLLM Proxy:** As an extra challenge, use the LiteLLM proxy to introduce caching and routing to reduce latency and cost.

---

## **Useful Resources**

Each task contains a collection of resources that will be helpful for you as you solve the task. There are links to topics and projects, documentation, and other helpful tutorials that you can use. You may not always need to use all the provided resources if you're already familiar with the concepts. In addition to the provided resources, you can always discuss with others and experts. You can use various channels — GitHub Issues, GitHub Discussions, PRs, or Discord.

---

## **Deliverables**

Each task contains a set of deliverables that bring you close to achieving the final goal. The final product is a production-ready LLM application.

---

## **Contributing**

All discussions and bug reports must be done via GitHub Issues or Discord, while code review is done via GitHub Pull Requests. For more information, see the CONTRIBUTING.md file.

---

### Deliverables

GitHub repo with:

- The final code solution in the `main` branch.
- At least three merged pull requests.

---

## **The Flow**

Fork → Clone → Branch → Implement → PR → Review

- Fork this repo to your own GitHub account.
- Create a new branch for each task (e.g., task-1) if applicable (if there is any code that has to be implemented).
- Implement the solution based on the task descriptions.
- Push the branch to the forked repo.
- Create a Pull Request from the fork back to the main repo.
- We will review the PR and provide feedback through GitHub.

