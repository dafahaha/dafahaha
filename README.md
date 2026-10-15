### Hi, I'm Daizhi Liao

Third-year undergraduate in Network Engineering at Guangzhou University. I build tools that audit deployed AI systems, run preregistered empirical studies in RL, and contribute a small number of fixes upstream in depth — rather than scattering patches across many repos.

Applying for PhD programs (Fall 2027) in Embodied AI / Reinforcement Learning / Robotics.

[Academic Homepage](https://dafahaha.github.io) | [Blog](https://dafahaha.github.io/blog/) | [CV](https://dafahaha.github.io/CV.pdf) | [ldz@e.gzhu.edu.cn](mailto:ldz@e.gzhu.edu.cn)

---

## Featured Work

**[TransitTruth](https://github.com/dafahaha/transit-truth)** — open-source auditing tool that verifies whether an AI API relay actually serves the advertised model, using statistical behavioral fingerprints (chi-square / KS tests, Bayesian updating). Includes a zero-install web demo and an extended technical report validating same-family discrimination (gpt-4o vs gpt-4o-mini, TVD up to 0.90, 91.3% in-distribution resubstitution posterior — self-consistency on the baseline's own reference, not held-out accuracy). Complements single-token fingerprinting work by focusing on fine-grained same-family distinctions.
&nbsp;&nbsp;&nbsp;[Tech Report (PDF)](https://github.com/dafahaha/transit-truth/blob/main/docs/tech_report.pdf) · [Live Demo](https://dafahaha.github.io/transit-truth/)

**[wm-audit](https://github.com/dafahaha/wm-audit)** — preregistered single-machine CPU audit suite that disentangles world-model *perceptual fidelity* (next-frame MSE / SSIM / NLL, plus fixed-filter stand-ins for LPIPS / rollout FVD — deterministic random-conv filter banks, not learned VGG/AlexNet backbones) from *control utility* (whether a planner can actually solve the task). A reduced pilot on one env (pixel_nav, 3 seeds × 3 capacities, 12k steps) found: pixel fidelity weakly predicts closed-loop return (H1 supported, |ρ|=0.32<0.4); control-relevant diagnostics did not (H2 not supported, ρ=0.26<0.6); INT8 compression did not degrade calibration faster than raw pixel fidelity (H3 not supported, n_pairs=9). This is a CPU reduced pilot, not the locked 200k-step × 5-seed × 2-env main run.

**[embodied-offpolicy-study](https://github.com/dafahaha/embodied-offpolicy-study)** — a Soft Actor-Critic implementation written from scratch in PyTorch (no Stable-Baselines3), run as a preregistered three-arm controlled study on Hopper-v4 (CPU, 120k env steps, 3 seeds/arm): Baseline (reward scale 1.0) vs RewardScaled (0.1) vs FixedAlpha (α fixed at 0.2). Welch p: Baseline–FixedAlpha 0.59, Baseline–RewardScaled 0.95; ANOVA F=0.22, p=0.81 — no statistically distinguishable effect detected (n=3). At 60k the reward-scaled arm looked ~3× better; extending to the preregistered 120k budget and adding the fixed-temperature control arm overturned that apparent gain as early seed noise.

**[rl-deploy-bench](https://github.com/dafahaha/rl-deploy-bench)** — cross-platform RL deployment and benchmarking toolkit. Export SB3 policies to ONNX/TorchScript, build TensorRT engines with FP16/INT8 quantization, and benchmark latency/throughput/accuracy across GPU and CPU from one config-driven CLI with auto-generated HTML reports. Jetson/edge is a target deployment path, not yet measured on device.

---

## Open Source Contributions

**Merged**

| Project | PR | Contribution |
|---------|-----|-------------|
| [microsoft/TextWorld](https://github.com/microsoft/TextWorld/pull/377) | #377 | Fixed `env.step` crash on multi-command input (non-greedy score parsing + unit tests) |
| [shmuma/ptan](https://github.com/shmuma/ptan/pull/57) | #57 | Fixed Gymnasium API compatibility in experience sources |
| [learnsyslab/gym-pybullet-drones](https://github.com/learnsyslab/gym-pybullet-drones/pull/319) | #319 | Replaced print() error statements with module logging; converted exit() calls to raised exceptions |
| [Eclectic-Sheep/sheeprl](https://github.com/Eclectic-Sheep/sheeprl/pull/340) | #340 | Added CONTRIBUTING guide and Code of Conduct |

**Under review (not yet merged) — selected code PRs in upstream RL/ML infrastructure**

| Project | PR | Contribution |
|---------|-----|-------------|
| [thu-ml/tianshou](https://github.com/thu-ml/tianshou/pull/1315) | #1315 | Fixed pickled policy restore under PyTorch 2.6 `weights_only` default |
| [ContinualAI/avalanche](https://github.com/ContinualAI/avalanche/pull/1701) | #1701 | Fixed MASPlugin raising on zero loss (falsy check) |
| [uoe-agents/epymarl](https://github.com/uoe-agents/epymarl/pull/92) | #92 | Fixed registration of multi-digit versioned PettingZoo envs |
| [vllm-project/vllm](https://github.com/vllm-project/vllm/pull/57400) | #57400 | Fixed `system_fingerprint=null` emitted under fingerprint-mode=none |
| [huggingface/datasets](https://github.com/huggingface/datasets/pull/8633) | #8633 | Accepted `pathlib.Path` in load/save_to_disk |
| [huggingface/diffusers](https://github.com/huggingface/diffusers/pull/14796) | #14796 | Fixed undefined attribute in TangentialClassifierFreeGuidance |
| [google/brax](https://github.com/google/brax/pull/676) | #676 | Fixed EpisodeWrapper metrics accumulation with action_repeat |
| [AI4Finance-Foundation/ElegantRL](https://github.com/AI4Finance-Foundation/ElegantRL/pull/488) | #488 | Fixed `argmax`→`max` in get_cumulative_rewards |
| [Farama-Foundation/PettingZoo](https://github.com/Farama-Foundation/PettingZoo/pull/1465) | #1465 | Fixed agent selector reinit in tictactoe reset |
| [MichalBortkiewicz/JaxGCRL](https://github.com/MichalBortkiewicz/JaxGCRL/pull/65) | #65 | Fixed XML path resolution in arm manipulation envs |
| [pandas-dev/pandas](https://github.com/pandas-dev/pandas/pull/68968) | #68968 | Fixed `to_html` href escaping with render_links + escape |

Smaller docs / community-health PRs (LICENSE, CONTRIBUTING, Code of Conduct, CI setup) across a number of smaller RL/ML projects, plus a typo fix in FluxVLA.

---

## Writing

- [Fixing a bug in Microsoft TextWorld — one line of regex and the multi-command parsing behind it](https://dafahaha.github.io/blog/textworld-bug-fix.html): root-cause writeup of merged PR #377. A greedy regex with DOTALL stitched two state blocks into one when a single line carried multiple commands.
- [CI passed green but the package wouldn't import: numpy and scipy missing from requirements](https://dafahaha.github.io/blog/ci-missing-deps.html): postmortem on a dependency-declaration bug found while running the TransitTruth audit pipeline — tests on a dirty machine passing says nothing about a clean install.

---

## Tech Stack

**RL / Robotics** — PyTorch · Stable-Baselines3 · Gymnasium · MuJoCo
**Deployment** — ONNX · ONNX Runtime · TensorRT · TorchScript · INT8/FP16
**Systems** — Python · C++ · Linux · Docker · Git · CI/CD · CUDA

---

![Daizhi's GitHub stats](https://github-readme-stats.vercel.app/api?username=dafahaha&show_icons=true&hide_border=true&count_private=true)
