# Daily Digest Skill

Fetch and summarize RSS and Substack feeds covering AI/ML engineering and frontier model labs. Send clean, focused digests to Shelby's Telegram every morning at 7am.

## Tools

- `web_fetch` — ONLY tool used, pulls RSS/Substack feeds directly (no Brave API, no web search)
- Telegram delivery via message tool

## Feeds

### AI/ML Engineering
- https://rsshub.app/huggingface/papers (HuggingFace daily papers)
- https://www.reddit.com/r/MachineLearning/.rss
- https://www.reddit.com/r/LocalLLaMA/.rss (applied ML, local models)

### Frontier Model Labs
- https://openai.com/news/rss.xml
- https://www.anthropic.com/rss.xml

### Researchers & Thought Leaders
- https://karpathy.bearblog.dev/feed/ (Andrej Karpathy)
- https://karpathy.substack.com/feed (Karpathy Substack)
- https://ai.meta.com/blog/feed/ (LeCun's Meta AI lab)

### AI Engineering & Builders
- https://simonwillison.net/atom/everything/ (Simon Willison)
- https://simonw.substack.com/feed (Simon Willison Substack)
- https://huyenchip.com/feed.xml (Chip Huyen)

### Agents & Applications
- https://openclaw.ai/blog/rss (OpenClaw blog)
- https://www.oneusefulthing.org/feed (Ethan Mollick)

### Ethics & Policy
- https://www.dair-institute.org/blog/rss (Timnit Gebru's DAIR)

### Tech News & Discussion
- https://hnrss.org/frontpage (Hacker News top stories)

## Logic

For each section, surface the **3–5 most notable items** from the last 24 hours:

- Fetch each feed using `web_fetch`
- Parse items and extract publication date + title
- Keep only items from the last 24 hours
- One sentence per item
- If a section has nothing new, write "Nothing notable today."
- No fluff. Be direct. Format as plain text with section headers.
- End with a one-line **"Worth a closer look:"** callout for the single most interesting item across all sections.

## Delivery

- **Channel:** Telegram
- **Chat ID:** 
- **Format:** Plain text, no markdown
- **Schedule:** 7:00 AM Pacific, daily

---

The cron job handles scheduling. This skill defines the fetch + summarize logic that runs at 7am every morning. No API keys required—uses standard RSS and Substack feeds.
