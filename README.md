# Bigdata.com — Getting Started

A set of self-contained Jupyter notebooks that get you productive with the
[Bigdata.com](https://bigdata.com) **REST API** — from your first call to
AI-powered research workflows. Every notebook uses plain HTTP (`requests`), so
the patterns translate to any language.

## Notebooks

| # | Notebook | What you'll learn |
|---|----------|-------------------|
| 00 | [`00_hello_world.ipynb`](notebooks/00_hello_world.ipynb) | One call, end-to-end: search the corpus and read results |
| 01 | [`01_setup_and_authentication.ipynb`](notebooks/01_setup_and_authentication.ipynb) | Register, create an API key, authenticate |
| 02 | [`02_knowledge_graph.ipynb`](notebooks/02_knowledge_graph.ipynb) | Find companies by details; resolve by ISIN/CUSIP/SEDOL/listing |
| 03 | [`03_search.ipynb`](notebooks/03_search.ipynb) | Fast vs. smart search; entity/keyword/sentiment/date/type filters |
| 04 | [`04_research.ipynb`](notebooks/04_research.ipynb) | The AI Research Agent (streamed, cited answers) |
| 05 | [`05_workflows.ipynb`](notebooks/05_workflows.ipynb) | Reproducible, templated research at scale |

Work through them in order — each builds on the last.

## Prerequisites

- Python 3.9+
- A Bigdata.com API key (notebook 01 shows how to create one in the
  [Developer Platform](https://platform.bigdata.com))

## Setup

```bash
pip install -r requirements.txt

# Provide your API key via an environment variable (never hard-code it):
export BIGDATA_API_KEY="your_api_key_here"

jupyter notebook   # or: jupyter lab
```

## API at a glance

| Service | Host | Endpoint |
|---|---|---|
| Knowledge Graph | `api.bigdata.com` | `POST /v1/knowledge-graph/companies` |
| Search | `api.bigdata.com` | `POST /v1/search` |
| Research Agent | `agents.bigdata.com` | `POST /v1/research-agent` (SSE) |
| Workflows | `agents.bigdata.com` | `POST /v1/workflow/execute` (SSE) |

Authentication is via the `X-API-KEY` request header on every call.

## Documentation & more

- API docs: https://docs.bigdata.com/api-rest/introduction
- Getting started: https://docs.bigdata.com/getting-started/introduction
- Cookbooks: https://github.com/Bigdata-com/bigdata-cookbook
  (incl. [Batch Search](https://github.com/Bigdata-com/bigdata-cookbook/tree/main/Batch_Search_API))
- Agent Swarm: https://agent-swarm.labs.bigdata.com/

---

© Bigdata.com · Licensed under [MIT](LICENSE)
