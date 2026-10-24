# Jiawise

**Your housing decisions, made wise.**
让每一个住房决策，都算得明白。

Jiawise is a personalized housing-decision engine. Tell it your finances, your time horizon, and what's changing in your life — a new baby, a move to a new city, a job change, a kid starting school — and it works out whether you should **rent, buy, invest, sell, or hold**, shows the math behind the recommendation, and gives you a concrete action plan.

> **中文说明见下方。**

---

## Why Jiawise?

Existing tools each answer one narrow question, and none of them talk to each other:

- **Rent-vs-buy calculators** (NYT, Zillow, Bankrate) are static and financials-only, with opaque assumptions — the same inputs can produce a breakeven anywhere from 4 to 8 years depending on the calculator.
- **Sell-channel comparison sites** are lead-generation funnels with a built-in conflict of interest.
- **Short-term-rental tools** (AirDNA, BNBCalc) estimate revenue, not decisions.

Nobody combines **life-event modeling + sell-channel comparison + short-term-rental analysis + scenario planning** in one personalized, transparent product. That is the gap Jiawise fills.

## Features

**Five decision paths, one engine:**

1. **Rent vs. Buy** — a full breakeven calculation (price, rent, down payment, rate, horizon, transaction costs) that tells you the exact year buying starts to win.
2. **Invest** — compare living in it, long-term renting it out, or running it as a short-term rental (Airbnb), with cash-flow and return estimates.
3. **Sell / Exit** — every exit channel side by side, ranked by **net proceeds**: traditional agent, discount brokerage (Redfin), iBuyer (Opendoor), cash buyer, FSBO, or keep it and rent it out.
4. **Relocation optimizer** 👀 our signature module — moving cities? It compares *sell the old home and invest the proceeds* vs. *keep it as a rental*, across long-term wealth and cash flow.
5. **Education & school districts** — test into a gifted program, buy into a top school district, or run both tracks in parallel — weighed against district home prices, prep costs, and private-school fallback costs.

**Life-event engine** — life changes are first-class inputs, not afterthoughts: having a baby, a child starting school, relocating for work, income changes, caring for family, divorce, retirement / downsizing.

**Transparent math ("show your work")** — the engine is a fully inspectable rules engine. Every assumption is visible and adjustable; every recommendation comes with its reasons. No black box.

**Real channels, one click away** — recommendations link straight out to the real services: [Redfin](https://www.redfin.com), [Zillow](https://www.zillow.com), and [Opendoor](https://www.opendoor.com).

**Bilingual** — full Chinese / English interface, switchable in one tap (中文 / EN).

## How it works

```
Your inputs                          Jiawise engine                     Your plan
─────────────────────                ──────────────────────────────     ─────────────────────
Finances (savings, income)     ──►   Breakeven & cash-flow models  ──►  Recommendation
Time horizon                   ──►   Life-event rule adjustments   ──►  Why (visible math)
Life events (baby, move, …)    ──►   Channel net-proceeds ranking  ──►  3-step action checklist
Risk appetite                  ──►   Scenario simulation           ──►  Links to real channels
```

## Tech

This POC is a **single self-contained static page** (`index.html`) — the entire decision engine runs client-side in JavaScript. No backend, no build step, no data leaves the browser.

| File | Purpose |
| --- | --- |
| `index.html` | The whole app: UI + decision engine |
| `space.json` | Runtime metadata |
| `icon.jpg` | Brand icon |

## Run it

Just open `index.html` in a browser. That's it.

## Roadmap

- Live market data (prices, rents, rates) instead of adjustable sample assumptions
- User accounts and saved scenarios
- Learning from real user outcomes (ML ranking on top of the transparent rules)
- More life events and more cities

## Disclaimer

Jiawise is a proof of concept. Figures shown in the app are illustrative estimates based on adjustable assumptions, **not financial advice**. Verify any real transaction with licensed professionals.

---

## 中文说明

**Jiawise 是一个个性化房产决策引擎。**

输入你的资金状况、收入稳定性、计划居住年限和人生事件（生娃、换城市、换工作、孩子入学……），Jiawise 会算出你应该 **租房、买房、投资、卖房还是继续持有**，把每一步的计算过程透明地展示出来，并给出一份可以直接执行的行动清单。

**五条决策路径：**

1. **租还是买** —— 完整的盈亏平衡测算，告诉你从第几年开始买比租划算
2. **怎么投资** —— 自住、长租、短租（Airbnb）三种用法对比
3. **怎么退出** —— 传统中介、折扣中介（Redfin）、iBuyer（Opendoor）、现金收购、自己卖，按**净到手收益**排序
4. **搬迁优化器**（核心特色）—— 换城市时，老房子是卖掉拿钱投资，还是留着出租，长期财富和现金流一比便知
5. **教育与学区** —— 考天才班、买学区房、还是双轨并行，结合学区房价、备考成本和私校备选一起算

**特点：** 人生事件是一等输入；数学全透明（show your work），每个假设都可调；推荐结果直达 Redfin / Zillow / Opendoor 真实渠道；中英双语界面一键切换。

**技术：** 纯静态单页（`index.html`），决策引擎全部在浏览器端运行，无后端、无构建步骤。用浏览器打开 `index.html` 即可使用。

> 本项目为 POC（概念验证），页面数字为基于可调假设的估算，不构成理财建议。
