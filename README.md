# Dedao Board

`Dedao Board` 是一个独立的 Claude Code skills 项目，用来把“私董会”及其成员视角打包成一个可复用仓库。

项目包含 1 个主持型 skill 和 6 个成员型 perspective skills，适合在遇到复杂问题时，快速拉起一场多视角讨论，最后收敛成行动建议。

## 包含内容

- `sidonghui`：私董会主持人，负责澄清议题、组织发言、提炼分歧、输出行动卡
- `gudian-perspective`：古典视角
- `liurun-perspective`：刘润视角
- `lixiaolai-perspective`：李笑来视角
- `munger-perspective`：芒格视角
- `wanweigang-perspective`：万维钢视角
- `wujun-perspective`：吴军视角

说明：

- 本仓库只包含私董会及其成员 skill
- 明确排除 `huashu-nuwa`
- 不包含其他非 skill 文件

## 使用方式

把本仓库中的 `skills/` 下目录复制到你的项目 `.claude/skills/` 中：

```text
your-project/
└── .claude/
    └── skills/
        ├── sidonghui/
        ├── gudian-perspective/
        ├── liurun-perspective/
        ├── lixiaolai-perspective/
        ├── munger-perspective/
        ├── wanweigang-perspective/
        └── wujun-perspective/
```

然后在 Claude Code 中使用：

- `开个私董会`
- `大家怎么看`
- `让芒格和吴军来讨论`
- `用刘润的视角看这个问题`

## 目录结构

```text
DedaoBoard/
├── README.md
├── .gitignore
└── skills/
    ├── sidonghui/
    │   └── SKILL.md
    ├── gudian-perspective/
    │   ├── SKILL.md
    │   └── references/research/
    ├── liurun-perspective/
    │   ├── SKILL.md
    │   └── references/research/
    ├── lixiaolai-perspective/
    │   ├── SKILL.md
    │   └── references/research/
    ├── munger-perspective/
    │   ├── SKILL.md
    │   └── references/research/
    ├── wanweigang-perspective/
    │   ├── SKILL.md
    │   └── references/research/
    └── wujun-perspective/
        ├── SKILL.md
        └── references/research/
```

## 项目说明

- `sidonghui` 会自动发现同目录下的 `*-perspective` 成员 skill
- 当前仓库已内置 6 位成员，可直接作为独立项目使用
- 如果后续新增其他 `*-perspective` skill，也可以继续接入私董会机制
