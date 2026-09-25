# 01 — mcp-zero-trust-gateway

**Priorité : P0** | Durée : 3–4 semaines | Différenciant FDE le plus net en entretien

## Pourquoi maintenant

ENISA Threat Landscape 2026 (22/09/2026) : 73 % des cibles = entités NIS2 ; terrain : pas de « firewall GenAI » mature. Un prompt malveillant peut abuser des tools d'un agent (virement, suppression, exfiltration).

## Mission jusqu'en prod

Gateway Zero Trust sur MCP : chaque tool call est authentifié, autorisé (OPA), audité. Playbooks SOC « agent compromis » : alerte + bascule en lecture seule.

## Stack

- Gateway MCP (Python, FastMCP ou équivalent)
- OPA (Open Policy Agent) pour les politiques d'autorisation
- Keycloak pour l'identité des agents et des utilisateurs
- Tools métier mock (virement, lecture CRM, envoi email)
- SIEM-lite (logs structurés, alertes)
- Docker Compose pour la démo locale

## Livrables

- [ ] Gateway MCP avec authn/authz par tool
- [ ] Politiques OPA versionnées (lecture vs écriture vs irréversible)
- [ ] 3 tools mock avec contrats d'interface
- [ ] Démo : prompt malveillant → virement bloqué → alerte + mode lecture seule
- [ ] Runbook « agent compromis »
- [ ] README : architecture, démarrage, démo, limites

## Garde-fous

- Aucun tool irréversible sans validation humaine explicite
- Quotas par agent (nombre d'appels, budget)
- Audit trail complet : qui, quoi, quand, pourquoi
- Rollback : désactivation d'un tool en une commande

## Sources

- [ENISA ETL 2026 — communiqué](https://www.enisa.europa.eu/news/exploring-the-evolution-of-the-cyber-threat-landscape-how-dependencies-weaken-our-digital-resilience)
- [ENISA ETL 2026 — PDF](https://www.enisa.europa.eu/sites/default/files/2026-09/ENISA%20Threat%20Landscape%202026_Final.pdf)