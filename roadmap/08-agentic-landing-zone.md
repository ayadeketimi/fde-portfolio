# 08 — agentic-landing-zone

**Priorité : P2** | Durée : 3–4 semaines

## Pourquoi maintenant

Modernisation banque 2026 = hybride (API legacy, conteneurs, DevSecOps, cloud souverain). Sans runtime maîtrisé (isolation, secrets, Zero Trust), les agents restent en sandbox (BdF / TransiCIO).

## Mission jusqu'en prod

Façade API + runtime isolé + catalogue MCP approuvé + CI/CD avec gates sécu+coût : 1er parcours métier en prod pilotée.

## Stack

- Spring Boot (façade API sur core mock)
- Agent worker (Python)
- Docker Compose + network policies
- GitHub Actions (gates CD : sécu + coût)
- Catalogue MCP approuvé (versionné)

## Livrables

- [ ] Façade API sur core métier mock
- [ ] Agent worker isolé (réseau, secrets)
- [ ] Catalogue MCP approuvé versionné
- [ ] CI/CD avec gates sécu + coût
- [ ] Démo : agent via façade uniquement ; PR qui casse un gate → bloquée
- [ ] README : architecture, démarrage, démo, limites

## Garde-fous

- Agent ne touche jamais le core directement
- Secrets hors du code (vault ou équivalent)
- Gates CD non contournables

## Sources

- Discours Denis Beau, Banque de France (09/09/2026)
- TransiCIO — DSI : transition banque-assurance