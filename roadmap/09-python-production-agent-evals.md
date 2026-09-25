# 09 — python-production-agent-evals

**Priorité : P0** | Durée : 4–6 semaines | Cœur du pitch volume Python en production pour Cohere FDE

## Pourquoi maintenant

Cohere exige du Python en production : code propre, testable, observable, scalable. Les exigences clés de l'offre FDE Agentic Platform : RAG et applications agentiques performantes (patterns ReAct ou Plan-and-Execute), frameworks d'évaluation mesurant précision, sécurité et latence, stack LLM (modèles frontier, bases vectorielles, frameworks d'orchestration). Le point faible à combler : volume de Python en production à démontrer concrètement, pas juste l'affirmer.

## Mission jusqu'en prod

Agent RAG bancaire minimal mais complet : ingestion de documents, retrieval, génération, boucle d'évaluation avec métriques mesurables. Déployé, testé, observable. C'est le projet à montrer en entretien Cohere (round coding et hiring manager).

## Stack

- Python 3.12+
- LangGraph (orchestration agentique, patterns ReAct / Plan-and-Execute)
- LangChain (ingestion, retrieval, génération)
- pgvector (vector store) ou Chroma pour le démarrage
- API Cohere ou OpenAI (modèle frontier)
- FastAPI (API de service)
- pytest (tests unitaires et d'intégration)
- OpenTelemetry (traces, métriques, logs)
- Docker Compose (déploiement local reproductible)
- GitHub Actions (CI : tests + lint)

## Livrables

- [ ] **Semaine 1 — Fondations** : squelette du projet, structure de dossiers, pyproject.toml, environnement virtuel, premier test pytest vert, README avec architecture
- [ ] **Semaine 2 — Pipeline RAG** : ingestion de documents (PDF/Markdown), chunking, embeddings, stockage pgvector, retrieval avec reranking, génération de réponse avec citations de sources
- [ ] **Semaine 3 — Agent LangGraph** : agent ReAct avec tools (recherche documentaire, calcul, appel API), pattern Plan-and-Execute en variante, gestion d'état et mémoire
- [ ] **Semaine 4 — Évaluations** : jeu de questions-réponses de référence (golden dataset), métriques faithfulness / answer relevance / context precision, framework d'évaluation automatisé, seuils de régression
- [ ] **Semaine 5 — Observabilité et API** : FastAPI exposant l'agent, OpenTelemetry (traces par requête, coût, latence), logging structuré, dashboard simple
- [ ] **Semaine 6 — Industrialisation** : Docker Compose, CI GitHub Actions, tests de charge basiques, documentation de démo, limites assumées

## Démo finale (pitch entretien)

1. Montrer le code : structure, tests, CI verte
2. Lancer l'agent sur une question bancaire réelle
3. Montrer les traces OpenTelemetry et le coût par requête
4. Montrer les résultats d'évaluation : précision, latence, taux d'échec
5. Expliquer les arbitrages : pourquoi ce chunking, ce reranker, ce pattern d'agent

## Garde-fous

- Un agent, un contexte — pas tout le SI (aligné roadmap 02)
- Contrat d'interface, jamais le cœur métier en direct
- Validation humaine sur action irréversible
- Observabilité dès le premier appel
- Pas de données bancaires réelles : jeu de données synthétique réaliste

## Lien avec les autres roadmaps

- roadmap 02 (secure-agent-rag-factory) : ce projet est la version Python pure et démontrable ; le 02 reste la version enterprise Java/Spring
- roadmap 06 (agent-otel-observability) : réutiliser les patterns OpenTelemetry
- fde-prep/interview/cohere-fde-loop.md : ce projet alimente le round coding et le hiring manager

## Sources

- Offre Cohere FDE Agentic Platform (UK/Europe) : https://jobs.ashbyhq.com/cohere/2d256112-b336-4539-8133-a0bf7f6698f0
- LangGraph documentation : https://langchain-ai.github.io/langgraph/
- Ragas (framework d'évaluation RAG) : https://docs.ragas.io/
