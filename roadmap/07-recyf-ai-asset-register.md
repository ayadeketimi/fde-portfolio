# 07 — recyf-ai-asset-register

**Priorité : P2** | Durée : 2–3 semaines

## Pourquoi maintenant

ANSSI a publié le ReCyF (doc de travail, 17/03/2026) : 15 objectifs EI/EE + 5 EE. Les briques IA (agents, LLM, MCP) doivent être intégrées au recensement SI et fournisseurs. Transposition FR (loi Résilience) : statut au 25/09/2026 non confirmé via Légifrance.

## Mission jusqu'en prod

Gap analysis ReCyF → plan 90 jours : qualification EE/EI, matrice écarts, backlog, preuves (IAM, journaux, exercices), IA/agents inclus dans le périmètre.

## Stack

- CMDB légère (Spring Boot + Postgres)
- Mapping objectifs ReCyF
- Export preuves (PDF/JSON)
- Docker Compose

## Livrables

- [ ] CMDB légère avec actifs IA (agents, modèles, MCP, données)
- [ ] Mapping objectifs ReCyF (15 EI/EE + 5 EE)
- [ ] Matrice écarts + backlog
- [ ] Démo : 10 actifs → écarts → backlog
- [ ] Export preuves
- [ ] README : architecture, démarrage, démo, limites

## Garde-fous

- Distinction EI / EE respectée
- Preuves horodatées
- Fournisseurs TIC critiques recensés

## Sources

- [ANSSI — NIS 2 : l'ANSSI poursuit et renforce sa dynamique d'accompagnement](https://cyber.gouv.fr/actualites/nis-2-lanssi-poursuit-et-renforce-sa-dynamique-daccompagnement/)
- [ReCyF PDF v2.5](https://messervices.cyber.gouv.fr/documents-ressources/20260317_NIS_V2_ReCyF_v2.5.pdf)

*Note : transposition FR au JO non confirmée Légifrance au 25/09/2026.*