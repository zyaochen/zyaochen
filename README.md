<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&amp;color=0:1E3A8A,50:2563EB,100:06B6D4&amp;height=160&amp;section=header&amp;text=zyaochen&amp;fontSize=48&amp;fontColor=ffffff&amp;animation=fadeIn&amp;fontAlignY=36" width="100%" alt="zyaochen" />

<p>我是一名 SRE，日常做线上稳定性。<br />这里的仓库主要用来从零学大模型、拆 LLM 推理引擎和 GPU 优化，配套代码在 CPU 上就能跑；另有 nginx 源码教程和几个 agent、运维小工具。</p>

<p>
  <a href="https://zyaochen.github.io/"><img src="https://img.shields.io/badge/%E9%A1%B9%E7%9B%AE%E4%B8%BB%E9%A1%B5-zyaochen.github.io-2563EB?style=flat-square&amp;labelColor=1F2937" alt="项目主页" /></a>
  <a href="https://zyaochen.github.io/#read"><img src="https://img.shields.io/badge/%E5%9C%A8%E7%BA%BF%E9%98%85%E8%AF%BB-7_%E5%A5%97%E4%B9%A6%E7%A8%BF-0891B2?style=flat-square&amp;labelColor=1F2937" alt="在线阅读" /></a>
  <a href="https://zyaochen.github.io/weft/"><img src="https://img.shields.io/badge/Weft-%E5%9C%A8%E7%BA%BF%E6%BC%94%E7%A4%BA-2563EB?style=flat-square&amp;labelColor=1F2937" alt="Weft 在线演示" /></a>
  <a href="https://colab.research.google.com/github/zyaochen/zero-to-vllm/blob/main/colab/02-ledger.ipynb"><img src="https://img.shields.io/badge/Colab-vLLM_%E7%AC%AC_2_%E7%AB%A0-F9AB00?style=flat-square&amp;logo=googlecolab&amp;logoColor=white&amp;labelColor=1F2937" alt="在 Colab 打开 zero-to-vllm 第 2 章" /></a>
</p>

</div>

## 书稿

每套都有在线阅读版（侧边目录、全文搜索、深浅色），Markdown 原稿在仓库的 `book/` 下。

| 系列 | 讲什么 | 篇幅 | 配套 |
|---|---|---|---|
| [从零掌握大模型](https://zyaochen.github.io/zero-to-llm/) | 从矩阵乘法讲到推理服务、RAG、Agent 和工程交付，每个技术决策都落到效果、显存、时延、成本四笔账上 | 30 篇 + 总览 | [81 段代码](https://github.com/zyaochen/zero-to-llm)，`tools/verify.py` 和正文输出逐字核对 |
| [从 0 开始 vLLM](https://zyaochen.github.io/zero-to-vllm/) | 显存账本、调度与抢占、Paged KV、前缀缓存、PD 分离、LoRA、部署实战 | 26 章 | [26 个代码目录](https://github.com/zyaochen/zero-to-vllm)，每章一个 Colab |
| [从 0 开始 SGLang](https://zyaochen.github.io/zero-to-sglang/) | 内存池与页表、RadixAttention、overlap 调度、HiCache、PD 分离 | 25 章 | [24 个代码目录](https://github.com/zyaochen/zero-to-sglang)，每个目录一个 Colab |
| [从 0 开始 llama.cpp](https://zyaochen.github.io/zero-to-llama/) | GGUF / GGML 结构、内存与带宽预测器、量化对照、CPU 调优、投机解码 | 22 章 | [22 个代码目录](https://github.com/zyaochen/zero-to-llama)，每章一个 Colab |
| [从 0 开始 GPU 优化](https://zyaochen.github.io/zero-to-gpu/) | 性能账本、访存与 GEMM、Tensor Core、互联、NCCL、K8s 调度、可靠性 | 33 章 | [24 个代码目录](https://github.com/zyaochen/zero-to-gpu)，每个目录一个 Colab |
| [LLM 系列](https://zyaochen.github.io/llm-atlas/) | 地基、系统、工程、场景四层长文，讲清原理、取舍和数字出处 | 65 篇 + 总览 | 不配代码，[694 张配图](https://github.com/zyaochen/llm-atlas) |
| [nginx 运维、开发与云原生](https://zyaochen.github.io/nginx-devops/) | 按 nginx 1.31.10 源码讲配置怎么生效，写一个自己的模块，再把 nginx 放进 Kubernetes | 31 章 | [32 个实验目录](https://github.com/zyaochen/nginx-devops)，和正文输出逐行比对 |

## 工具

- **[Weft](https://github.com/zyaochen/weft)**：无限画布上的对话，节点之间的连线就是下一轮的上下文。剪断一根线，下一次回答就读不到那段历史；Claude Code / Codex 会话也能打开成画布来修剪和分支。fork 自 [ThoughtDAG](https://github.com/chenxiachan/thoughtdag)（MIT）。
- **[ngx_stream_upstream_check_module](https://github.com/zyaochen/ngx_stream_upstream_check_module)**：给 nginx 四层代理加主动健康检查，支持 TCP、UDP、HTTP 探测，补丁覆盖 nginx 1.24–1.31。
- **[onssh](https://github.com/zyaochen/onssh)**：在浏览器里登录 SSH 终端，Python 3 + xterm.js，带主机密钥校验和目标白名单。

后两个是 2017 年前后的老项目，2026 年 11 月按当前版本重新整理过。

## 日常工作

- **全球高可用机房架构**：架构优化、风险识别、演练攻防、混沌工程。
- **数据面高可用**：评估数据库、缓存和 KV 存储的冗余度与故障域分布，建设自动化运维。
- **可靠性度量**：以容灾标准为基线，度量现网的达成情况，找出差距，推动改进。
- **让 agent 接手重复的分析**：取数、对账、写复盘初稿做成 agent 能调用的工具，人只做判断。Weft 就是在这件事里做出来的。

更早几年做 DevOps：Docker、Kubernetes、Go、nginx。

## 30 秒试一下

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

不想在本地装环境，点上面的 Colab 徽章，在浏览器里跑同一章的单元测试和 CPU 命令。想直接用 Weft：

```bash
npm install -g weft-canvas
weft serve       # 在 http://localhost:3001 提供画布并打开浏览器
```

## 限制

- **zero-to-\* 是学习用的配套代码，不是库**。模拟器复现的是引擎主干里的关键账本，结果要和真实日志对账才算数。各仓库 README 写了版本基线（具体到 commit），换了版本，数字可能对不上。
- **zero-to-llm 后半部分的案例读数是假设读数**。准确率、时延、成本这些案例数字是示意，不是实测；能复算的是代码输出和公式推导，正文里都标明了。
- **Colab notebook 只放 CPU 能跑的命令**。要 GPU、模型文件或运行中服务的命令没有放进去。
- **nginx-devops 的运维篇和开发篇实验只在 macOS arm64 上跑过**，云原生篇的实验要一台装了 Docker 和 kind 的 Linux 机器。
- **Weft 的画布数据存在浏览器 IndexedDB 里**，没有同步也没有账号，用「导出备份（.json）」备份；桌面安装包未签名。详见它的 [README](https://github.com/zyaochen/weft#limitations)。
- 2016–2017 年的旧博客已下线，源文件留在 [archive/hexo-blog-2017](https://github.com/zyaochen/zyaochen.github.io/tree/archive/hexo-blog-2017) 分支。

对哪个仓库有问题，直接在那个仓库开 issue。
