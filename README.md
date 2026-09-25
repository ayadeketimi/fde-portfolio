# FDE Portfolio — Fabrice Yoro

Portfolio de projets **Forward Deployed Engineer** : preuves concrètes, code réel, architecture documentée, démos fonctionnelles. Chaque dépôt démontre une compétence FDE — intégration SI réelle, garde-fous, observabilité, coût, rollback — pas un notebook.

## Objectif

Montrer en entretien DSI qu'on sait aller **jusqu'en production**, pas seulement concevoir l'architecture. Chaque projet est un cas d'usage IA réel dont les DSI parlent en septembre 2026, livrable en 2–4 semaines.

## Roadmap des projets

| # | Dépôt | Sujet | Durée | Priorité |
|---|---|---|---|---|
| 1 | `mcp-zero-trust-gateway` | Gateway MCP Zero Trust (OPA, Keycloak, tools mock) | 3–4 sem. | P0 |
| 2 | `secure-agent-rag-factory` | Usine agents + RAG sécurisée (classification accès données) | 3–4 sem. | P0 |
| 3 | `ai-act-evidence-pack` | Registre IA + evidence pack Article 50 (AI Act) | 2–3 sem. | P0 |
| 4 | `agentic-finops-meter` | FinOps IA agentique — unit economics par agent | 2–3 sem. | P1 |
| 5 | `dora-ready-agent-platform` | Plateforme agentique hybride DORA-ready (bascule LLM) | 3–4 sem. | P1 |
| 6 | `agent-otel-observability` | Observabilité agentique bout-en-bout (OTel, coût, dérive) | 2–3 sem. | P1 |
| 7 | `recyf-ai-asset-register` | Registre actifs IA aligné ReCyF / NIS2 | 2–3 sem. | P2 |
| 8 | `agentic-landing-zone` | Landing zone agentique sur SI existant (façade API, gates CD) | 3–4 sem. | P2 |

## Ordre de construction recommandé

1. **`mcp-zero-trust-gateway`** — différenciant FDE le plus net en entretien
2. **`secure-agent-rag-factory`** — cœur du pitch Architecte IA / Tech Lead Agentic
3. **`ai-act-evidence-pack`** — calendrier 2026 tangible pour DSI / RSSI / DPO

## Sources de la veille

- Flash veille DSI du 25/09/2026 (bot Veille DSI) : sujets chauds, missions jusqu'en prod, specs dépôts
- ENISA Threat Landscape 2026 (22/09/2026)
- Cigref — ROI des solutions DIA générative et agentique (15/01/2026)
- CIO Online — GenAI : les DSI tentent de garder le contrôle (26/03/2026)
- Discours Denis Beau, Banque de France (09/09/2026) — cyber-souveraineté
- Commission UE — AI Act
- ANSSI — ReCyF v2.5 (17/03/2026)

## Règles de travail

- Code réel, pas de démo factice : chaque dépôt doit tourner en local via Docker Compose
- README pro : architecture, démarrage, démo, garde-fous, limites
- Observabilité dès le premier appel : coût, latence, dérive
- Validation humaine sur toute action irréversible
- Plan de sortie : documentation, rollback, KPI

*Mis à jour le 25 septembre 2026.*