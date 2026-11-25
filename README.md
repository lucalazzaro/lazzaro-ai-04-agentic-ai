# GreenThumb — Agentic Customer-Support Assistant

> Progetto sviluppato nell'ambito del Master in AI Solution Architecture
> (ProfessionAI) — modulo Agentic AI. Caso di studio a fini didattici.

## Descrizione
An AI assistant for the fictional e-commerce company GreenThumb. It answers
customer questions about returns, defective products and consumer rights by
combining an LLM agent with a knowledge base of company policies. The agent is
exposed through a local FastAPI endpoint and its answers are evaluated with
automated metrics.

## Stack
- Python 3
- LangChain, LangGraph (prebuilt agent with tool calling)
- OpenAI models via `langchain-openai`
- FastAPI + Uvicorn (local chat endpoint)
- ChromaDB (knowledge base retrieval)
- DeepEval and RAGAS (evaluation)
- Google Colab notebook

## Skill dimostrate
- Agent design with tool calling (LangGraph)
- Retrieval over a policy knowledge base
- Exposing an agent through a REST API
- Automated evaluation of LLM answers (DeepEval, RAGAS)
- Handling of customer-data privacy and consumer-law constraints in prompts

## Come eseguire
The notebook is designed for Google Colab. It reads the API key from Colab
secrets (`OPENAI_API_KEY`).

1. Open `Assistente_AI.ipynb` in Google Colab.
2. Add `OPENAI_API_KEY` to the Colab secrets panel.
3. Run the cells in order. The chat endpoint starts on `http://127.0.0.1:8000/chat`.

To run it outside Colab, replace `userdata.get(...)` with an environment
variable read:

```bash
export OPENAI_API_KEY="your-key-here"
```

## Note
- Caso di studio a fini didattici. I dati, le aziende e i contatti citati nel
  codice sono interamente fittizi. Email addresses use the `example.com` domain.
- `OPENAI_API_KEY` is required and must never be committed to the repository.
