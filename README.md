# AI Travel Agent

A small LLM agent that plans trips and returns **validated, structured output**. It can search the web when it needs fresh info.

## What it does
- Built with LangChain's `create_agent` on top of a Groq-hosted LLM.
- Uses a **DuckDuckGo search tool** to look things up when helpful.
- Forces the final answer into a Pydantic schema (`TravelOutput`): `destination`, `budget` (nullable, never guessed), `duration`, and a short `summary`.
- Includes a retry wrapper and a fallback printer for when the model returns raw text or a tool call fails.

## Stack
`LangChain` · `Groq` · `Pydantic` · `DuckDuckGo Search`

## Run it
Open `Travel_Agent.ipynb` in Google Colab and add the secret `GROQ_API_KEY` (Colab → Secrets).
