<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&amp;color=0:1E3A8A,50:2563EB,100:06B6D4&amp;height=180&amp;section=header&amp;text=zyaochen&amp;fontSize=52&amp;fontColor=ffffff&amp;animation=fadeIn&amp;fontAlignY=38" width="100%" />

<p>我是一名 SRE，日常做线上稳定性。这里的仓库主要用来从零学大模型、按章拆 LLM 推理引擎和 GPU 优化，配套代码在 CPU 上就能跑；另有一个管理 agent 上下文的画布工具 Weft。</p>

<a href="https://github.com/zyaochen">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=20&duration=2800&pause=900&color=2563EB&center=true&vCenter=true&width=760&lines=SRE+%C2%B7+Reliability+%C2%B7+Disaster+Recovery+Drills;Learning+LLMs+from+zero%3A+math%2C+training%2C+serving%2C+RAG+and+agents;Reading+LLM+inference+engines+from+scratch%3A+vLLM+%C2%B7+SGLang+%C2%B7+llama.cpp;Building+Weft%3A+see%2C+cut+and+rewire+what+the+next+agent+turn+reads" alt="SRE, reliability, learning LLMs from zero, LLM inference engines and agent tooling" />
</a>

<p>
  <a href="https://zyaochen.github.io/weft/"><img src="https://img.shields.io/badge/Weft-Live_demo-2563EB?style=for-the-badge&labelColor=1F2937" alt="Weft live demo" /></a>
  <a href="https://colab.research.google.com/github/zyaochen/zero-to-vllm/blob/main/colab/02-ledger.ipynb"><img src="https://img.shields.io/badge/zero--to--vllm-Open_in_Colab-F9AB00?style=for-the-badge&logo=googlecolab&logoColor=white&labelColor=1F2937" alt="Open zero-to-vllm in Colab" /></a>
</p>

</div>

## 🪄 About me

```text
陈子瑶 · SRE · Beijing

SRE working on reliability day to day; reading LLM inference engines from scratch
and building agent tooling on the side.
```

## ✨ 现在在做的

