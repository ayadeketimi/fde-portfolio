# 02 — secure-agent-rag-factory

**Priorité : P0** | Durée : 3–4 semaines | Cœur du pitch Architecte IA / Tech Lead Agentic

## Pourquoi maintenant

Bpifrance : ~200 cas GenAI proposés, ~20 en prod ; agents classés par accès données. Maif : gouvernance + « Maintien en Conditions Intelligentes ». Cigref : ROI classique inadapté, coûts cachés 30–40 % du total.

## Mission jusqu'en prod

Usine agents + RAG sécurisée : registre des agents, MCP autorisés, RAG traçable. 1–2 agents en prod avec logging + quotas. Angle banque : IAM outil-par-outil, observabilité coût/conformité/dérive.

## Stack

- Java 21 / Spring Boot (façade API, IAM, orchestration)
- Python (RAG : ingestion, retrieval, génération)
- pgvector ou OpenSearch (vector store)
- MCP stub (tools autorisés)
- React (UI de démonstration)
- OpenTelemetry (traces, métriques, logs)
- Docker Compose

## Livrables

- [ ] Architecture de référence : classification agents par accès données
- [ ] Pipeline RAG traçable (chunk → source → réponse)
- [ ] Registre des agents (identité, scopes, quotas)
- [ ] Démo : agent RH (données internes) vs agent veille web ; tool interdit → refus ; kill-switch
- [ ] Observabilité : coût par requête, latence, dérive
- [ ] README : architecture, démarrage, démo, limites

## Garde-fous

- Un agent, un contexte — pas tout le SI
- Contrat d'interface, jamais le cœur métier en direct
- Validation humaine sur action irréversible
- Observabilité dès le premier appel

## Sources

- [CIO Online — GenAI : les DSI tentent de garder le contrôle](https://www.cio-online.com/actualites/lire-genai-les-dsi-tentent-de-garder-le-controle-pour-ne-pas-payer-les-pots-casses-16933.html)
- [Cigref — ROI des solutions DIA générative et agentique](https://www.cigref.fr/evaluer-le-retour-sur-investissement-des-solutions-dia-generative-et-agentique)