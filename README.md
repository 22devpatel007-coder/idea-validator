# Idea Validator

This folder has two ready-to-use versions of the same idea-validation system:

- [Claude Idea Validator Skill](claude-idea-validator-skill/) for Claude.
- [ChatGPT Idea Validator Plugin](chatgpt-idea-validator-plugin/) for ChatGPT.

**Jump to setup:**

- [Set up in Claude](#set-up-in-claude)
- [Set up in ChatGPT](#set-up-in-chatgpt)

The tool reviews a product, startup, app, service, or business idea. It looks for demand, competitors, costs, technical problems, and risks. It gives one verdict:

- **BUILD** — evidence supports starting.
- **TEST** — the idea is possible, but demand is not proven.
- **MODIFY** — change the customer, offer, price, or business model.
- **REJECT** — do not continue with the idea in its current form.

The result is a decision aid. It does not prove that an idea will succeed.

## Choose a platform

| Use case | Recommended setup |
|---|---|
| Claude desktop, web, or Claude Code | Claude Skill |
| ChatGPT desktop or web | Custom GPT, or Plugin Creator when it is available |

## Set up in Claude

### Option 1: Claude.ai

1. Open Claude.
2. Go to **Settings**.
3. Open the **Skills** section.
4. Create or add a custom skill.
5. Upload or package the folder [claude-idea-validator-skill](claude-idea-validator-skill/) as a skill.

The ZIP must contain `claude-idea-validator-skill/SKILL.md` at the top level, with the `references/`, `templates/`, and `workflows/` folders inside it.

Example ZIP layout:

```text
claude-idea-validator-skill/
  SKILL.md
  references/
  templates/
  workflows/
```

After setup, start a new chat and ask Claude to validate an idea. Claude should load the skill when the request matches it.

### Option 2: Claude Code

Copy the complete skill folder to Claude's personal skill directory:

```powershell
Copy-Item -Recurse ".\claude-idea-validator-skill" "$env:USERPROFILE\.claude\skills\idea-validator"
```

The final file must be here:

```text
%USERPROFILE%\.claude\skills\idea-validator\SKILL.md
```

Start Claude Code, then test it:

```text
/idea-validator
```

You can also ask normally:

```text
Use the idea-validator skill to test this idea:
An appointment and reminder app for independent dental clinics in India.
```

To use the skill only in one project, copy the folder to:

```text
.claude\skills\idea-validator\
```

### Claude setup files

- [SKILL.md](claude-idea-validator-skill/SKILL.md) contains the main instructions.
- [references](claude-idea-validator-skill/references/) contains research and scoring rules.
- [templates](claude-idea-validator-skill/templates/) contains report formats.
- [workflows](claude-idea-validator-skill/workflows/) contains quick, deep, comparison, and re-score steps.

## Set up in ChatGPT

ChatGPT account types and workspace features can differ. Use the best available option below.

### Option 1: Custom GPT

This is the simplest setup when your account can create GPTs.

1. Open ChatGPT and select **Explore GPTs**.
2. Select **Create**.
3. Open the configuration or setup view.
4. Set the name to **Idea Validator**.
5. Add this description:

   > Critically evaluate product and business ideas with market, customer, competitor, technical, and financial research. Give an evidence-based BUILD, TEST, MODIFY, or REJECT recommendation.

6. Open [PLUGIN_CREATOR_PROMPT.md](chatgpt-idea-validator-plugin/PLUGIN_CREATOR_PROMPT.md) and copy it into the GPT instructions.
7. Use [SKILL.md](chatgpt-idea-validator-plugin/SKILL.md) as the main behavioral instructions.
8. Upload these supporting folders if the GPT editor allows file uploads:
   - [references](chatgpt-idea-validator-plugin/references/)
   - [workflows](chatgpt-idea-validator-plugin/workflows/)
   - [templates](chatgpt-idea-validator-plugin/templates/)
9. Turn on web search if available.
10. Test the GPT in Preview before saving or sharing it.

Free, Go, Plus, and Pro personal accounts may not be able to create or publish new GPTs. In that case, use the conversation fallback below.

### Option 2: Plugin Creator

Use this option when **Plugin Creator** or the plugin tools are available in your ChatGPT workspace.

1. Open Plugin Creator or ChatGPT Plugins.
2. Start a new plugin project.
3. Copy [PLUGIN_CREATOR_PROMPT.md](chatgpt-idea-validator-plugin/PLUGIN_CREATOR_PROMPT.md) into the creator.
4. Attach or provide:
   - [SKILL.md](chatgpt-idea-validator-plugin/SKILL.md)
   - [references](chatgpt-idea-validator-plugin/references/)
   - [workflows](chatgpt-idea-validator-plugin/workflows/)
   - [templates](chatgpt-idea-validator-plugin/templates/)
5. Name the skill **idea-validator**.
6. Enable web search if the setup offers it.
7. Test the plugin in Preview.
8. Save, share, or publish it only after you confirm the setup.

Plugin setup and availability depend on the account and workspace. This package does not install or publish a plugin automatically.

### Option 3: Normal ChatGPT conversation

If neither a custom GPT nor Plugin Creator is available:

1. Open a normal ChatGPT chat.
2. Upload [SKILL.md](chatgpt-idea-validator-plugin/SKILL.md) and the supporting folders.
3. Ask ChatGPT to treat `SKILL.md` as instructions for this conversation.
4. Paste or upload the needed reference files as requested.
5. Ask for a short or deep evaluation.

You can also copy the contents of [PLUGIN_CREATOR_PROMPT.md](chatgpt-idea-validator-plugin/PLUGIN_CREATOR_PROMPT.md) into the first message.

## Test prompt

Use this prompt in Claude or ChatGPT:

> Use Idea Validator to deeply evaluate this idea: an appointment and reminder platform for independent dental clinics in India. Research customer demand, competitors, alternatives, pricing, distribution, technical feasibility, costs, and risks. Cite sources. Give me a BUILD / TEST / MODIFY / REJECT verdict and the cheapest experiment to validate willingness to pay.

## Simple workflow

1. Describe the idea and its target customer.
2. Add location, price, business model, and founder limits.
3. Add any real evidence you already have.
4. Ask for a quick or deep evaluation.
5. Review the verdict and the lowest-cost next experiment.

For user-supplied evidence, include sample size, participant selection, and raw results when possible.

## Important limits

- Web search can be unavailable or limited.
- The tool is not a team of separate agents.
- Market research does not prove product-market fit.
- Surveys and compliments do not prove willingness to pay.
- Real customers, payments, or signed commitments are stronger evidence.
- The final decision belongs to the user.

## Source folders

- [chatgpt-idea-validator-plugin/README.md](chatgpt-idea-validator-plugin/README.md) — original ChatGPT package notes.
- [chatgpt-idea-validator-plugin/PLUGIN_CREATOR_PROMPT.md](chatgpt-idea-validator-plugin/PLUGIN_CREATOR_PROMPT.md) — prompt for Plugin Creator.