- **[zero-to-llm](https://github.com/zyaochen/zero-to-llm)：从零掌握大模型**。31 篇从矩阵乘法讲到推理服务、RAG、Agent 和工程交付，每个技术决策都落到效果、显存、时延、成本四笔账上。正文里 81 段代码都抽了出来，`tools/verify.py` 逐字核对正文贴出的输出。
- **四套「从 0 开始」配套代码**：按章拆 vLLM、SGLang、llama.cpp 和 GPU 优化。每章带一个能在 CPU 上跑的模拟器或实验脚本，配单元测试和一个 Colab notebook；`book/` 里是全文的 Markdown 版。
- **[Weft](https://github.com/zyaochen/weft)**：无限画布上的对话，节点之间的连线就是下一轮的上下文。长时间的 agent 分析跑偏时，用它看清并剪掉 agent 正在读的过时上下文。
- **让 agent 接手重复的稳定性分析**：取数、对账、写复盘初稿做成 agent 能调用的工具，人只做判断。Weft 就是在这件事里做出来的。

## 🧭 日常工作

- **全球高可用机房架构探索**：探索全球多机房的高可用架构，架构优化、风险识别、演练攻防、混沌工程。
- **数据面高可用**：评估数据库、缓存和 KV 存储的冗余度与故障域分布，建设自动化运维。
- **可靠性度量**：以容灾标准为基线，度量现网的达成情况，识别差距，驱动改进。

更早几年做 DevOps：Docker、Kubernetes、Go、Nginx。下面「不再维护」里的仓库都是那时写的。

## 🧭 关注方向

**稳定性** · 容灾演练 · 多活与副本治理 · 故障复盘 · 稳定性数据口径

**LLM 基础** · 数学与模型结构 · 预训练与对齐 · RAG 与 Agent 评测

**LLM 推理** · vLLM · SGLang · llama.cpp · KV 缓存与调度 · PD 分离 · Embedding / Rerank 服务

**GPU 与集群** · CUDA · NCCL · RDMA · K8s 调度 · 节点烤机

**agent 工具** · 上下文工程 · Claude Code / Codex 工作流

## 📦 现在在维护的仓库

| 仓库 | 它做什么 | 在哪能跑 |
|---|---|---|
| [**zero-to-llm**](https://github.com/zyaochen/zero-to-llm) | 从零掌握大模型，共 31 篇：数学 → 模型结构 → 预训练 → 后训练与对齐 → 推理服务 → RAG 与 Agent → 工程交付；`book/` 是全文，各章目录放正文里的可运行代码和期望输出 | 只要 CPU；9 篇要 torch（CPU 版），其余只要 NumPy 或标准库；输出在 Python 3.11 上生成 |
| [**zero-to-vllm**](https://github.com/zyaochen/zero-to-vllm) | 按章拆 vLLM v0.32.0，共 26 章：显存账本、调度与抢占、Paged KV、prefix caching、PD 分离、LoRA、部署实战、Embedding 与 Rerank 服务 | `sim_*.py` 在 CPU 上跑（Python ≥ 3.11）；`gpu_*.py` 和起服脚本要 GPU |
| [**zero-to-sglang**](https://github.com/zyaochen/zero-to-sglang) | 按章拆 SGLang v0.5.22，书稿 25 章、配套代码 24 个目录：内存池、RadixAttention、overlap 与 CUDA Graph、HiCache、PD 分离、Embedding 与 Rerank 服务 | CPU 练习需要 Python ≥ 3.10 + numpy |
| [**zero-to-llama**](https://github.com/zyaochen/zero-to-llama) | 按章拆 llama.cpp，共 22 章：GGUF/GGML 结构、内存与带宽预测器、量化对照、CPU 调优、投机解码；数字来自一台 4 vCPU / 8 GB、没有 GPU 的机器 | Python ≥ 3.9 标准库，不装 `gguf` 包也能读 GGUF |
| [**zero-to-gpu**](https://github.com/zyaochen/zero-to-gpu) | 按章拆 GPU 优化（CUDA 13.4），书稿 33 章、配套代码 24 个目录：性能账本、访存与 GEMM、Tensor Core、NVLink / PCIe / RDMA、NCCL、K8s 调度、可靠性、MoE 专家并行 | `sim_*.py` 在 CPU 上跑（Python ≥ 3.10 + numpy）；`*.cu` 和 `gpu_*.py` 要 GPU |
| [**Weft**](https://github.com/zyaochen/weft) | 每次问答是画布上的一个节点，剪断一根连线，下一轮就读不到那段历史；可以接 Claude Code / Codex 这类终端 agent。[ThoughtDAG](https://github.com/chenxiachan/thoughtdag) 的 fork（MIT） | Node.js ≥ 20，本地 Web 应用加一个小代理；也有[在线演示](https://zyaochen.github.io/weft/) |

## ⚡ 30 秒试一下

不需要 GPU，算一张 H100 上跑 Qwen3-8B 时 vLLM 能分到多少 KV 缓存：

```bash
git clone https://github.com/zyaochen/zero-to-vllm.git
cd zero-to-vllm/02-ledger
python3 sim_ledger.py --model qwen3-8b --gpu h100-sxm
```

期望输出的开头：

```text
Qwen3-8B on 1 x H100 SXM  weight=bf16 kv=bf16 util=0.92
  requested          72.86 GiB  (总显存 x util)
  - 权重             15.26 GiB
  ...
  = KV 可用          55.43 GiB  ← 对照日志 Available KV cache memory
```

不想在本地装环境，可以点上面的 Colab 徽章，在浏览器里跑同一章的单元测试和 CPU 命令。

从零学大模型，先算四个代表模型每个词元要占多少 KV 缓存（只用标准库）：

```bash
git clone https://github.com/zyaochen/zero-to-llm.git && cd zero-to-llm
python3 01-matmul/ex07.py
python3 tools/verify.py 01   # 第 01 篇全部 7 段，和正文输出逐字核对；需要 NumPy
```

期望输出的开头：

```text
Qwen3-32B     262144 B/token =  256.0 KiB/token
Qwen3.8-27B    65536 B/token =   64.0 KiB/token
DeepSeek-V3    70272 B/token =   68.6 KiB/token
Kimi K3        27648 B/token =   27.0 KiB/token
...
```

想直接用 Weft，装 npm 包就行：

```bash
npm install -g weft-canvas
weft serve       # 在 http://localhost:3001 提供画布并打开浏览器
```

或者从源码跑：

```bash
git clone https://github.com/zyaochen/weft.git && cd weft
npm install
npm run server   # 终端 1：模型代理，http://localhost:3001
npm run dev      # 终端 2：画布，http://localhost:5173
```

## ⚠️ 使用前要知道的

- **zero-to-\* 是学习用的配套代码，不是库**。模拟器复现的是引擎主干里的关键账本，结果要和真实日志对账才算数。四个引擎和 GPU 仓库的 README 写了版本基线（具体到 commit），zero-to-llm 写了模型规格的核对日期和运行环境；换了版本，数字可能对不上。
- **zero-to-llm 后半部分的案例读数是假设读数**。准确率、时延、成本这些案例数字是示意用的，不是实测；能复算的是代码输出和公式推导，正文里都标明了。这个仓库没有 Colab notebook。
- **Colab notebook 只放 CPU 能跑的命令**。要 GPU、模型文件或运行中服务的命令没有放进去，要自己找机器跑。
- **Weft 的画布数据存在浏览器 IndexedDB 里**，没有同步也没有账号，用「导出备份（.json）」备份；桌面安装包未签名。限制和排障见它的 [README](https://github.com/zyaochen/weft#limitations)。
- **2015–2020 的仓库不再维护**：
  - [ngx_stream_upstream_check_module](https://github.com/zyaochen/ngx_stream_upstream_check_module)：Nginx stream 模块的 TCP 健康检查；
  - [onssh](https://github.com/zyaochen/onssh)：基于 SSH 的 Web 终端，Python 2.7 + Tornado；
  - [nginx-devops](https://github.com/zyaochen/nginx-devops)；
  - [旧博客](https://github.com/zyaochen/zyaochen.github.io/tree/archive/hexo-blog-2017)：运维 / Docker / Go 方向的存档，已下线，源文件留在这个分支；[zyaochen.github.io](https://zyaochen.github.io/) 现在是项目主页。

## 📮 联系

对哪个仓库有问题，直接在那个仓库开 issue。
