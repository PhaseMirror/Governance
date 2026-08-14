# Phase Mirror Governance Stack

Welcome to the **Phase Mirror Governance Stack**. This repository contains the canonical policies, agent operational instructions, and architectural mandates governing the Phase Mirror project, its mathematical core (PIRTM), and its legal/ESI integration layer (Sedona Spine).

## 1. Architectural Overview

The Phase Mirror ecosystem is built upon a deterministic, mathematically verifiable foundation governed by strict rules on system modification, legal compliance, and agent operations. The stack bridges:

- **PIRTM (Prime-Indexed Runtime Model)**: A standalone runtime and verified MLIR dialect ensuring contractive session execution.
- **Sedona Spine**: A Rust Engine and WASM SDK acting as the sole mandatory source of truth for all Electronic Stored Information (ESI) retention, litigation hold, and spoliation risk logic.
- **API-Based Agents**: Workbench-integrated agents operating strictly within the governance framework.

## 2. Constitutional Frame & The Math-First Rule

All system behavior is governed by the **Ξ-Constitution v1.0**. 
Lawful evolution obeys `Ξ(t+1) = Ψ(Ξ(t))` where `Ψ = PIRTM ∘ CSL ∘ Langlands ∘ Attestation ∘ DriftAudit`.

### Engineering Mandates:
- **Math-First**: PIRTM is treated as mathematics expressed in code. All operations require executable certification coverage.
- **L0 Invariants**: Strict guarantees around transpile-time contractivity checks, link-time spectral-small-gain proofs, and prime-indexed modules.
- **Self-Modification Boundaries**: The `governance/self_modification/` surface is highly restricted, requiring pre-checks through `lobian_guard.py`, `watchdog.py` state transitions, and a CI-tested `kill_switch.py`.

## 3. Legal and ESI Governance (PhaseMirror-Legal)

For all ESI-related operations within Phase Mirror, the **Sedona Spine Mandate** enforces:

- **Zero Drift**: No agent, UI component, or backend service may independently calculate preservation risk levels or retention durations.
- **Path of Integrity**: All legal logic strictly routes through: `Engine (Rust)` → `SDK (TS/WASM)` → `Contract (CONTRACT.md)` → `UI/Agent`.
- **Policy-Driven Variation**: Domain-specific legal variation exists only in declarative YAML policies, not in hardcoded logic. Agents transform engine-computed facts into narratives but never override core risk computations.

## 4. Agent Operational Integrity & Gateways

Agents operate via the PhaseMirror Workbench and maintain L0 governance:

| Agent | Purpose | API Endpoint |
| :--- | :--- | :--- |
| **Legalese Scopist** | ESI retention auditing & spoliation risk | `http://localhost:3000/v1` |
| **The Commander** | Governed operator shell & workflow execution | `http://localhost:3001/v1` |

AI-generated work touching ESI must satisfy the provenance chain: **Policy** → **Event Log** → **Kernel Computation** → **Narrative**.

## 5. Development & AGI Readiness Gates

Project development is strictly gate-ordered by specific AGI Readiness ADRs (Architectural Decision Records). You must not work past a later ADR before earlier acceptance criteria pass.

- **ADR Repository**: `artifacts/docs/adr/`
- **Key Gates**: Governance Ledger Binding, CI-Enforced Gate Sequencing, Self-Modification Boundary Audits, Runtime Contractivity Scope.

## Reference Artifacts

- **Project Context & Agent Instructions**: `AGENTS.md`, `GEMINI.md`
- **Engine Core**: `models/legalese-scopist/`
- **Agent Contracts**: `CONTRACT.md`

---
*For contributing to the implementation or updating policies, please refer to the specific gate sequencing rules and escalation protocols defined in `AGENTS.md`.*