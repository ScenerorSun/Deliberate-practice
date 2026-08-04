# Deliberate-practice — 刻意练习 Skill 蒸馏包

> 把安德斯·艾利克森《刻意练习》（Peak: Secrets from the New Science of Expertise, 2016）蒸馏成一组可被 AI Agent 调用的方法论 skills。

## 这是什么

一本 300 页的书，拆成 6 个原子化的、带触发条件的、可执行的 AI skills。每个 skill 都是一个 `SKILL.md`，包含：

- **R** — 原文引用（标注出处）
- **I** — 方法论骨架（用自己的话重写）
- **A1** — 书中的应用案例
- **A2** — 触发场景与语言信号（何时该激活）
- **E** — 可执行步骤（含完成标准）
- **B** — 边界与失败模式（何时不该用）

蒸馏流水线：cangjie-skill（RIA-TV++：Adler 分析 → 5 提取器并行 → 三重验证 → RIA++ 构造 → Zettelkasten 链接 → 压力测试 → 交付）。

## Skill 列表

| skill | 一句话定位 | 触发关键词 |
|-------|-----------|-----------|
| `deliberate-practice-engine` | 诊断任何练习是否有效，输出升级处方 | 练习没用 / 怎么进步 / 这样练对吗 |
| `comfort-zone-calibration` | 判断挑战度是否到位（80/20 原则） | 舒适区 / 假努力 / 加大难度 |
| `mental-representation-builder` | 从新手思维升级到专家思维 | 专家直觉 / 没框架 / 建立语感 |
| `plateau-breakthrough` | 瓶颈期换策略三步法 | 卡住了 / 练不上去 / 突破不了 |
| `feedback-loop-designer` | 无导师时搭建即时反馈系统 | 没老师 / 怎么复盘 / 如何检验 |
| `talent-myth-debunker` | 拆穿天赋决定论 | 没天赋 / TA 是天才 / 要天赋吗 |

## 目录结构

```
.
├── BOOK_OVERVIEW.md        # 整书理解（Adler 四步）
├── verified.md             # 三重验证通过的单元 + 判定理由
├── INDEX.md                # skill 地图 + 引用图
├── GLOSSARY.md             # 共享术语词典
├── DIGEST.md               # 精华长文（不读全书也够用）
├── PIPELINE_STATE.md       # 蒸馏流水线状态
├── candidates/             # 原始候选池（审计用）
├── rejected/               # 被淘汰单元 + 原因
└── <skill-slug>/
    ├── SKILL.md            # skill 本体（可被 agent 加载）
    ├── test-prompts.json   # 触发测试（含诱饵题）
    └── description.md      # 知乎文体简介
```

## 如何使用

三种方式：

1. **直接读 `DIGEST.md`** — 只想了解核心方法论，5 分钟读完精华。
2. **把某个 `<skill>/SKILL.md` 安装到你的 Agent skills 目录**（如 `~/.workbuddy/skills/` 或项目 `.claude/skills/`），Agent 就能在你"练了很久没进步""卡住了""没天赋"等场景自动调用对应方法论。
3. **用 `test-prompts.json` 验证触发** — 每个 skill 附测试用例，含应调用/不应调用（诱饵）场景。

## 使用路径建议

- 新手起步：`talent-myth-debunker`（破障碍）→ `deliberate-practice-engine`（定方向）
- 练了没感觉：`deliberate-practice-engine`（诊断）→ `comfort-zone-calibration`（查强度）
- 明确卡住：`plateau-breakthrough` → `mental-representation-builder`
- 自学无师：`feedback-loop-designer`

## 版权说明

- 原书版权归安德斯·艾利克森（Anders Ericsson）与罗伯特·普尔（Robert Pool）所有。
- 本仓库的 SKILL.md 为方法论蒸馏产物（引用片段 ≤150 字，用于学术讨论）。
- 蒸馏工具：kangarooking/cangjie-skill（AGPL-3.0）。本仓库内容为独立创作，非衍生代码。

## 蒸馏信息

- 蒸馏日期：2026-08-04
- 蒸馏方式：cangjie-skill RIA-TV++ 流水线
- 源文本：Z-Library 电子版全文 → Markdown

---

*由既明博士工作流自动生成。*
