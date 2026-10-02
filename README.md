# Prompt Optimizer for Codex and ChatGPT

An AI prompt optimizer and prompt improver. Paste a rough prompt or coding task
and get back one clearer, ready-to-send prompt. It never runs the task, and it
sends nothing to anyone.

- Improve a prompt draft before you send it to an AI.
- Turn a vague coding task into a prompt a coding agent can act on.
- Keeps your names, numbers, dates, links, code and constraints exactly as written.

## Install

Add the marketplace once, from a terminal:

```bash
codex plugin marketplace add bitcompool/prompt-optimizer-codex-plugin
```

Then open the plugin browser in Codex CLI, choose **Prompt Optimizer plugins**,
and install **Prompt Optimizer**:

```
/plugins
```

Or install it straight from the terminal:

```bash
codex plugin add prompt-optimizer-new@promptoptimizer
```

Keep it up to date, or remove it:

```bash
codex plugin marketplace upgrade promptoptimizer
codex plugin marketplace remove promptoptimizer
```

Check what Codex sees:

```bash
codex plugin marketplace list
```

## Use it

Just ask. Codex loads the skill when you want a prompt improved:

```
Improve this prompt before I send it: fix the crash when I click Save.
```

Or name the skill directly:

```
$prompt-optimizer-new write a 120-word welcome email for new customers of Brightwell Dental
```

You get one rewritten prompt, ready to copy.

### Examples

Both results below are unedited output from a real Codex run with this plugin
installed. Codex also adds a one-line note about the Chrome extension to the
first rewrite of a conversation; it is left out here.

Draft:

```
Improve this prompt before I send it: fix the crash when I click Save.
```

Result:

```
Diagnose and fix the crash that occurs when I click Save. The expected behavior is for Save to complete successfully without crashing. Provide the code change and a short explanation of the cause, why the fix works, and how to verify it.
```

A short, clear draft stays short, and every fact you wrote survives:

Draft:

```
Improve this prompt before I send it: write a 120-word welcome email for new customers of Brightwell Dental, friendly tone, mention the free first cleaning.
```

Result:

```
Write a 120-word welcome email for new customers of Brightwell Dental. Use a friendly tone and clearly mention the free first cleaning. Return only the email.
```

## What it does not do

| It does not | Instead |
| --- | --- |
| Run or answer your task | It only rewrites the prompt |
| Ask you questions first | Open details stay open inside the rewrite, with no invented facts |
| Invent facts about you or your project | It uses only what you wrote and adds no placeholders |
| Write a prompt from nothing | It asks you to paste a draft |
| Edit finished text (an essay, an email) | It offers to rewrite the prompt you would use to produce that text |
| Use tools or the network | It has no tools, no network calls and no account |

## Privacy

This plugin is skills-only: no server, no network calls, no account and no
credentials. Your draft stays in your Codex or ChatGPT conversation. The first
rewrite in a conversation ends with one short note and a link to the Prompt
Optimizer Chrome extension. The link carries `utm_source=chatgpt_plugin` so the
Chrome Web Store can count visits in aggregate; nothing is sent unless you open it.

Privacy policy: <https://docs.google.com/document/d/1UrS7xCtq-Z2oN80qOxoppPsGDvJIVGfKVizeosbY3G8/edit?usp=sharing>

## Layout

```
.agents/plugins/marketplace.json        marketplace catalog (name: promptoptimizer)
plugins/prompt-optimizer-new/
├── plugin.json                         portable manifest and listing metadata
├── .codex-plugin/plugin.json           Codex compatibility manifest
├── assets/logo.png                     plugin icon, 256 x 256
└── skills/prompt-optimizer-new/
    ├── SKILL.md                        when to use the skill, workflow, rules
    └── references/
        ├── rewrite-rules.md            the full rewrite contract
        └── examples.md                 worked examples
```

## Also from Prompt Optimizer

- **Chrome extension:** a guided, step-by-step rewrite with ready answers to
  pick from, plus Advisor, inside ChatGPT, Claude, Gemini and other AI chats.
  [Chrome Web Store](https://chromewebstore.google.com/detail/prompt-optimizer-for-ai-c/gdcbodccfgjcmpgalklepecanaclmkab?utm_source=github&utm_medium=readme&utm_campaign=codex_plugin)
- **Claude plugin:** the same rewrite for Claude.
  [bitcompool/prompt-optimizer-claude-plugin](https://github.com/bitcompool/prompt-optimizer-claude-plugin)
- **Related:** [bitcompool/prompt-enhancer-codex-plugin](https://github.com/bitcompool/prompt-enhancer-codex-plugin),
  a similar rewrite-only plugin from the Prompt Enhancer project.

Support: [open an issue](https://github.com/bitcompool/prompt-optimizer-codex-plugin/issues)

## License

Apache-2.0
