# AiHanLab Xiaohongshu Knowledge Notes

面向 AI 初学者的小红书知识图解、概念词解和多图笔记 Skill。

> 这是个人维护的开源仓库，不是 Anthropic 或 OpenAI 的官方项目，也不代表任何上游项目对本仓库的认可。

## Skill

| Skill | 适用场景 | 入口 |
|---|---|---|
| `aihanlab-xhs-knowledge-notes` | AI 概念词解、知识图解、长文或截图转多图笔记 | [查看 Skill](.codex/skills/aihanlab-xhs-knowledge-notes/SKILL.md) |

它负责选题判断、事实核验、故事化脚本、3:4 多图规划、标题正文话题和视觉生成提示，不会盲目照读输入材料。

## 安装

```bash
git clone https://github.com/Nahzzz77/aihanlab-skills.git
mkdir -p ~/.codex/skills
cp -R aihanlab-skills/.codex/skills/aihanlab-xhs-knowledge-notes ~/.codex/skills/
```

重新启动或刷新 Codex 后，可以通过 `$aihanlab-xhs-knowledge-notes` 显式调用。

## 已拆分的 Skill

- [`aihanlab-competitive-analysis`](https://github.com/Nahzzz77/aihanlab-competitive-analysis)：跨行业竞品分析、产品拆解和差异化决策。
- [`human-writing`](https://github.com/Nahzzz77/human-writing)：自然中文创作、改稿和叙事表达。

## 使用边界

- 只处理公开资料或用户有权提供的材料。
- 不要把账号信息、本机路径、内部资料或未公开计划提交到公开仓库。
- 事实性内容应保留来源和日期，并在发布前复核。
