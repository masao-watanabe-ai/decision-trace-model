# decision-trace-model

Decision Trace Model is a conceptual architecture for
externalizing decision logic from AI systems.

Instead of embedding decisions inside model weights,
application code, or implicit operational rules,
the model represents decision processes as explicit,
traceable structures.

This enables AI systems to preserve not only the final result,
but also the reasoning path that led to the decision.

---

# Core Structure

A decision process is represented as the following pipeline:

Event
↓
Signal
↓
Decision Contract
↓
Behavior Tree
↓
Human Boundary
↓
Decision Ledger

Each layer plays a specific role:

* **Event** – Observed facts or inputs from the environment
* **Signal** – Predictions or scores produced by AI models
* **Decision Contract** – Explicit decision rules describing how signals are interpreted
* **Behavior Tree** – Execution structure controlling how decisions are evaluated
* **Human Boundary** – Points where human confirmation or responsibility is required
* **Decision Ledger** – Immutable records of how the decision was produced

Through this structure, decision-making becomes an explicit,
auditable, and reusable object within AI systems.

---

# Decision Ledger

The **Decision Ledger** preserves decision histories as
append-only records.

A ledger entry contains:

* the full **decision trace**
* execution context
* model and policy versions
* audit metadata
* integrity information

This ensures that decisions can be:

* audited
* reproduced
* explained
* traced across time

The ledger concept is inspired by systems used in:

* financial auditing
* safety-critical engineering
* distributed systems
* blockchain-style append-only logs

In the Decision Trace Model, the ledger acts as the
**historical memory of decision systems**.

---

# Example Decision Traces

Two example domains are provided to illustrate how the
Decision Trace Model can represent decision processes
across different industries.

## Manufacturing

Material selection decision trace for engineering design.

Example scenario:

* selecting materials for components
* evaluating corrosion risk
* balancing cost and safety constraints
* recording design decision reasoning

## Retail

Store promotion decision trace for operational store decisions.

Example scenario:

* detecting high inventory risk
* triggering promotional actions
* applying store policy constraints
* recording operational decisions

Each example demonstrates how the following components
work together to represent decision processes:

* `ontology.json` – defines the semantic structure of decision elements
* `decision-contract.dsl` – describes decision logic as explicit contracts
* `behavior-tree.yaml` – defines the execution flow of the decision process
* `trace-example.json` – shows the final recorded decision trace
* `ledger-example.json` – shows how the trace is preserved in the decision ledger

---

# Schemas

This repository also includes reference schemas for the
core structural components of the Decision Trace Model.

```
schemas/
├─ ontology.schema.json
├─ decision-contract.schema.json
├─ behavior-tree.schema.json
├─ decision-trace.schema.json
└─ decision-ledger.schema.json
```

These schemas define the structural representation of:

* decision ontologies
* decision contracts
* behavior tree execution flows
* decision traces
* decision ledger records

The schemas serve as a **reference specification** for
implementing traceable decision systems across different platforms.

Note that:

* `decision-contract.dsl` represents the **human-readable decision logic**
* `decision-contract.schema.json` represents the **structured form of contracts after parsing**

---

# Related Repositories

### decision-trace-engine

Runtime engine for executing decision contracts and
recording decision traces.

### decision-trace-studio

Tools for inspecting, visualizing, and editing decision structures.

### decision-trace-platform

Platform architecture for building traceable decision systems.

---

# Articles

This repository accompanies a series of articles explaining
the Decision Trace Model.

Blog
[https://deus-ex-machina-ism.com](https://deus-ex-machina-ism.com)

LinkedIn
[https://www.linkedin.com/in/masao-watanabe/](https://www.linkedin.com/in/masao-watanabe/)


