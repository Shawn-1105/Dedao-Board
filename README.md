# Dedao Board

A private advisory board powered by perspective skills. When you face a complex question, summon multiple thinkers to analyze it from their unique angles — then let an AI moderator synthesize consensus, disagreements, and actionable next steps.

## What's Inside

### The Board Orchestrator

- **sidonghui** — The private board meeting skill. Structures the discussion into 8 steps: topic clarification → member selection → key questions → problem reframing → independent judgments → cross-examination → convergence → action card.

### Board Members (Perspective Skills)

Each member is a distillation of a real thinker's mental models, decision heuristics, and expression DNA:

| Member | Focus Area | Key Mental Models |
|--------|-----------|-------------------|
| **古典 (Gu Dian)** | Personal development, career transformation | Mental walls, super individual, unique knowledge + niche needs |
| **李笑来 (Li Xiaolai)** | Investment, long-term thinking, attention management | Compounding accumulation, attention > time > money, OS upgrade |
| **查理·芒格 (Charlie Munger)** | Multi-disciplinary thinking, investment, psychology | Inversion, latticework of mental models, circle of competence |
| **万维钢 (Wan Weigang)** | Scientific thinking, anti-commonsense, systems | Fox thinking, deliberate practice, humans > AI |
| **吴军 (Wu Jun)** | Engineering thinking, tech history, general education | Energy + information, stackable progress, historical telescope |
| **刘润 (Liu Run)** | Business strategy, entrepreneurship, efficiency | Underlying logic, evolutionary thinking, leverage, value formula |

## How It Works

1. You raise a question
2. The moderator clarifies the topic and selects the most relevant members
3. Members ask probing questions first (no advice yet)
4. The moderator reframes your problem
5. Members give independent judgments
6. Cross-examination on key disagreements
7. Moderator converges with prioritized action items
8. You get a concrete action card with timeline and success criteria

## How to Use

These are [Claude Code skills](https://docs.anthropic.com/en/docs/claude-code). Copy the skill directories into your project's `.claude/skills/` folder:

```
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

Then in Claude Code, say:

- `开个私董会` or `大家怎么看` — activate the board
- `用吴军的视角` — activate a single member
- `散会` — end the session

## Adding New Members

The board dynamically discovers all `*-perspective` skills. Add any new perspective skill to the `.claude/skills/` directory and it automatically joins the board.

## Structure

```
skills/
├── sidonghui/                    # Board orchestrator
│   └── SKILL.md
├── gudian-perspective/           # Gu Dian
│   ├── SKILL.md
│   └── references/research/      # 6 research documents
├── liurun-perspective/           # Liu Run
├── lixiaolai-perspective/        # Li Xiaolai
├── munger-perspective/           # Charlie Munger
├── wanweigang-perspective/       # Wan Weigang
└── wujun-perspective/            # Wu Jun
```
