# PATi — Private Algorithmic Trading (international)

**Shared Oxygen, LLC**

---

## Executive summary

**PATi** (Private Algorithmic Trading) is a **self-hosted** algorithmic trading platform: strategy logic, learning signals, and operator workflows run on **your infrastructure**—so sensitive research, agent behavior, and trade history are not a SaaS product’s dataset. The product pairs a **Mission Control** operator console with an **end-to-end operating rhythm** from premarket preparation through intraday management and end-of-day discipline, designed for **equities, options, and crypto** in a **single** configurable stack.

PATi is built around a **council of specialized AI roles** (not a single “do-everything” model). Multiple perspectives feed a **consensus** decision, while a **Risk** function can **veto** proposals that fail portfolio constraints—governance that mirrors how professional desks separate idea generation from risk approval.

PATi does **not** promise returns. It is positioned for operators who want **discipline, auditability, and continuous improvement** under their own control.

---

## Visual summary

At-a-glance relationship maps: how custody, decisions, the trading day, and learning reinforce each other.

### Figure 1 — Custody: your control plane

```mermaid
%%{init: {"theme": "base"}}%%
flowchart TB
  subgraph yp["Your organization"]
    direction TB
    UI["Operator console\n(Mission Control)"]
    core["PATi stack\n(automation + lifecycle)"]
    local["On-prem AI\n(optional)"]
    UI <--> core
    core <--> local
  end
  subgraph rel["Your brokers and data"]
    br["Execution venues"]
    data["Research & data feeds\n(you entitle)"]
  end
  core --> br
  core --> data

  style yp fill:#EEF2FF,stroke:#6366F1,stroke-width:2px
  style rel fill:#ECFDF5,stroke:#10B981,stroke-width:2px
  style UI fill:#4F46E5,stroke:#312E81,stroke-width:2px,color:#F8FAFC
  style core fill:#7C3AED,stroke:#5B21B6,stroke-width:2px,color:#FAF5FF
  style local fill:#F59E0B,stroke:#B45309,stroke-width:2px,color:#1C1917
  style br fill:#10B981,stroke:#047857,stroke-width:2px,color:#F0FDF4
  style data fill:#0EA5E9,stroke:#0369A1,stroke-width:2px,color:#F0F9FF
```

**Takeaway:** you retain governance of research, prompts, and trade history—on your side of the boundary. **Brokers, data, and terms are yours to configure.**

### Figure 2 — Governance: specialists, consensus, risk gate

```mermaid
%%{init: {"theme": "base"}}%%
flowchart LR
  subgraph inputs["Specialist perspectives"]
    direction TB
    sp["Multiple AI roles\n(each domain-focused)"]
  end
  sp --> cs["Consensus synthesis"]
  cs --> rv{"Risk & portfolio limits\n(approve or veto)"}
  rv -->|Approved| ex["Order lifecycle &\nprotective discipline"]
  rv -->|Veto| aud["Block + audit trail"]
  ex --> mkt["Markets (your brokers)"]

  style inputs fill:#FAF5FF,stroke:#C084FC,stroke-width:2px
  style sp fill:#A855F7,stroke:#6B21A8,stroke-width:2px,color:#FAF5FF
  style cs fill:#3B82F6,stroke:#1E3A8A,stroke-width:2px,color:#EFF6FF
  style rv fill:#F97316,stroke:#9A3412,stroke-width:2px,color:#FFFBEB
  style ex fill:#22C55E,stroke:#14532D,stroke-width:2px,color:#F0FDF4
  style aud fill:#F43F5E,stroke:#9F1239,stroke-width:2px,color:#FFF1F2
  style mkt fill:#14B8A6,stroke:#0F766E,stroke-width:2px,color:#F0FDFA
  linkStyle 0 stroke:#7C3AED,stroke-width:2px
  linkStyle 1 stroke:#2563EB,stroke-width:2px
  linkStyle 2 stroke:#16A34A,stroke-width:2px
  linkStyle 3 stroke:#E11D48,stroke-width:2px
  linkStyle 4 stroke:#0D9488,stroke-width:2px
```

**Takeaway:** idea generation and **permission to proceed** are separate—like a professional desk, not a single opaque score.

### Figure 3 — Operating cadence (typical market day)

