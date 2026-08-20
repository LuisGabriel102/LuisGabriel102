# Luis Gabriel

**Engenheiro de IA Aplicada** — construo sistemas onde LLMs trabalham em produção, não em demo.

## O que estou construindo

**[Nexus](https://github.com/LuisGabriel102/rpg-api)** — RPG narrado por IA — FastAPI sobre Neon Postgres, empacotado para Railway:

- **Narração multi-modelo:** Claude Opus como narrador principal, com prefixo de prompt cacheável byte-idêntico entre chamadas (latência e custo sob controle)
- **Modelos pequenos como guardrail:** um Haiku valida cada narração (resposta de uma palavra), outro extrai fatos canônicos do turno em JSON estrito
- **Memória de mundo:** embeddings de 768 dimensões sobre os fatos canônicos, com indexação e consulta saindo do mesmo módulo — vetor indexado e vetor consultado nunca divergem
- **Pipeline de imagem** com 3 provedores (Flux, Gemini, GPT)
- **Backend FastAPI:** 11 routers, 86 endpoints; painel administrativo NiceGUI com 29 páginas; 28 tabelas SQLModel

## Stack

Python · FastAPI · PostgreSQL (Neon) · psycopg3 + SQLModel/asyncpg · NiceGUI · Railway · APIs Claude, Gemini e OpenAI
