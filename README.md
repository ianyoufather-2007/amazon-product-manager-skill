# Amazon Product Manager Skill

A Codex skill for Amazon marketplace product decisions: market screening, product selection, launch planning, profit repair, growth review, inventory risk, and stop-loss calls.

This project is designed for small Amazon sellers and lean product teams that need product-manager discipline without large-company overhead. It helps an AI agent convert incomplete marketplace evidence into explicit decisions, metrics, next actions, and risks.

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

More examples are in `examples/`.

## Data And Privacy

This skill does not require bundled private data. Bring your own marketplace evidence: keywords, ASINs, price bands, review summaries, cost assumptions, FBA estimates, PPC metrics, or inventory data.

Do not commit account credentials, browser session folders, raw customer data, supplier quotes, proprietary exports, or paid-tool datasets unless you have permission to publish them.

## License

MIT
