# RadianVector - Broad scope

RadianVector works on evaluating and improving how AI models run.

Our work spans language, image, audio, video, and multimodal models, with a focus on practical AI systems research and engineering across:

- **Inference** — performance, throughput, latency, quantization, speculative decoding, serving, and runtime configuration.
- **Agents** — agent execution, tool use, reliability, and evaluation.
- **Evaluations** — reproducible evaluation harnesses, behavioral testing, model reliability, and safety and reliability evaluations.
- **Benchmarks & experiments** — controlled experiments across models and inference stacks, with code and methodology published where possible.
- **Evaluation & research tools** — utilities, datasets, and infrastructure used in our experiments.

Repositories in this organization contain code accompanying RadianVector research, benchmarks, tutorials, and technical experiments.

Website: https://radianvector.com


## RadianVector - Current work 

We measure how AI models behave once they are quantized, served and put under load — and publish what we can share and what we think is useful to the community.

Most published inference numbers cannot be checked: the configuration is unstated, the scoring is opaque, runs are single, and nothing that failed appears. We build fixed instruments, score them by code, compare configurations question by question, and measure how much two identical runs disagree to give insights into reproducibility and randomness of runs. 

## Published work

Two benchmark studies, free to read, no registration:

- **[Beyond tokens per second](https://radianvector.com/benchmarks/qwen3-8-27b-rtx-4090)** — 71 controlled inference configurations on a single 24 GiB card: four 4-bit checkpoint builds, KV-cache precision, CUDA graphs, speculative decoding and concurrency from one user to thirty-two, with answer accuracy measured on every arm. Includes a 7.4% throughput gain we measured and then qualified, because on short answers it cost 6.5 accuracy points.
- **[Thinking on, measured](https://radianvector.com/benchmarks/qwen3-8-27b-thinking-rtx-4090)** — what a model's native reasoning mode is worth and where it stops paying, across four effort settings, four checkpoints and nine concurrency levels.

Method, instrument and open questions: **[radianvector.com/research](https://radianvector.com/research)**

Tutorials on model internals: **[radianvector.com/tutorials](https://radianvector.com/tutorials/)**

## What we have been working on recently

**Inference behaviour.** Throughput, latency, quantization, KV-cache precision, speculative decoding, serving and runtime configuration — measured with answer quality checked alongside speed, because a configuration that is faster and answers differently is not a free win.

**Evaluation harnesses.** Fixed, seeded, programmatically scored task suites with a measured repeatability floor and paired comparison built in. RV-380, the instrument behind both studies above, is 380 tasks across reasoning, long-context retrieval, instruction following and structured output.

**Reproducibility tooling.** Every published figure names the campaign it came from, and automated checks recompute each one from the raw results before a page ships.


## Roadmap

- Raw data behind the published studies
- Extending the harness to agent and tool-use evaluation
- Wider platform (SGLang, TensorRT-LLM, etc) and runtime coverage

## Repositories

This organization will hold the code, instruments and data behind RadianVector's published research. It is new — the first repositories are being prepared.

---

[radianvector.com](https://radianvector.com) · [hello@radianvector.com](mailto:hello@radianvector.com) · Silicon Valley, California, USA
