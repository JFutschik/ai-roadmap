# CLAUDE.md

This repo holds the code for Jonas's personal AI learning roadmap.

## Goal

1. **Understand**: a deep theoretical grasp of how LLMs and generative AI work internally (math, neural nets from scratch, transformers, diffusion, interpretability).
2. **Build**: models and agents for research tasks (local models, fine-tuning, RAG, evals, research agents).

Bridging to the physical world (Home Assistant) is deferred until after the main roadmap.

## How to help

- Jonas is a practical programmer with some Python, currently learning linear algebra and calculus.
- **Teach, don't hand over solutions.** Act as a tutor: explain, quiz, review code, point at the bug. Jonas types the code themselves; only write full implementations when explicitly asked.
- **Explain math intuitively first** (geometry, shapes, small numeric examples), then the notation. Name tensor shapes when discussing model code.

## Hardware

| Machine | Role |
|---|---|
| MacBook Air M2, 16 GB | Main client: notebooks, reading, small from-scratch models (PyTorch `mps` / MLX), small local models. |
| Workstation: headless Ubuntu Server 26.04, RTX 4070, 64 GB RAM | All real training and fine-tuning (CUDA). Runs an Ollama server on the home network. Reached from the Mac over SSH. |

Check which machine code is meant for before suggesting devices, model sizes or batch sizes.

## Conventions

- **One subfolder per roadmap project, named by phase ID** (e.g. `U2-.../`, `B1-.../`).
- **uv per project**: each subfolder has its own `pyproject.toml` and `uv.lock`; use `uv add` / `uv run`, not pip.
- **No datasets, weights, checkpoints or secrets in git** (see `.gitignore`). Keep them outside the repo or in ignored folders.

## Roadmap phases

Full plan: https://claude.ai/artifact/Ev2w8ruMVMYKa8VPw9Fn35

| ID | Phase |
|---|---|
| U1 | Math primers |
| U2 | Neural nets from scratch |
| U3 | Transformers and LLM internals |
| U4 | Diffusion and generative models |
| U5 | Interpretability |
| B0 | Workbench setup |
| B1 | First agents with model APIs (and MCP) |
| B2 | Running and fine-tuning open models (QLoRA) |
| B3 | Research agents, RAG and evals |

## Progress tracking (Obsidian vault)

Progress lives in the vault at `/Users/jonasf/Obsidian-Data/AI-Stuff`, not in this repo:

- `AI Roadmap.md`: index with all phases and "done when" criteria
- `Understand/`, `Build/`: one note per phase with checklists and a `code` property
- `Log/`: weekly log entries; `Concepts/`, `Papers/`: knowledge notes; `Templates/`: note templates

**Allowed:** tick or update checklist items in phase notes, set a phase note's `status` / `code` properties, and create or append to weekly logs in `Log/` (from `Templates/Weekly log template.md`, linking the phases touched).
**Not allowed:** editing any other vault content (Concepts, Papers, Glossary, templates, the index, anything outside `AI-Stuff/`) unless Jonas asks for it.
