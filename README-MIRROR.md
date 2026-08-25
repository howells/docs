# openrouter-docs — local mirror

**This is the source of truth for OpenRouter API behaviour. Verify against these
files before writing or reviewing any OpenRouter code. Never guess.**

Same pattern as `~/Sites/mastra-docs`, `~/Sites/exa-docs`, `~/Sites/firecrawl-docs`.

## What this is

A **partial, sparse** clone of `github.com/OpenRouterTeam/docs` — the repo that
renders <https://openrouter.ai/docs>.

- Cloned: **2026-08-05**, upstream `00a9a0f` (`2026-08-04`)
- `git clone --depth 1 --filter=blob:none --sparse`, excluding `/images`,
  `/public`, `/assets`. 18 MB.
- A single-file export is also available at
  <https://openrouter.ai/docs/llms-full.txt> (3.6 MB) if you want grep-only.

## Where the answers live

| Question | File |
|---|---|
| Machine-readable request/response schema | `openapi/` |
| Endpoint reference (chat completions, params) | `api_reference/` |
| Provider routing, fallbacks, `provider` block | `guides/` (search `provider-routing`) |
| Structured outputs / `response_format` | search `structured-output` under `guides/` |
| Prompt caching per upstream provider | search `prompt-caching` |
| Attribution headers (`HTTP-Referer`, `X-Title`) | `app-attribution.mdx` |
| Client SDKs | `client-sdks/`, `agent-sdk/` |

## Refresh

```bash
cd ~/Sites/openrouter-docs && git fetch --depth 1 origin main && git reset --hard origin/main
```
