# 36-rfp-Agent

Répondeur automatisé d'appels d'offres (RFP). Se connecte à une Google Sheet via un compte de service, lit le questionnaire RFP dans un DataFrame, et utilise un agent IA avec une base de connaissances markdown (documents d'entreprise indexés dans Qdrant) pour remplir la colonne "Réponse" (Oui/Non/Partiel avec justification), puis réécrit la feuille complétée sur Google Sheets.

## Tech stack

agno (Agent, OpenAIChat, ReasoningTools, MarkdownKnowledgeBase, Qdrant), pygsheets, pandas, python-dotenv

## Lancer le projet

```bash
pip install agno pygsheets pandas python-dotenv
```

Créer un `.env` avec `OPENAI_API_KEY`, `QDRANT_API_KEY`, `QDRANT_URL`, et un fichier `client_secret.json` (compte de service Google)

```bash
python main.py
```
