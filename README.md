# LangGraph — Learning Notebooks

Hands-on notebooks and notes for learning [LangGraph](https://github.com/langchain-ai/langgraph): from core concepts and
basic workflows (sequential, parallel, conditional, iterative) to chatbots, persistence, tools, human-in-the-loop and
subgraphs. Each topic folder has a Jupyter notebook with working code and a PDF with notes.

## Topics

| # | Topic | What it covers | Notebook | Notes |
|---|---|---|---|---|
| 4 | Core concepts | Graphs, state, nodes, edges | — | [PDF](4_Understanding_core_concepts_of_LangGraph/Core%20Concept%20of%20Langraph.pdf) |
| 5 | Sequential workflow | Nodes run one after another (e.g. BMI calculator workflow) | [ipynb](5_Sequential_Workflow_LangGraph/LangGraph_Sequential_Workflows.ipynb) | [PDF](5_Sequential_Workflow_LangGraph/LangGraph_Sequential_Workflows.pdf) |
| 6 | Parallel workflow | Fan-out / fan-in nodes running in parallel (e.g. batsman statistics) | [ipynb](6_Parallel_workflow_LangGraph/Parallel_workflow_LangGraph%20(1).ipynb) | [PDF](6_Parallel_workflow_LangGraph/LangGraph_V6_Parallel_Workflows.pdf) |
| 7 | Conditional edges | Routing between branches (e.g. quadratic equation solver) | [ipynb](7_Conditional_edges/Conditional_workflow_LangGraph.ipynb) | [PDF](7_Conditional_edges/LangGraph_V7_Conditional_Workflows.pdf) |
| 8 | Iterative workflow | Loops until a condition is met (tweet generator + evaluator) | [ipynb](8_Iterative_workflow/Iterative_workflow_LangGraph.ipynb) | [PDF](8_Iterative_workflow/LangGraph_V8_Iterative_Workflows.pdf) |
| 9 | Chatbot | Message state with `add_messages`, memory with `MemorySaver` | [ipynb](9_chatbot_in_langgraph/Chatbot_in_LangGraph.ipynb) | [PDF](9_chatbot_in_langgraph/LangGraph_Chatbot_Notes.pdf) |
| 10 | Persistence | Checkpointers, time travel, updating state, fault tolerance | [ipynb](10_Persistance_in_langgraph/10_persistence.ipynb) | [PDF](10_Persistance_in_langgraph/Persistence_in_LangGraph_Notes.pdf) |
| 17 | Tools | Binding tools to the LLM and running them inside the graph | [ipynb](17_Tools_in_langgraph/Tools__in_LangGraph.ipynb) | [PDF](17_Tools_in_langgraph/Tools_in_LangGraph_Notes.pdf) |
| 20 | Human-in-the-loop | Pausing the graph with `interrupt` and resuming with `Command` | [ipynb](20_HITL_langgraph/HITL__in_LangGraph.ipynb) | [PDF](20_HITL_langgraph/HITL_in_LangGraph_Notes.pdf) |
| 21 | Subgraphs | Graphs as nodes — separate state and shared state | [subgraphs](21_Subgraph_in_Langgraph/15_subgraphs.ipynb) · [shared state](21_Subgraph_in_Langgraph/15_subgraph_shared.ipynb) | [PDF](21_Subgraph_in_Langgraph/Subgraphs_in_LangGraph_Notes.pdf) |

## Running the notebooks

The notebooks were written in Google Colab and use OpenAI models through `langchain_openai`.

```bash
pip install langgraph langchain langchain-openai
```

* **Colab:** add `OPENAI_API_KEY` under *Secrets* (🔑 in the left sidebar); the notebooks read it with
  `userdata.get('OPENAI_API_KEY')`.
* **Locally:** set the environment variable instead and skip the `google.colab` cell:

  ```bash
  export OPENAI_API_KEY="your-key"        # Windows PowerShell: $env:OPENAI_API_KEY="your-key"
  ```

## Tech stack

`langgraph` · `langchain-core` · `langchain-openai` · Python · Jupyter / Google Colab

## License

[MIT](LICENSE)
