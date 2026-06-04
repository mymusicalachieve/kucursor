# Ad Agency — Cursor Skill

광고 대행사 캠페인을 **AE → 카피 → 제작 4팀(병렬) → 대표 검수 → 바이블 통합**까지 오케스트레이션하는 Cursor Agent Skill입니다.

## What's included

```
.cursor/
├── skills/ad-agency/SKILL.md   # Main orchestrator skill
└── agents/
    ├── ad-ae.md
    ├── ad-copywriter.md
    ├── ad-image-team.md
    ├── ad-video-team.md
    ├── ad-outdoor-team.md
    ├── ad-creative-team.md
    └── ad-ceo-review.md
```

## Setup

1. Clone this repository.
2. Open the project folder in **Cursor**.
3. The skill loads automatically from `.cursor/skills/ad-agency/`.

For personal use across all projects, copy `.cursor/skills/ad-agency/` to:

```
Windows: C:\Users\<YOU>\.cursor\skills\ad-agency\
macOS/Linux: ~/.cursor/skills/ad-agency/
```

## Usage

In Cursor Agent chat, start a campaign with a prompt like:

> 브랜드 캠페인 기획해줘. 브랜드는 OO, 목표는 인지도 향상, 타겟은 20대 여성.

The agent will run the full pipeline and save outputs under `campaigns/{brand-slug}/`:

| Step | Output |
|------|--------|
| AE | `01_ae_brief.md` |
| Copy | `02_copy.md` |
| Image / Video / Outdoor / Creative | `03`–`06` (parallel) |
| CEO review | `07_review.md` |
| Campaign bible | `08_campaign_bible.md` |

## Requirements

- [Cursor](https://cursor.com) with Agent mode
- Subagent profiles in `.cursor/agents/` (included in this repo)
