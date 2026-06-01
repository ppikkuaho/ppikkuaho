# Pietari Pikkuaho

Applied-AI architect and engineer. Pietari designs and ships production LLM systems — agentic orchestration, multi-stage evaluation, and the platform plumbing underneath them — and the work runs, not just demos.

The repositories below are the proof. They span four areas on purpose: agentic infrastructure, ML systems, conventional backend/SWE, and graphics. Each one is real software that was built to solve a real problem and verified to work.

## Core work

- **[tori-watch](https://github.com/ppikkuaho/tori-watch)** — An LLM-powered marketplace-watch service: FastAPI on Cloud Run, a staged LLM evaluation pipeline, Postgres, and a Next.js front end. The fetcher reverse-engineers an undocumented pagination scheme to lift recall from ~7% to ~70%.
- **[media-ingest-pipeline](https://github.com/ppikkuaho/media-ingest-pipeline)** — An async media-ingestion and transcription pipeline: FastAPI plus Redis workers, SSRF-guarded fetchers, and a multi-LLM consensus evaluation harness that grades model output against a golden set.
- **[inter-agent-bus](https://github.com/ppikkuaho/inter-agent-bus)** — A lease-authenticated message broker for coordinating multiple local AI-agent sessions, with mirrored JS/Python clients and PTY adapters. It coordinates the agent sessions that build these projects.
- **[recursive-subagent-runtime](https://github.com/ppikkuaho/recursive-subagent-runtime)** — A recursive subagent supervisor for Claude Code and Codex: spawn, wait, observe, and cancel with depth caps, fcntl locking, and process-group isolation.
- **[unet-activation-visualizer](https://github.com/ppikkuaho/unet-activation-visualizer)** — An interactive 3D visualizer and PyTorch forward-hook pipeline for SDXL U-Net activations and cross-attention, with a causal intervention engine that edits activations and observes the effect on the output.
- **[mcp-servers](https://github.com/ppikkuaho/mcp-servers)** — A collection of Model Context Protocol servers (Outlook/Graph, async media transcription, Telegram, a Codex wrapper) for agent workflows.

## More

Agentic infrastructure: [mcp-llm-router](https://github.com/ppikkuaho/mcp-llm-router) · [agent-delegation-contract](https://github.com/ppikkuaho/agent-delegation-contract) · [cognitive-config](https://github.com/ppikkuaho/cognitive-config) · [claude-skills](https://github.com/ppikkuaho/claude-skills) · [llm-design-principles](https://github.com/ppikkuaho/llm-design-principles)

ML systems: [colbert-semantic-search](https://github.com/ppikkuaho/colbert-semantic-search) (ColBERT late-interaction retrieval, PLAID index, FastAPI query API)

Backend / SWE: [health-sync](https://github.com/ppikkuaho/health-sync) (HealthKit → CloudKit → DuckDB → Python, durable resumable sync) · [whispert](https://github.com/ppikkuaho/whispert) (serverless transcription on GCP, signed-URL uploads, adaptive ffmpeg chunking)

Graphics / systems: [autonomous-cuda-to-metal-port](https://github.com/ppikkuaho/autonomous-cuda-to-metal-port) (a long-horizon agentic harness driving a CUDA image-to-3D port to Apple Silicon, validated stage-by-stage against an H100 reference) · [reshade-vulkan-metal-port](https://github.com/ppikkuaho/reshade-vulkan-metal-port) (ReShade effects as a portable Vulkan compute pipeline running on Metal via MoltenVK)

Security research: [geo-block-redteam-study](https://github.com/ppikkuaho/geo-block-redteam-study) (a checkout-time geo-restriction safeguard — methodology, findings, and defensive lessons, target abstracted)
