# 彤彤的 AI 技能集 · Tongtong AI Skills

两个「人设型」AI 技能（Agent Skills），让 AI 化身专业顾问，既能回答专业问题，也能产出对应主题的**内容**（小红书 / 短视频脚本 / 公众号长文）。

> 技能格式：`SKILL.md`（YAML frontmatter + Markdown 正文）+ `references/` 参考资料。适用于 WorkBuddy、Claude Code、以及任何支持 Agent Skills 的智能体。

---

## 包含的技能

| 技能 | 人设 | 覆盖领域 |
|---|---|---|
| [wine-somm-mentor](./wine-somm-mentor) | 世界级侍酒师导师 + 90 后红酒内容创作者 | 品种、产区风土、酿造、橡木桶、品鉴、质量分级、缺陷判断、侍酒服务、餐酒搭配 |
| [home-organizing-planner](./home-organizing-planner) | 资深整理收纳规划师 + 90 后生活方式创作者 | 整理收纳体系、家庭空间规划、小户型、衣橱管理、搬家整理、断舍离、家庭动线、生活美学 |

---

## 一、红酒心灵大师 · wine-somm-mentor

**定位**：让没有葡萄酒基础的人也能喜欢葡萄酒，让专业人士也认可深度。

**它做什么**

- **陪伴式教学**：问品种、产区、怎么选酒、怎么品、怎么配餐、怎么醒酒 —— 给出准确、系统、好懂的讲解。
- **内容创作**：以这个人设产出小红书笔记、短视频口播脚本、公众号长文、专业品酒笔记。

**表达原则**：专业但易懂，像顶级侍酒师面对普通消费者教学；先讲体验，再给知识；先建画面，再上术语。

**触发场景**：提到 葡萄酒 / 红酒 / 白葡萄酒 / 香槟 / 品种 / 产区 / 品鉴 / 餐酒搭配 / 醒酒 / 侍酒，或求推荐「新手入门喝什么」「送什么酒」。

**文件结构**

```
wine-somm-mentor/
├── SKILL.md
├── references/
│   ├── knowledge.md            # 系统知识库：品种/产区/酿造/气候/橡木桶/品鉴/质量/缺陷/侍酒/搭配
│   └── voice-and-content.md    # 口吻校准、教学四步结构、内容模板、Avoid 清单
└── assets/
    ├── tasting_note_template.md   # 专业品酒笔记模板
    └── content_templates.md       # 小红书 / 短视频 / 公众号模板 + 标题钩子库
```

---

## 二、整理收纳规划心灵大师 · home-organizing-planner

**定位**：整理不是丢东西，而是重新认识自己；空间不只是变整齐，而是帮人找回生活的掌控感。

**它做什么**

- **陪伴式咨询**：用户描述家乱、找不到东西、换季崩溃时，给出有温度、可落地的诊断与建议。
- **内容创作**：以这个人设产出小红书笔记、短视频口播脚本、公众号长文等生活方式内容。

**核心框架**：**空间问题 → 心理需求 → 生活改变**。一次只给一个今天就能做的小行动，绝不一次性甩满方案。

**触发场景**：提到 收纳 / 整理 / 断舍离 / 衣橱 / 搬家 / 小户型 / 动线 / 空间规划，或表达「我是不是太懒了」这类自责情绪。

**文件结构**

```
home-organizing-planner/
├── SKILL.md
└── references/
    ├── methodology.md        # 十大领域方法论 + 诊断提问清单（核心知识库）
    └── voice-and-formats.md  # 口吻校准、咨询五步结构、内容模板、Avoid 清单
```

---

## 安装

把需要的技能文件夹放进你的 Agent 技能目录即可：

```bash
# WorkBuddy / Claude Code（用户级）
git clone https://github.com/804531603-sketch/tongtong-ai-skills.git
cp -r tongtong-ai-skills/wine-somm-mentor ~/.workbuddy/skills/
cp -r tongtong-ai-skills/home-organizing-planner ~/.workbuddy/skills/
```

> Claude Code 用户把路径换成 `~/.claude/skills/`。
> 装完后重启 Agent，直接用自然语言触发，不需要记任何命令。

---

## 设计说明

这两个技能都属于「**人设型技能**」：不是工具箱，而是一套**说话方式 + 知识体系 + 内容生产方法**。所以每个技能里都有三样东西：

1. **Persona** —— 开口前要进入的身份与信念
2. **references/** —— 支撑专业度的知识库
3. **红线** —— 明确写出「不做什么」（不堆术语、不制造焦虑、不贴标签、不夸大）

如果你也想写自己的技能，可以直接拿这两个当模板。

---

## License

MIT —— 见 [LICENSE](./LICENSE)。可自由使用、修改、商用，保留版权声明即可。
