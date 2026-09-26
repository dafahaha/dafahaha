### Hi, I'm Daizhi Liao

Third-year undergraduate at Guangzhou University, Network Engineering. Research focus: reinforcement learning, embodied AI, and AI systems safety — combining empirical methods with shipping open-source tools.

Applying for PhD programs (Fall 2027) in Embodied AI / Reinforcement Learning / Robotics.

[Academic Homepage](https://dafahaha.github.io) | [CV](https://dafahaha.github.io/CV.pdf) | [ldz@e.gzhu.edu.cn](mailto:ldz@e.gzhu.edu.cn)

---

## Research

**Interests:**
- Reinforcement learning for embodied agents (off-policy algorithms, sample efficiency)
- Behavioral fingerprinting and empirical auditing of LLM API services
- Cross-platform RL deployment, model compression and quantization
- AI safety and adversarial robustness

**Featured Work**

**[TransitTruth](https://github.com/dafahaha/transit-truth)** — open-source auditing tool that verifies whether an AI API relay actually serves the advertised model, using statistical behavioral fingerprints (chi-square / KS tests, Bayesian updating). Includes a zero-install web demo and a **20-page technical report** validating same-family discrimination (gpt-4o vs gpt-4o-mini, TVD up to 0.90, 91.3% posterior identification). Complements single-token fingerprinting work by focusing on fine-grained same-family distinctions.
&nbsp;&nbsp;&nbsp;[Tech Report (PDF)](https://github.com/dafahaha/transit-truth/blob/main/docs/tech_report.pdf) · [Live Demo](https://dafahaha.github.io/transit-truth/)

**[rl-deploy-bench](https://github.com/dafahaha/rl-deploy-bench)** — cross-platform RL deployment and benchmarking toolkit. Export SB3 policies to ONNX/TorchScript, build TensorRT engines with FP16/INT8 quantization, and benchmark latency/throughput/accuracy across GPU and CPU from one config-driven CLI with auto-generated HTML reports.

---

## Open Source Contributions

**Merged**

| Project | PR | Contribution |
|---------|-----|-------------|
| [shmuma/ptan](https://github.com/shmuma/ptan/pull/57) | #57 | Fixed Gymnasium API compatibility in experience sources |
| [Algorineko/AgenticArXiv-RL](https://github.com/Algorineko/AgenticArXiv-RL/pull/72) | #72 | Added MIT License, CONTRIBUTING, issue templates, CI |
| [NVlabs/FluxVLA](https://github.com/NVlabs/FluxVLA/pull/122) | #122, #123 | Fixed typo and installation docs |

**In Review — Code Bug Fixes**

| Project | PR | Contribution |
|---------|-----|-------------|
| [microsoft/TextWorld](https://github.com/microsoft/TextWorld/pull/377) | #377 | Fixed `env.step` crash on multi-command input (non-greedy score parsing + tests) |
| [vllm-project/vllm](https://github.com/vllm-project/vllm/pull/57400) | #57400 | Fixed `system_fingerprint=null` emitted under fingerprint-mode=none |
| [pandas-dev/pandas](https://github.com/pandas-dev/pandas/pull/68968) | #68968 | Fixed `to_html` href escaping with render_links + escape |
| [google/brax](https://github.com/google/brax/pull/676) | #676 | Fixed EpisodeWrapper metrics accumulation with action_repeat |
| [Farama-Foundation/PettingZoo](https://github.com/Farama-Foundation/PettingZoo/pull/1465) | #1465 | Fixed agent selector reinit in tictactoe reset |
| [huggingface/datasets](https://github.com/huggingface/datasets/pull/8633) | #8633 | Accepted `pathlib.Path` in load/save_to_disk |
| [huggingface/diffusers](https://github.com/huggingface/diffusers/pull/14796) | #14796 | Fixed undefined attribute in TangentialClassifierFreeGuidance |
| [AI4Finance-Foundation/ElegantRL](https://github.com/AI4Finance-Foundation/ElegantRL/pull/488) | #488 | Fixed `argmax`→`max` in get_cumulative_rewards |
| [learnsyslab/gym-pybullet-drones](https://github.com/learnsyslab/gym-pybullet-drones/pull/319) | #319 | Replaced print statements with standard logging |
| [MichalBortkiewicz/JaxGCRL](https://github.com/MichalBortkiewicz/JaxGCRL/pull/65) | #65 | Fixed XML path resolution in arm manipulation envs |

Plus documentation work in [UoA-CARES/cares_reinforcement_learning](https://github.com/UoA-CARES/cares_reinforcement_learning/pull/409) #409 and community/CI setup across several smaller RL projects.

---

## Tech Stack

**RL / Robotics** — PyTorch · Stable-Baselines3 · Gymnasium · MuJoCo
**Deployment** — ONNX · ONNX Runtime · TensorRT · TorchScript · INT8/FP16
**Systems** — Python · C++ · Linux · Docker · Git · CI/CD · CUDA

---

![Daizhi's GitHub stats](https://github-readme-stats.vercel.app/api?username=dafahaha&show_icons=true&hide_border=true&count_private=true)
