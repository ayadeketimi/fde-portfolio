# 05 — dora-ready-agent-platform

**Priorité : P1** | Durée : 3–4 semaines

## Pourquoi maintenant

DORA applicable depuis le 17/01/2025. Denis Beau (BdF/ACPR), 09/09/2026 : concentration hyperscalers/IA = risque (expertise, lock-in, scénario type kill switch) ; leviers multi-cloud, réversibilité, open source, CTPP.

## Mission jusqu'en prod

RAG « data stays » + bascule fournisseur LLM testée : classification workloads, clauses portabilité, tests de bascule, cartographie tiers TIC critiques.

## Stack

- Abstraction `LlmProvider` (interface commune)
- Ollama local (fournisseur A) + API cloud mock (fournisseur B)
- pgvector (données locales, RAG « data stays »)
- Chaos « kill provider » (test de bascule)
- Docker Compose

## Livrables

- [ ] Interface `LlmProvider` avec 2 implémentations (local + cloud)
- [ ] RAG sur données locales (pgvector)
- [ ] Démo : panne fournisseur A → bascule B, données locales
- [ ] Test de bascule automatisé (CI)
- [ ] Cartographie des tiers TIC critiques
- [ ] README : architecture, démarrage, démo, limites

## Garde-fous

- Données jamais envoyées au fournisseur cloud
- Bascule testée avant incident, pas pendant
- Mesure de latence/coût par fournisseur

## Sources

- [Discours Denis Beau, Banque de France (09/09/2026)](https://www.banque-france.fr/fr/system/files?file=2026-09/2026_09_09_ADB_Conference_CyberSouverainete-discours_D_Beau_0.pdf)
- [TransiCIO — DSI : transition banque-assurance](https://www.transicio.com/publications/dsi-transition-banque-assurance/)