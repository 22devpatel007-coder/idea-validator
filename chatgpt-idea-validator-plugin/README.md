# ChatGPT Idea Validator

A reusable ChatGPT skill package for evidence-based evaluation of products, startups, SaaS, apps, services, and business ideas.

## What is included
- Main skill instructions (`SKILL.md`)
- Seven research perspectives
- Evidence audit and weighted scoring
- Separate research-confidence assessment
- BUILD / TEST / MODIFY / REJECT decision rules
- Quick and deep workflows
- Report and assumption-register templates
- Mermaid architecture diagram
- Plugin Creator setup prompt

## Important platform note
This package is not a standalone application, and it does not create seven autonomous agents. The seven perspectives are structured research roles. ChatGPT should use web search and any enabled capabilities that are actually available. It must not claim parallel agents ran unless the platform truly ran them.

ChatGPT's product setup and availability can vary by account and workspace. For this package, the intended route is to use the **Plugin Creator** app to create a reusable ChatGPT plugin containing this skill and its reference files. If Plugin Creator is unavailable, use the included instructions as a reusable prompt in a normal ChatGPT conversation or supported workspace.

## Setup using Plugin Creator
1. Extract this ZIP.
2. Open the Plugin Creator app in ChatGPT (if available).
3. Give it the contents of `PLUGIN_CREATOR_PROMPT.md`.
4. Attach or provide `SKILL.md`, the files in `references/`, `workflows/`, and `templates/`.
5. Ask it to create a plugin named **Idea Validator** with one skill named **idea-validator**.
6. Ensure the skill's behavior rules are in its main instructions. Keep the reference documents as supporting material.
7. Enable web research/search if the plugin setup offers that capability.
8. Test with the sample prompt below.
9. Review the plugin's output for fabricated claims, unsupported market sizing, and false confidence before relying on it.

Plugin Creator may require user confirmation or additional configuration. This ZIP does not install or publish a plugin automatically.

## Plugin Creator prompt
See `PLUGIN_CREATOR_PROMPT.md`.

## Test prompt
> Use Idea Validator to deeply evaluate this idea: an appointment and reminder platform for independent dental clinics in India. Research customer demand, competitors, alternatives, pricing, distribution, technical feasibility, costs, and risks. Cite sources. Give me a BUILD / TEST / MODIFY / REJECT verdict and the cheapest experiment to validate willingness to pay.

## Research limitations
- Web research may not be available in every conversation or workspace.
- Desk research cannot prove product-market fit.
- Customer willingness to pay needs real-world evidence.
- Scores are decision aids, not probabilities.
- Financial scenarios depend on assumptions.
- The user makes the final business decision.

## Portability
The research methodology and report formats can be reused in Claude Skills, Codex, or other tools, but their installation and tool instructions must be adapted to each platform.
