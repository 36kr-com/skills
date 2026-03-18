# 36kr Skills

A collection of agent skills for querying [36kr](https://36kr.com) open data, powered by the [openclaw](https://36kr.com?channel=openclaw) API.

## Available Skills

### 36kr-hotlist

Fetches the 36kr 24-hour hot list articles. Updated hourly.

**Use when:**
- 查热榜 / 36kr热榜 / 今日热榜
- "What's trending on 36kr?"
- "Show me the top articles today"
- 看看今天最火的文章 / 热点资讯

**Data source:** `https://openclaw.36krcdn.com/media/hotlist/{date}/24h_hot_list.json`

---

### 36kr-aireportlist

Fetches the 36kr AI self-report (自助报道) article list. Updated every 2 hours.

**Use when:**
- 查自助报道 / 36kr自助报道 / 最新自助报道
- "Show me the latest AI report articles"
- AI寻求报道 / 36kr aireport

**Data source:** `https://openclaw.36krcdn.com/media/aireport/{date}/ai_report_articles.json`

---

## Installation

```bash
# Install all skills
npx skills add <your-github-username>/36kr-skills

# Install a specific skill
npx skills add <your-github-username>/36kr-skills --skill 36kr-hotlist
npx skills add <your-github-username>/36kr-skills --skill 36kr-aireportlist
```

## Usage

Once installed, the skills are automatically triggered when you ask relevant questions in your agent:

```
查热榜
36kr热榜有什么？
看看今天最火的文章
查自助报道
最新36kr自助报道列表
```

## Skill Structure

```
skills/
├── 36kr-hotlist/
│   ├── SKILL.md              # Agent instructions
│   ├── api-reference.md      # Full API spec
│   ├── examples.md           # Usage examples
│   └── scripts/
│       ├── fetch_hotlist.py  # Python query script
│       └── fetch_hotlist.sh  # Shell query script
└── 36kr-aireportlist/
    ├── SKILL.md              # Agent instructions
    ├── api-reference.md      # Full API spec
    ├── examples.md           # Usage examples
    └── scripts/
        ├── fetch_aireport.py # Python query script
        └── fetch_aireport.sh # Shell query script
```

## License

MIT
