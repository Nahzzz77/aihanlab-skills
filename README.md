# AiHanLab Skills

面向产品研究、内容创作与知识表达的个人 Codex Skills 集合。每个 Skill 都是一套可复用的工作方法，可按需单独安装和调用。

> 这是个人维护的开源仓库，不是 Anthropic 或 OpenAI 的官方项目，也不代表任何上游项目对本仓库的认可。

## 当前 Skill

| Skill | 适用场景 | 入口 |
|---|---|---|
| `aihanlab-competitive-analysis` | 跨行业竞品分析、产品拆解、定位比较、能力矩阵、差异化与 MVP 决策 | [查看 Skill](.codex/skills/aihanlab-competitive-analysis/SKILL.md) |
| `aihanlab-xhs-knowledge-notes` | 面向 AI 初学者的小红书知识图解、概念词解和多图笔记 | [查看 Skill](.codex/skills/aihanlab-xhs-knowledge-notes/SKILL.md) |
| `human-writing` | 通用中文创作、改稿、叙事、科普、评论、口播与演讲稿 | [查看 Skill](.codex/skills/human-writing/SKILL.md) |

## `aihanlab-competitive-analysis`

这是一套基于证据的通用竞品分析方法，不限定旅行行业。它可以处理链接、录屏、截图、文件、官方资料、评论和实际体验，适用于 AI 产品、App、小程序、SaaS、内容平台、交易平台、消费应用和硬件。

核心特点：

- 区分已验证事实、可见线索、第三方报告、分析推断和未观察项
- 把“有没有”与“做得好不好”分开判断
- 根据行业和用户决策动态选择比较维度
- 还原真实用户流程，而不是只罗列功能
- 用加权能力矩阵支持定位、同质化、差异化和 MVP 取舍
- 明确公开数据、隐私、版权、平台条款与访问控制边界

调用示例：

- “用 `$aihanlab-competitive-analysis` 分析这个小程序录屏，告诉我哪些是 MVP 必须做的。”
- “比较这三款 AI SaaS 的定位、工作流和差异化机会。”
- “分析两个内容平台的推荐功能，我们应该跟进、拒绝还是做出差异。”
- “把调研资料整理成一页竞品战卡，并标出证据强弱。”

## 其他 Skill

### `aihanlab-xhs-knowledge-notes`

负责选题判断、事实核验、故事化脚本、3:4 多图规划、标题正文话题和视觉生成提示，适合将 AI 概念、长文本、截图或文件整理为小红书知识内容。

### `human-writing`

负责检查材料充分度、区分现实与虚构边界、保留自然中文节奏，并清理机构腔、营销腔和模型腔。包含通用写作参考与硬性规则检查脚本。

## 安装

克隆仓库后，把需要的 Skill 目录复制到 Codex Skills 目录：

```bash
git clone https://github.com/Nahzzz77/aihanlab-skills.git
mkdir -p ~/.codex/skills
cp -R aihanlab-skills/.codex/skills/aihanlab-competitive-analysis ~/.codex/skills/
```

也可以按同样方式复制其他 Skill。重新启动或刷新 Codex 后，通过 `$skill-name` 显式调用；满足描述中的触发条件时，运行环境也可能自动选择对应 Skill。

## 使用边界

- 竞品结论会随版本、地区、账号、套餐和时间变化；报告应保留研究日期与证据来源。
- 只分析公开或用户有权提供的资料，不绕过登录、付费墙、限流、反爬、权限或技术保护。
- 不要把私密录屏、账号信息、本机路径、内部路线图或未公开产品计划提交到公开仓库。
- 社交平台内容和用户评论可能带有样本偏差、商业合作或时效问题，不应直接当作代表性事实。
- Skill 输出是研究和决策辅助，不替代法律、隐私、安全或合规审查。

## 目录结构

```text
.codex/
└── skills/
    ├── aihanlab-competitive-analysis/
    │   ├── SKILL.md
    │   ├── LICENSE
    │   ├── NOTICE
    │   ├── agents/
    │   └── references/
    ├── aihanlab-xhs-knowledge-notes/
    └── human-writing/
        ├── SKILL.md
        ├── references/
        └── scripts/
```

## 许可与来源

各 Skill 目录可能采用不同许可，请以对应目录内的文件为准。

`aihanlab-competitive-analysis` 受到 Anthropic `knowledge-work-plugins` 仓库中 `competitive-brief` Skill 的启发，并在名称、结构、证据模型、行业适配、安全边界和输出契约上进行了实质修改。该目录按 Apache License 2.0 提供，详见其 [LICENSE](.codex/skills/aihanlab-competitive-analysis/LICENSE) 与 [NOTICE](.codex/skills/aihanlab-competitive-analysis/NOTICE)。

其他 Skill 不会因为新增这一目录而自动改为 Apache License 2.0。
