# ThinkingLearning

AI Agent 学习技能包集合 - 为 AI Agent 设计的自包含学习系统。

## 设计理念

每个技能包（`*-skills/`）都是**自包含**的，可以直接复制到任何支持 Skills 的 AI Agent 中使用。

**核心原则**：
- AI 是学生的学习伙伴和引路人
- 讲解与提问并重，循序渐进
- 引导思考，确保真正学会

## 技能包列表

### [first-principles-skills](first-principles-skills/) - 第一性原理学习系统

基于李善友教授13节课程，通过循序引导式教学 + 费曼学习法训练第一性原理思考方式。

**教学方式**：讲解铺垫 → 苏格拉底式提问 → 费曼检验 → 总结强化

**触发词**：开始学习、开始第N课、我的理解、查看进度、复习、测试

**目录结构**：
```
first-principles-skills/
├── SKILL.md                   # 核心配置（入口文件）
├── courses/                   # 13节课程内容
├── references/                # 参考文档（提问模板、费曼方法等）
└── templates/                 # 用户数据模板
```

**学习数据**存储在同级目录 `first-principles-study/{user_id}/`

## 如何使用

### 在 Claude Code 中使用

1. 将技能包目录添加到 Claude Code 的 skills 配置中
2. 使用触发词开始学习，如：`开始第1课`

### 部署到其他 Agent

1. 复制整个 `*-skills/` 目录到目标项目
2. 在同级目录创建对应的 `*-study/` 目录存储用户数据
3. 配置 Agent 读取 `SKILL.md` 作为行为准则

## 技能包规范

每个技能包应包含：

| 文件/目录 | 作用 |
|----------|------|
| `SKILL.md` | 核心配置，定义角色、行为、触发词 |
| `courses/` | 课程内容 |
| `references/` | 参考文档 |
| `templates/` | 用户数据模板 |

## 项目结构

```
ThinkingLearning/
├── first-principles-skills/   # 第一性原理技能包
│   ├── SKILL.md
│   ├── courses/
│   ├── references/
│   └── templates/
├── first-principles-study/    # 用户学习数据（gitignore）
├── .gitignore
└── README.md
```

## 许可

个人学习使用。
