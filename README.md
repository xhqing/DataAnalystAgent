<div align="center">

<img src="assets/logo.svg" width="640" alt="Echo logo" />

![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)
![Stars](https://img.shields.io/github/stars/xhqing/DataAnalystAgent?style=social)
![Last Commit](https://img.shields.io/github/last-commit/xhqing/DataAnalystAgent)
![AI Agent](https://img.shields.io/badge/Type-AI%20Agent-FF1493)
<img src="https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/xhqing/xhqing/main/traffic/badges/DataAnalystAgent.json" alt="Visits/day (14d)" />

</div>

# DataAnalystAgent · Echo

> **数据分析师** — 流水线的反馈回路与学习引擎，做归因、分发建议、沉淀打法库。
>
> **Data Analyst** — The feedback loop that attributes outcomes to decisions, routes advice to each agent, and compounds learnings into a playbook.

**拟人名 / Persona：Echo**（回声 · 让业绩「回声」成整条链路的反馈）

---

## 职责 / What it does

把成交 / 流量 / 退款数据**归因**到各环节决策，产出：① 分发式建议（按环节写给对应 agent）；② 累积 playbook（打法库，供所有 agent 查询）。

Attributes outcomes to each stage's decisions and produces: ① routed advice per agent; ② a cumulative playbook queryable by all agents.

## 在流水线中的位置 / Pipeline position

① Scout 研判 → ② Wright 生产 → ③ Buzz 引流 → ④ Vendy 成交 → ⑤ **Echo** 复盘（建议回流给前面所有环节）

## 内置能力 / Built-in skills

- `anysearch` · `find-skill` — 通用搜索与技能发现

## 约束 / Constraints

归因依赖产物契约的可追溯标签（`product_id` / `trend_id` / `channel` / `campaign_id`）；对前段（选品）宽容、对后段（成交）采信。

## License

MIT
