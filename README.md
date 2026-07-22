# MOI Benchmark

MOI Benchmark 由五个彼此独立的功能测评 Track 组成。每个 Track 的方案、调研、实现、数据、参评系统、运行记录和报告全部保存在自己的根级目录内。

## 目录

```text
.
├── astra/              # Astra Benchmark Track
├── memoria/            # Memoria Benchmark Track
├── document-parsing/   # 文档解析 Benchmark Track
├── rag/                # RAG Benchmark Track
├── nlp2sql/            # NLP2SQL Benchmark Track
├── docs/               # 仅保存跨 Track 治理、ADR、进度和历史混合稿
├── .github/            # 项目级 Issue / PR 模板
├── README.md
└── ROADMAP.md
```

## Track 内部约定

每个 Track 独立使用以下结构；没有内容的目录不提前创建：

```text
<track>/
├── README.md           # Track 状态、负责人和入口
├── plans/              # drafts / approved / superseded
├── research/           # 当前证据与 archive
├── benchmark/          # contracts / tasks / adapters / evaluators / harness / tests
├── datasets/           # manifest、版本、划分和校验和；不提交大型 payload
├── systems/            # 参评系统、模型、工具和环境版本
├── runs/               # 不可变 run record 与外部工件哈希
├── reports/            # Track 分析稿、里程碑报告和发布版
├── decisions/          # 仅影响该 Track 的 ADR
└── progress/           # Track 阶段快照
```

跨 Track 共同规则放在 `docs/`；任何只服务某个 Track 的内容不得放在根目录或 `docs/`。

## 当前状态

| Track    | 当前状态       | 入口                                  |
| -------- | -------------- | ------------------------------------- |
| Astra    | 方案草稿待审阅 | [astra/](astra/)                       |
| Memoria  | 待建立方案     | [memoria/](memoria/)                   |
| 文档解析 | 待建立方案     | [document-parsing/](document-parsing/) |
| RAG      | 待建立方案     | [rag/](rag/)                           |
| NLP2SQL  | 方案草稿待审阅 | [nlp2sql/](nlp2sql/)                   |

Astra 与 NLP2SQL 的草稿尚未审阅，不代表已经确认竞品、指标、任务、排期或资源。

## 留痕链

```text
Track Research
  → Track Plan 审阅
  → Issue / ADR
  → Benchmark 资产 PR
  → Dataset / System / Task 版本冻结
  → Run Record
  → Track Report
  → Release
  → 持续回归
```

项目级推进见 [ROADMAP.md](ROADMAP.md)，目录边界见 [docs/repository-structure.md](docs/repository-structure.md)。
