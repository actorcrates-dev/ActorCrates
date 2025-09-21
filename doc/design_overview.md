# ActorCrate Design Overview

## 1. Purpose & Scope
ActorCrate is a modular framework for simulating high-fidelity agents derived from public figures, archival data, or user-provided corpora. It is designed for research, education, and scenario-driven exploration, enabling users to interact with, observe, and stress-test agent behavior in controlled environments.

## 2. System Architecture
- **Corpus Ingestion:** Pipelines for transforming raw data (text, audio, video, metadata) into agent-ready formats.
- **Agent Libraries:** Parameterized agent definitions (traits, states, provenance, consent status).
- **Simulation Layer:** Scenario engine, stateful agent interactions, event loop, and scenario builder.
- **UX Interface:** Markdown/GUI outputs, scenario builder, audit logs, and clear distinction of agent speech/actions/logs.
- **Governance/Guardrails:** Consent management, ethical constraints, auditability, and provenance tracking.

## 3. Data & Agent Schemas
- YAML schemas define agents, scenarios, and sessions.
- Schemas are extensible for new agent types, scenario formats, and metadata fields.
- See `docs/agent_schema.yaml` for current drafts.

## 4. Simulation Workflow
1. **Corpus Ingestion:** Process and structure source data.
2. **Agent Instantiation:** Create agents with defined traits and provenance.
3. **Scenario Setup:** Define environment, prompts, overlays, and agent roles.
4. **Simulation Run:** Agents interact, states and metadata are dynamically updated.
5. **Output & Audit:** Generate structured logs, behavioral reports, and audit trails.

## 5. Differentiators
- **Structured Agent Depth:** Agents have substrates (dispositions), perturbations (stressors), and activators (triggers).
- **Simulation Layering:** Stateful sessions, agent self-reflection, and "play against type" capabilities.
- **Real-World Anchoring:** Agents instantiated from public figures/archetypes using accessible corpora.
- **Interpretability:** Metadata streams (emotional state, cognition logs, cluster position) for transparency.
- **Ethics by Design:** Explicit guardrails, consent, and provenance from the start.

## 6. Extensibility & Modularity
- Add new agents, corpora, or scenario types via modular schemas and plug-in points.
- Designed for community contributions and collaborative archetype/scenario building.

## 7. Roadmap & Open Questions
- See `docs/roadmap.md` for milestones and planned features.
- Current open questions:
  - How to optimize document throughput under rate limits?
  - What additional ethical guardrails are needed?
  - How to best support community-driven archetype libraries?
