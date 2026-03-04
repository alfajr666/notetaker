---
title: AI agent design patterns

---

# AI agent design patterns

---
type: Video
source_type: YouTube
source_url: https://youtu.be/GDm_uH6VxPY?si=juYGOR37trnds-BO
Date: 2026-02-27
Date modified: 2025-03-01

themes: AI Agents, Agentic Workflows, Single Agent, Sequential Agents, Parallel Agents, ADK

---
# 🧠 AI Summary
> This video introduces fundamental **AI agent design patterns** using the **Agent Development Kit (ADK)** [00:01:41]. It compares **Single Agent**, **Sequential Agent**, and **Parallel Agent** patterns, highlighting how each handles complexity, control, and latency. While single agents are simple, they become unreliable with complex tasks [00:02:23]. Sequential patterns provide an "assembly line" for predictable, repeatable tasks [00:03:32], while parallel patterns concurrently execute independent subtasks to significantly reduce latency [00:05:27].

---

## 📌 Key Insights
* **Single Agent Pattern**: Best for straightforward tasks where the model determines its own sequence of tool use [00:01:34]. However, it lacks control and becomes unreliable ("nondeterministic") when managing massive system instructions or multistep logic [00:02:23].
* **Sequential Agent Pattern**: Designed for highly structured, repeatable tasks where the output of one sub-agent becomes the input for the next [00:03:25]. This creates a predictable "assembly line" effect, though it is less flexible in dynamic situations [00:04:58].
* **Shared Session State**: In sequential and parallel workflows, agents communicate via a shared "scratch pad" or state, allowing specialized agents to read findings from previous steps using curly brace notation in prompts [00:04:26].
* **Parallel Agent Pattern**: Enables multiple specialized agents (e.g., museum finder, concert finder) to run concurrently [00:05:27]. This is ideal for reducing latency but increases initial costs and requires a final "aggregator" agent to synthesize results [00:06:00, 00:06:54].
* **ADK Integration**: All patterns are demonstrated using the **Agent Development Kit (ADK)** and its web UI, showcasing real-time tracing of tool calls and session state values [00:01:57, 00:04:11].
* **Complexity Trade-offs**: 
    * **Single**: Simple but uncontrollable [00:02:43].
    * **Sequential**: Reliable but rigid [00:04:58].
    * **Parallel**: Fast but complex/costly [00:07:29].

---

## 📝 Analyst Notes
* **Deterministic vs. Nondeterministic**: The video emphasizes that as system instructions grow "massive," the reliability of single agents drops because AI behavior cannot be perfectly guaranteed [00:02:34].
* **Hybrid Workflows**: The "Parallel" pattern is rarely used in isolation; the demo shows it combined with a sequential "aggregator" step to create a usable final output, suggesting that real-world agentic design is usually a mix of these patterns [00:05:52].
* **Tool Progression**: This is the first of a series; future episodes are expected to cover more advanced patterns like "loop and critique" (self-correction) and "agent as a tool" [00:07:57].

---

tags: #AIAgents #AgenticDesign #MachineLearning #ADK #GoogleCloud

[TASK COMPLETE - READY FOR NEXT INPUT]