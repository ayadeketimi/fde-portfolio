# 04 — agentic-finops-meter

**Priorité : P1** | Durée : 2–3 semaines

## Pourquoi maintenant

En prod, le coût bascule sur l'inférence continue. IDC (relayé) : sous-estimation jusqu'à 30 % des coûts infra IA d'ici 2027. Deloitte FR (nov. 2025) : 10 % ont intégré le FinOps métiers/IT. Silicon/IDC FR : 73 % des DSI placent l'optimisation coûts IT dans le top 3 2026.

## Mission jusqu'en prod

Metering + chargeback + hard stop budgets par agent : unit economics (€/requête/dossier), quotas, FinOps-as-code sur pipelines agents/MCP.

## Stack

- Meter OTel (spans enrichis : tokens, modèle, coût)
- Grafana (dashboards coût par agent)
- Mock LLM pricing (tarifs réels des fournisseurs)
- Budget gate CI (hard stop)
- Docker Compose

## Livrables

- [ ] Meter OTel avec enrichissement coût par appel LLM
- [ ] Dashboards Grafana : €/agent, €/requête, tendance
- [ ] Chargeback par équipe / projet
- [ ] Démo : budget atteint → agent en pause (hard stop)
- [ ] FinOps-as-code : seuils versionnés
- [ ] README : architecture, démarrage, démo, limites

## Garde-fous

- Coût visible avant l'appel, pas après
- Alerte avant le hard stop
- Historique des décisions de budget

## Sources

- [IT Social — Coûts cachés de l'infrastructure IA](https://itsocial.fr/metiers/metiers-actualites/couts-caches-de-linfrastructure-ia-le-finops-devient-le-cadre-de-pilotage-du-budget/)
- [Deloitte FR — Technologie, levier de performance économique](https://www.deloitte.com/fr/fr/services/consulting/research/faire-de-la-technologie-un-veritable-levier-de-performance-economique.html)
- [Silicon — Benchmarks FinOps 2026](https://www.silicon.fr/business-1367/les-benchmarks-de-lit-2026-les-solutions-de-finops-doptimisation-des-couts-it-226720)

*Note : le chiffre IDC 30 % est relayé par la presse ; le rapport primaire n'a pas été ouvert.*