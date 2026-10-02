# Privacy Policy: Prompt Optimizer plugin for ChatGPT and Codex

Last updated: October 2, 2026

This policy covers the Prompt Optimizer plugin for ChatGPT and Codex
("the plugin"). The Prompt Optimizer Chrome extension is a separate product
with its own privacy policy:
<https://docs.google.com/document/d/1UrS7xCtq-Z2oN80qOxoppPsGDvJIVGfKVizeosbY3G8/edit?usp=sharing>

## Short version

The plugin does not collect, store, sell or share personal data. It has no
accounts. It never receives your draft.

## How it works

- **Your drafts.** The rewrite is done by your own AI assistant, inside your
  conversation, by following fixed instructions that the plugin supplies. The
  plugin does not read, receive, store or forward your draft or the rewritten
  prompt.
- **The endpoint.** The version in OpenAI's Plugins Directory declares one
  read-only tool, `get_prompt_optimization_guide`. It takes no input and
  returns the same fixed rewrite rules every time. It is served by a static
  endpoint
  that has no database, no storage and makes no outbound requests. It receives
  only the standard protocol messages that ChatGPT or Codex send to any tool
  server (for example "list your tools"). Logging and analytics are turned off
  for the endpoint.
- **Hosting.** The endpoint runs on Cloudflare Workers. As with any hosting
  provider, Cloudflare processes technical request data, such as the IP address
  of the connecting service, to deliver the response. We do not receive or keep
  that data.
- **Codex marketplace copy.** The plugin you install from this repository with
  `codex plugin marketplace add` is skills-only: no tool, no server and no
  network requests.
- **The note.** The first rewrite in a conversation ends with one short note
  and a link to the Prompt Optimizer Chrome extension. The link carries
  `utm_source=chatgpt_plugin` so the Chrome Web Store can count visits in
  aggregate. Nothing is sent unless you open the link, and then the Chrome Web
  Store and Google handle the visit under their own policies.
- **Your assistant.** OpenAI processes your conversation in ChatGPT or Codex
  under its own terms and privacy policy. This plugin does not change that.

## Children

The plugin is not directed at children and collects no data from anyone.

## Changes

If this policy changes, the new version is published here with a new date.

## Contact

Questions: <https://github.com/bitcompool/prompt-optimizer-codex-plugin/issues>
