# 06 — agent-otel-observability

**Priorité : P1** | Durée : 2–3 semaines

## Pourquoi maintenant

Sans supervision, pas de MCI ni de preuve AI Act ni de ROI (Cigref / CIO Online). Les agents doivent être tracés bout-en-bout comme une API métier : prompts, tools, coût, dérive.

## Mission jusqu'en prod

Traces bout-en-bout des agents : chaque appel LLM, chaque tool call, chaque décision — avec coût et latence. Détection de dérive (écart comportemental vs baseline).

## Stack

- OpenTelemetry (SDK Java + Python)
- Tempo / Grafana (traces, flamegraphs)
- Agents sample (Java + Python)
- Redaction PII automatique
- Docker Compose

## Livrables

- [ ] Instrumentation OTel des agents sample
- [ ] Flamegraph tools par requête
- [ ] Coût par trace (€)
- [ ] Alerte dérive (écart vs baseline)
- [ ] Redaction PII dans les traces
- [ ] README : architecture, démarrage, démo, limites

## Garde-fous

- PII redactée avant export
- Rétention configurable
- Pas de trace sur données sensibles en clair

## Sources

- Cigref — ROI des solutions DIA générative et agentique
- CIO Online — GenAI : les DSI tentent de garder le contrôle

*Note : besoin terrain ; pas de norme unique imposée à ce jour.*