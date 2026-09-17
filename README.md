### Hi, I'm Daizhi Liao 👋

I'm a third-year undergraduate at **Guangzhou University**, majoring in Network Engineering with a focus on AI systems. My research sits at the intersection of **reinforcement learning**, **embodied AI**, and **efficient model deployment** — closing the gap between RL research and real-world robot and edge hardware.

I'm applying for **PhD programs (Fall 2027)** in Embodied AI / Reinforcement Learning / Robotics.

🔗 **[Academic Homepage](https://dafahaha.github.io)** &nbsp;|&nbsp; 📄 **[CV](https://dafahaha.github.io/CV.pdf)** &nbsp;|&nbsp; 📧 [ldz@e.gzhu.edu.cn](mailto:ldz@e.gzhu.edu.cn)

---

## 🔬 Research

**Research Interests:**
- Reinforcement learning for embodied agents (off-policy algorithms, sample efficiency)
- Cross-platform RL model deployment (GPU / Jetson / CPU)
- Model compression and quantization for RL policies (INT8 / FP16)
- AI safety and adversarial robustness

**Featured Project — [rl-deploy-bench](https://github.com/dafahaha/rl-deploy-bench)**

A cross-platform RL model deployment and performance benchmarking toolkit. Export Stable-Baselines3 policies to ONNX/TorchScript, build TensorRT engines with FP16/INT8 quantization, and benchmark latency, throughput, and accuracy across x86 GPU, NVIDIA Jetson, and CPU — all from one config-driven CLI with auto-generated HTML reports.

*Research value:* Provides a reproducible benchmark for studying the accuracy-latency tradeoff of RL policy quantization across hardware platforms.

---

## 🤝 Open Source Contributions

| Project | PR | Contribution | Status |
|---------|-----|-------------|--------|
| [scikit-learn/scikit-learn](https://github.com/scikit-learn/scikit-learn/pull/34981) | #34981 | Fixed `compute_class_weight` coercing string labels (e.g. `"1"`) to int, breaking dict lookup for string class weights | Open |
| [vllm-project/vllm](https://github.com/vllm-project/vllm/pull/57400) | #57400 | Fixed `system_fingerprint: null` emitted in non-streaming responses when `--fingerprint-mode=none`; added `exclude_none=True` to model_dump | Open |
| [Farama-Foundation/Gymnasium](https://github.com/Farama-Foundation/Gymnasium/pull/1719) | #1719 | Fixed `mj_forward` not called after `mj_step`, causing inconsistent body xpos/qpos in observations (e.g. Reacher-v5) | Open |
| [huggingface/trl](https://github.com/huggingface/trl/pull/7264) | #7264 | Fixed `entropy_from_logits` returning NaN for zero-probability tokens (`0 * -inf = NaN`); replaced -inf logps with 0 before multiplication | Open |
| [UoA-CARES/cares_reinforcement_learning](https://github.com/UoA-CARES/cares_reinforcement_learning/pull/409) | #409 | Algorithm docs (DQN, PPO, overview) rewritten against actual codebase API; 44-algorithm index | Under review |
| [OWASP/secure-agent-playbook](https://github.com/OWASP/secure-agent-playbook/pull/28) | #28 | Fixed outdated OWASP LLM Top 10 IDs across 5 files | Open |
| [redai-studio/Relax](https://github.com/redai-studio/Relax/pull/294) | #294 | Docker-free installation guide (bilingual EN/ZH) | Open |

---

## 🛠 Tech Stack

**RL and Learning** — PyTorch · Stable-Baselines3 · Gymnasium · MuJoCo
**Deployment** — ONNX · ONNX Runtime · TensorRT · TorchScript · INT8/FP16 quantization
**Edge and Robotics** — NVIDIA Jetson (Xavier/Orin) · ROS · CUDA · cuDNN
**Systems** — Python · C++ · Linux · Docker · Git · CI/CD

---

![Daizhi's GitHub stats](https://github-readme-stats.vercel.app/api?username=dafahaha&show_icons=true&hide_border=true&count_private=true)