```mermaid
%%{init: {"theme": "base"}}%%
flowchart LR
  pr["Preparation &\nscreening"] --> id["Intraday\nworkflows"]
  id --> pm["Ongoing\nposition oversight"]
  pm --> dh["End-of-day\ndiscipline and wrap-up"]
  dh -.->|next session| pr

  style pr fill:#FCD34D,stroke:#B45309,stroke-width:2px,color:#422006
  style id fill:#38BDF8,stroke:#0369A1,stroke-width:2px,color:#082F49
  style pm fill:#A78BFA,stroke:#5B21B6,stroke-width:2px,color:#2E1065
  style dh fill:#FB7185,stroke:#9F1239,stroke-width:2px,color:#4C0519
  linkStyle 0,1,2 stroke:#6366F1,stroke-width:3px
  linkStyle 3 stroke:#F43F5E,stroke-width:2px
```

**Takeaway:** automation is a **day cycle**, not a one-off backtest or alert script.

### Figure 4 — Learning loop

```mermaid
%%{init: {"theme": "base"}}%%
flowchart LR
  oc["Closed trades &\noperational metrics"] --> ms["Attribution &\nquality measurement"]
  ms --> pl["Tuning under policy\n& configuration"]
  pl -.->|informs next decisions| cal["Ongoing\nselectivity & calibration"]

  style oc fill:#475569,stroke:#0F172A,stroke-width:2px,color:#F8FAFC
  style ms fill:#8B5CF6,stroke:#4C1D95,stroke-width:2px,color:#F5F3FF
  style pl fill:#EC4899,stroke:#9D174D,stroke-width:2px,color:#FDF2F8
  style cal fill:#22D3EE,stroke:#0E7490,stroke-width:2px,color:#042F2E
  linkStyle 0,1 stroke:#A78BFA,stroke-width:2px
  linkStyle 2 stroke:#F472B6,stroke-width:2px
```

**Takeaway:** selectivity and clarity tighten as evidence accumulates, within policies you set.

### Figure 5 — How teams often automate

```mermaid
%%{init: {"theme": "base"}}%%
flowchart TB
  a["A — Signals & research\nthen wire execution"]
  b["B — Vendor-hosted quant\neconomy & scale"]
  c["C — PATi: private stack\ncouncil + risk gate + custody"]

  style a fill:#E2E8F0,stroke:#94A3B8,stroke-width:2px,color:#0F172A
  style b fill:#BFDBFE,stroke:#3B82F6,stroke-width:2px,color:#1E3A8A
  style c fill:#4F46E5,stroke:#1E1B4B,stroke-width:4px,color:#F5F3FF
```


*A, B, and C are different build-or-buy patterns—**not** steps in one workflow.*

PATi is the third: **operator custody** and a **governed** end-to-end stack—in one self-hosted product, not a chain of point tools.

---

## The problem PATi addresses

Most trading failures are operational: the gap between backtests and live markets, weak execution hygiene, and systems that cannot explain *why* a trade was taken or blocked. Single-model approaches often collapse many domains (technicals, sentiment, derivatives structure, events, and portfolio risk) into one abstraction—raising both blind spots and fragility when regimes change.

PATi’s design thesis is that **trading is multi-domain work**, and that robust automation should look like a **governed process**: specialists contribute evidence, a consensus synthesizes, risk can say “no,” and outcomes feed a **closed-loop** improvement cycle.

---

## What makes PATi distinctive

| Theme | What it means for an operator |
| --- | --- |
| **Privacy & control** | Run on premises; use **your** data subscriptions and **your** execution relationships. Core intelligence can use **local** large-language model inference, avoiding dependency on a cloud model vendor for the core stack. |
| **Specialist council + governance** | Multiple AI roles (strategy, technicals, sentiment, options, exits, macro, events, anomaly detection, and post-trade learning) feed a **consensus**; **Risk** can **veto**—hard separation of “idea” vs “permission.” |
| **Autonomous operations** | Scheduled workflows from **premarket** through **intraday** activity, **position lifecycle management**, and **end-of-day** processes—an operating cadence, not a one-off script. |
| **Cross-asset, one platform** | A unified operator experience and automation fabric across **equities, options, and crypto** with **broker-agnostic** integration (configurable; primary institutional-grade connectivity where supported by your brokers). |
| **Capital-protection discipline (NLWTIAL)** | “Never Let a Winner Turn Into a Loser” is **policy**, not a slogan: structured progression from protection at entry through breakeven and trailing behavior, with **MFE/MAE**-style position analytics to support defensible risk management. |
| **Global session readiness (optional)** | When enabled, a **multi-market** scheduler coordinates regional workflows and keeps market-scoped state coherent—relevant to operators who want one control plane across regions, not a patchwork of scripts. |
| **Transparency** | Decisions, vetoes, and execution attempts are intended to be **auditable** so leadership can answer “what happened, and why” with evidence—not folklore. |
| **Self-improvement** | Outcomes are fed back to calibrate selectivity, weights, and confidence over time, under configuration control—tighten when evidence says tighten. |

