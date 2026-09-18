### Hi, I'm Daizhi Liao

Third-year undergraduate at Guangzhou University, Network Engineering. Research focus: reinforcement learning, embodied AI, and efficient model deployment — bridging RL research and real-world edge hardware.

Applying for PhD programs (Fall 2027) in Embodied AI / Reinforcement Learning / Robotics.

[Academic Homepage](https://dafahaha.github.io) | [CV](https://dafahaha.github.io/CV.pdf) | [ldz@e.gzhu.edu.cn](mailto:ldz@e.gzhu.edu.cn)

---

## Research

**Interests:**
- Reinforcement learning for embodied agents (off-policy algorithms, sample efficiency)
- Cross-platform RL model deployment (GPU / Jetson / CPU)
- Model compression and quantization for RL policies (INT8 / FP16)
- AI safety and adversarial robustness

**Featured Project — [rl-deploy-bench](https://github.com/dafahaha/rl-deploy-bench)**

Cross-platform RL model deployment and benchmarking toolkit. Export SB3 policies to ONNX/TorchScript, build TensorRT engines with FP16/INT8 quantization, and benchmark latency/throughput/accuracy across x86 GPU, Jetson, and CPU — from one config-driven CLI with auto-generated HTML reports.

---

## Open Source Contributions

**Merged**

| Project | PR | Contribution |
|---------|-----|-------------|
| [shmuma/ptan](https://github.com/shmuma/ptan/pull/57) | #57 | Fixed Gymnasium API compatibility in experience sources |
| [Algorineko/AgenticArXiv-RL](https://github.com/Algorineko/AgenticArXiv-RL/pull/72) | #72 | Added MIT License, CONTRIBUTING, issue templates, CI |
| [NVlabs/FluxVLA](https://github.com/NVlabs/FluxVLA/pull/122) | #122, #123 | Fixed typos and installation docs |

**In Review — Code Bug Fixes**

| Project | PR | Contribution |
|---------|-----|-------------|
| [scikit-learn/scikit-learn](https://github.com/scikit-learn/scikit-learn/pull/34986) | #34986 | Removed `int(c)` coercion in `compute_class_weight` that broke dict lookup for string labels parsing as int (Fixes #34883) |
| [DLR-RM/stable-baselines3](https://github.com/DLR-RM/stable-baselines3/pull/2289) | #2289 | Fixed `DummyVecEnv`/`SubprocVecEnv` ignoring reset options/seeds on auto-reset |
| [microsoft/TextWorld](https://github.com/microsoft/TextWorld/pull/377) | #377 | Fixed `env.step` crash on multi-command input causing `int()` parse failure |
| [google/brax](https://github.com/google/brax/pull/676) | #676 | Fixed EpisodeWrapper metrics accumulation with action_repeat |
| [huggingface/datasets](https://github.com/huggingface/datasets/pull/8633) | #8633 | Fixed `pathlib.Path` regression in dataset loading |
| [huggingface/diffusers](https://github.com/huggingface/diffusers/pull/14796) | #14796 | Code improvement |

**In Review — Docs / Other**

| Project | PR | Contribution |
|---------|-----|-------------|
| [UoA-CARES/cares_reinforcement_learning](https://github.com/UoA-CARES/cares_reinforcement_learning/pull/409) | #409 | Algorithm docs rewritten against actual codebase API |
| [OWASP/secure-agent-playbook](https://github.com/OWASP/secure-agent-playbook/pull/28) | #28 | Fixed outdated OWASP LLM Top 10 IDs |

---

## Tech Stack

**RL** — PyTorch · Stable-Baselines3 · Gymnasium · MuJoCo
**Deployment** — ONNX · ONNX Runtime · TensorRT · TorchScript · INT8/FP16
**Edge/Robotics** — NVIDIA Jetson · ROS · CUDA · cuDNN
**Systems** — Python · C++ · Linux · Docker · Git · CI/CD

---

![Daizhi's GitHub stats](https://github-readme-stats.vercel.app/api?username=dafahaha&show_icons=true&hide_border=true&count_private=true)
