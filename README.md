# Lecture Study Skills

将老师课件整理成复习笔记或详细自学讲义的两份 Agent Skills。中文为主，保留英文术语、可回查的页码和逐步例题。

| 技能 | 适合需求 | 默认成品 |
| --- | --- | --- |
| [summarize-slides](skills/summarize-slides/SKILL.md) | 考前复习、重点总结、公式速查 | TeX + PDF |
| [lecture-tutor](skills/lecture-tutor/SKILL.md) | 详细讲解、自学讲义、证明与直觉 | TeX + PDF |

两者都尊重明确指定的 Markdown、仅 TeX 或聊天输出。PDF 是否可以生成取决于运行环境实际提供的编译和导出能力。

## 使用

将 `skills/` 下所需的技能文件夹完整复制到 Agent 使用的技能目录，保留 `references/` 和 `LICENSE`。例如 Codex 的用户技能目录是 `~/.codex/skills/`；其他客户端按其配置选择目录。已安装同名技能时先备份并替换原目录，避免同时加载两份同名技能。

```text
用 summarize-slides 把这个课件整理成复习笔记，只要 Markdown。
保留页码、英文术语，例题要有步骤。
```

```text
用 lecture-tutor 详细讲解这个课件的第 2–4 章。
区分课件原证明与补充证明，生成 TeX 和 PDF。
```

PDF 输入优先配合可用的 PDF 读取技能或等价工具。内置 LaTeX 编辑器可用时优先使用；本地构建需具备支持中文的引擎、字体和宏包。Markdown 模式无需 LaTeX。不自动安装编译器。

## 本次改进

- 保留本地已有的 Markdown 模式、稀疏重点标签、白话解释和逐步例题。
- 区分 PDF 物理页、印刷页及不同来源，增加覆盖表与针对来源的核查。
- 明确标记新增例题/证明；无法确认的数学内容不编造。
- 去掉按页数比例、句数或重点标签配额凑内容的要求。
- 数据库示例独立为按需参考，补充集合/多重集、NULL、SQL 方言等语义边界。
- 区分内置预览、成功编译和实际 PDF 导出，移除写死的 `/tmp` 与 Linux 命令。
- 去掉重复约束和无关技能禁用规则，保留缺工具时的可行处理路径。

## 来源与许可

本仓库基于用户电脑上已有版本改进，不代表原作者官方版本：

- `summarize-slides` 来源：[Li-Baichuan-James/summarize-slides-skill](https://github.com/Li-Baichuan-James/summarize-slides-skill)，原版权 Li Baichuan。该技能的本地版本另含 Markdown、重点标签和数据库逐步例题定制。
- `lecture-tutor` 来源：[Epiphanythu/lecture-tutor-skill](https://github.com/Epiphanythu/lecture-tutor-skill)，原版权 Epiphanythu。

原始 MIT 许可分别保留在两份技能目录。新增文档与修改同样以 MIT 许可发布，见根目录 [LICENSE](LICENSE)。仓库仅包含技能和说明，不包含个人课件、学习笔记、账号凭据或电脑路径。

## 验证范围

发布前检查技能元数据、引用文件和许可证，并进行场景审查。具体记录见 [REVIEW.md](REVIEW.md)。本轮没有使用真实课程 PDF 完整生成讲义，实际课程内容质量与 PDF 排版仍需要在使用时核验。