---

## Who PATi is for

- **Systematic trading leaders** who need repeatable automation with governance.
- **Security- and IP-sensitive** teams who will not cede **strategy, prompts, and transaction metadata** to a multi-tenant cloud.
- **Operators** who value **exits, risk, and process** as the durable edge—not ad hoc alpha rumors.
- **Builders** who want a full platform to extend, not a closed black box.

---

## Market context: what PATi is built to lead

Competing and adjacent tools are named **only to anchor categories** in the footnotes; the point is not to catalogue their roadmaps, but to state what PATi **is architected to combine** in one **operator-run** system—each row is a **product commitment** (see “What makes PATi distinctive” above and your deployment configuration), not a performance promise.

| Where PATi is purpose-built | What PATi delivers (product fact) | What is usually elsewhere in the market |
| --- | --- | --- |
| **Custody of IP and data** | Runs on **your** infrastructure; your strategy, prompts, and operating history are not a shared SaaS dataset by design. | Many stacks centralize **research, execution, or charting in vendor or broker** environments. |
| **Governed machine intelligence** | A **council of specialist roles** with **consensus** and a **separate Risk veto**—explicit separation of “generate ideas” vs “permit risk.” | Typical automation is a **single model, single “bot,”** or **research tool without portfolio veto gating** in the same product. |
| **End-to-day operating system** | **Scheduled** workflows from premarket through intraday, **position lifecycle**, and **end-of-day** discipline in **one** stack. | The market is full of **strong point solutions** (charts, backtests, APIs) that still leave **stitching and ops** to the team. |
| **Cross-asset, one operator plane** | **Equities, options, and crypto** through **configurable** broker relationships in a **unified** Mission Control. | Teams often run **separate** tools or **regional** stacks per asset class. |
| **Enforced loss-avoidance discipline (NLWTIAL)** | “Never Let a Winner Turn Into a Loser” is a **stated** operating doctrine with **staged** protective action—not an optional add-on. | **Exit discipline** is often left to discretion or a separate system. |
| **Optional global session awareness** | **Multi-market** scheduling and **market-scoped** state when you turn it on—**one** control model for more than one region. | **Regional** or **separate** schedulers are the common default. |
| **Audit and learning under policy** | Decisions, vetoes, and execution attempts are intended to be **auditable**; outcomes feed **calibration** under **your** config policy. | **Provenance and tuning** are often **fragmented** across notebooks, logs, and ad hoc scripts. |

A **broker** (e.g. [IBKR](https://www.interactivebrokers.com/en/trading/ib-api.php), [Alpaca](https://alpaca.markets/)) is a **counterparty and connection**, not a substitute for a full **governance, council, and workflow** product—PATi sits **above** the wire you select.

**Irrefutability standard:** the left column is **architectural intent**; the middle column matches **PATi’s public product description** in this material. The right column is a **broad** industry pattern (not a review of a single vendor) and is **not** a feature matrix.

### References (categories only)

- **Hosted quant + open engine** — [QuantConnect](https://www.quantconnect.com/) · [LEAN](https://www.lean.io/)  
- **Widely distributed retail (FX/CFD class) platform family** — [MetaTrader 5 — algorithmic trading](https://www.metatrader5.com/en/automated-trading)  
- **Futures- / NinjaScript-centered platform** — [NinjaTrader](https://ninjatrader.com/trading-platform/)  
- **Charting + Pine (strategy mode per vendor help)** — [TradingView — autotrade & Pine](https://www.tradingview.com/support/solutions/43000481026-how-to-autotrade-using-pine-script-strategies/)  
- **US API-first broker (example class)** — [Alpaca](https://alpaca.markets/)  
- **Global multi-asset broker + APIs (venue class)** — [IBKR API](https://www.interactivebrokers.com/en/trading/ib-api.php)

---

## Disclosures

Algorithmic systems can connect to **live markets**. All trading involves risk of loss. Past or simulated performance does not guarantee future results. Operators remain responsible for **regulatory compliance**, **suitability**, **market data entitlements**, and **broker terms** in their jurisdictions. This document is **not** investment advice.

---

**Shared Oxygen, LLC** · **PATi** — Private Algorithmic Trading
