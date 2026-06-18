# Amazon Product Manager Skill

A Codex skill for Amazon marketplace product decisions: market screening, product selection, launch planning, profit repair, growth review, inventory risk, and stop-loss calls.

中文说明: [docs/README.zh-CN.md](docs/README.zh-CN.md)

Related projects:

- Integrated agent for end-to-end routing: [amazon-pm-integrated-agent](https://github.com/ianyoufather-2007/amazon-pm-integrated-agent)
- Lightweight agent wrapper: [01-product-manager-workflow-agent](https://github.com/ianyoufather-2007/01-product-manager-workflow-agent)

Use this repository when you want the core Codex skill. Use `amazon-pm-integrated-agent` when you want a cleaner agent layer that routes loose product ideas into PM triage or QYPM-style stage gates.

This project is designed for small Amazon sellers and lean product teams that need product-manager discipline without large-company overhead. It helps an AI agent convert incomplete marketplace evidence into explicit decisions, metrics, next actions, and risks.

## 中文快速开始

这是一个给 Codex / AI Agent 用的 Amazon 产品经理决策 skill。它不是爬虫，也不是“自动出爆品”的工具，而是帮助 AI 按产品经理流程做市场筛选、产品机会判断、Launch 计划、利润修复、库存风险和 Go / No-Go 决策。

安装后可以直接这样问：

```text
使用 $amazon-product-manager 帮我判断 Amazon US 的 coffee capsule holder 市场是否值得进入。

我的约束：
- 小品牌
- 首批预算有限
- 可做竹木、陶瓷或轻金属材质
- 目标售价 $15-$35

请输出 Enter Market / Watch Market / Avoid Market 决策、最适合的小切口、还缺什么证据、主要风险和未来 7 天验证计划。
```

完整中文说明见：[docs/README.zh-CN.md](docs/README.zh-CN.md)

## What It Does

- Screens markets, categories, niches, price bands, and product lines before choosing a SKU.
- Evaluates demand, competition, economics, differentiation, operations, capital pressure, and compliance risk.
- Produces decisions such as `Enter Market`, `Watch Market`, `Avoid Market`, `Go`, `No-Go`, `Test First`, `Rework Offer`, and `Kill or Liquidate`.
- Creates structured artifacts: market screening memos, product selection memos, launch plans, profit rescue plans, inventory reviews, weekly business reviews, and stop-loss memos.
- Keeps assumptions visible when data is missing.

## Repository Structure

```text
skills/
  amazon-product-manager/
    SKILL.md
    agents/openai.yaml
    references/
      amazon-decision-framework.md
      amazon-pm-templates.md
      market-screening-framework.md
examples/
docs/
```

## Installation

Copy the skill folder into your Codex skills directory.

Windows PowerShell:

```powershell
$src = ".\skills\amazon-product-manager"
$dst = "$env:USERPROFILE\.codex\skills\amazon-product-manager"
New-Item -ItemType Directory -Force -Path (Split-Path $dst) | Out-Null
Copy-Item -Recurse -Force $src $dst
```

macOS/Linux:

```bash
mkdir -p ~/.codex/skills
cp -R skills/amazon-product-manager ~/.codex/skills/amazon-product-manager
```

Restart Codex after installing the skill.

## Example Prompt

```text
Use $amazon-product-manager to evaluate whether I should enter the coffee capsule holder market on Amazon US. I have a small brand, limited launch budget, and can source metal or bamboo products. Give me an Enter/Watch/Avoid decision, evidence needed, first wedge, risks, and next actions.
```

More examples are in `examples/`, including an anonymized market-screening output: [examples/anonymized-market-screening-output.md](examples/anonymized-market-screening-output.md).

## Data And Privacy

This skill does not require bundled private data. Bring your own marketplace evidence: keywords, ASINs, price bands, review summaries, cost assumptions, FBA estimates, PPC metrics, or inventory data.

Do not commit account credentials, browser session folders, raw customer data, supplier quotes, proprietary exports, or paid-tool datasets unless you have permission to publish them.

## License

MIT
