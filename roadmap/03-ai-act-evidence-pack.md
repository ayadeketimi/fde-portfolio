# 03 — ai-act-evidence-pack

**Priorité : P0** | Durée : 2–3 semaines | Calendrier 2026 tangible pour DSI / RSSI / DPO

## Pourquoi maintenant

Enforcement AI Act dès le 02/08/2026 (supervision AI Office + autorités nationales, obligations de transparence actives). Annexe III (haut risque) reportée au 02/12/2027 (Omnibus AI, 27/07/2026). Urgence déployeur : inventaire, rôles, preuves de transparence — pas attendre 2027.

## Mission jusqu'en prod

Registre des systèmes IA + checklist Article 50 + evidence pack reconstructible : version du modèle, prompts, chunks RAG, revue humaine. Export PDF/JSON pour audit.

## Stack

- Spring Boot + Postgres (registre, métadonnées)
- React (UI registre + panneau de preuve)
- Export PDF/JSON (evidence pack)
- Docker Compose

## Livrables

- [ ] Registre des systèmes IA (modèle, version, usage, responsable)
- [ ] Checklist Article 50 automatisée
- [ ] Logging de provenance RAG au niveau du chunk
- [ ] Démo : chat → panneau preuve → export evidence pack
- [ ] Plan de remédiation Annexe III (template)
- [ ] README : architecture, démarrage, démo, limites

## Garde-fous

- Preuves immuables (hash, horodatage)
- Séparation des rôles : déployeur vs auditeur
- Rétention configurable (RGPD)

## Sources

- [Commission UE — AI Act](https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai)
- CIO Online (sujet 1)