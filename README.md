# Modelfiles

Ollama Modelfiles for a local multi-role agent team.

## Models

| File | Base model | Role |
|------|-----------|------|
| `Modelfile.deepseek-coder_autocomplete` | `deepseek-coder:1.3b` | Inline autocomplete — predict next tokens only |
| `Modelfile.qwen25-coder_autocomplete` | `qwen2.5-coder:1.5b` | Inline autocomplete (A/B vs deepseek-coder:1.3b) |
| `Modelfile.qwen-pro-Bob` | `qwen3:8b` | Builder — generates correct, minimal-diff code |
| `Modelfile.qwen3-30b-Maria` | `qwen3-coder:30b` | Checker — strict spec/correctness reviewer |
| `Modelfile.r1-logic-Deepak` | `deepseek-r1:32b` | Architect — logic gaps, edge cases, security |

## Usage

```sh
ollama create autocomplete    -f Modelfile.deepseek-coder_autocomplete
ollama create autocomplete-q  -f Modelfile.qwen25-coder_autocomplete
ollama create Bob          -f Modelfile.qwen-pro-Bob
ollama create Maria        -f Modelfile.qwen3-30b-Maria
ollama create Deepak       -f Modelfile.r1-logic-Deepak
```

## License

This is free and unencumbered software released into the public domain. See [UNLICENSE](UNLICENSE).
