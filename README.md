# Modelfiles

Ollama Modelfiles for a local multi-role agent team.

## Models

| File | Base model | Role |
|------|-----------|------|
| `Modelfile.deepseek-coder_autocomplete` | `deepseek-coder:1.3b` | Inline autocomplete — predict next tokens only |
| `Modelfile.qwen25-coder_autocomplete` | `qwen2.5-coder:1.5b` | Inline autocomplete (A/B vs deepseek-coder:1.3b) |
| `Modelfile.nemotron-32b-Afolabe` | `nemotron-mini-4b-instruct` | Architect — discovery, revision, final spec |
| `Modelfile.qwen-pro-Bob` | `qwen3:8b` | Builder (legacy) — superseded by qwen3-coder-30b-Bob |
| `Modelfile.qwen3-coder-30b-Bob` | `qwen3-coder:30b` | Builder — generates correct, minimal-diff code (CPU) |
| `Modelfile.qwen3-30b-Maria` | `qwen3-coder:30b` | Checker — strict spec/correctness reviewer |
| `Modelfile.qwen3-8b-Petra` | `qwen3:8b` | Planner — build order sequencer (GPU) |
| `Modelfile.qwen3-35b-Kwame` | `qwen3:35b` | Planner (A/B vs Petra, CPU) |
| `Modelfile.qwen3-30b-Tess` | `qwen3:30b` | Tester — generates pytest suites |
| `Modelfile.r1-logic-Deepak` | `deepseek-r1:32b` | Stress tester — logic gaps, edge cases, security |
| `Modelfile.r1-logic-Roja` | `deepseek-r1:32b` | Spec reviewer — gaps, contradictions, open questions |

## Usage

```sh
ollama create autocomplete    -f Modelfile.deepseek-coder_autocomplete
ollama create autocomplete-q  -f Modelfile.qwen25-coder_autocomplete
ollama create nemotron-32b-design   -f Modelfile.nemotron-32b-Afolabe
ollama create qwen3-coder-30b-builder -f Modelfile.qwen3-coder-30b-Bob
ollama create qwen3-30b-spec        -f Modelfile.qwen3-30b-Maria
ollama create qwen3-8b-plan         -f Modelfile.qwen3-8b-Petra
ollama create qwen35-35b-modulator  -f Modelfile.qwen3-35b-Kwame
ollama create qwen3-30b-test        -f Modelfile.qwen3-30b-Tess
ollama create r1-logic              -f Modelfile.r1-logic-Deepak
ollama create r1-32b-spec           -f Modelfile.r1-logic-Roja
```

## License

This is free and unencumbered software released into the public domain. See [UNLICENSE](UNLICENSE).
