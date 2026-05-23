# SEO Agent — Integration Spec

## Purpose

SEO Agent (в Paperclip / Factory) читает документы из hackathon-vault и создаёт SEO-оптимизированный контент для продвижения Office Cat.

## Input Sources

| Vault Section | Documents | SEO Output |
|---------------|-----------|------------|
| `01-idea/` | Vision, positioning | Landing page copy, meta descriptions |
| `02-research/` | Market size, competitors | Blog posts, infographics, whitepapers |
| `03-product/` | PRD, features | Product pages, feature descriptions |
| `04-business/` | Business model, metrics | Investor content, press releases |
| `05-marketing/` | GTM strategy | Social media posts, email campaigns |
| `06-technical/` | Architecture | Developer docs, technical blog |
| `07-operations/` | Roadmap | Timeline content, milestone updates |

## Workflow

```
1. SEO Agent читает новые/обновлённые документы из vault
2. Анализирует ключевые слова, темы, данные
3. Генерирует SEO-контент:
   - Blog posts (1500-2500 слов)
   - LinkedIn posts (150-300 слов)
   - Twitter threads (5-10 твитов)
   - ProductHunt descriptions
   - Meta descriptions (150-160 chars)
   - Title tags (50-60 chars)
4. Сохраняет в `05-marketing/seo-output/`
5. Обновляет `05-marketing/content-calendar.md`
```

## Keyword Strategy

### Primary Keywords
- "office companion robot"
- "team social catalyst"
- "workplace wellbeing"
- "office pet robot"
- "team bonding tool"

### Secondary Keywords
- "employee engagement"
- "workplace isolation"
- "open plan office"
- "team building alternative"
- "office wellness"

### Long-tail Keywords
- "robot cat for office emotional support"
- "digital pet for team collaboration"
- "AI companion for workplace wellbeing"
- "social robot for employee engagement"

## Content Templates

### Blog Post Template
```
Title: [Number] Ways [Product] [Benefit]
Hook: Problem statement with data
Body: 
  - Point 1 (with data from vault)
  - Point 2 (with case study)
  - Point 3 (with expert quote)
CTA: [Action] → [Link]
SEO: Primary keyword in H1, secondary in H2s
```

### LinkedIn Post Template
```
Hook: Contrarian statement or question
Story: Personal experience or data
Lesson: Key insight from vault
CTA: "What do you think?" or "Link in comments"
```

## Output Structure

```
05-marketing/
├── seo-output/
│   ├── 2026-05-24-blog-market-size.md
│   ├── 2026-05-25-linkedin-founder-story.md
│   ├── 2026-05-26-twitter-thread.md
│   └── ...
├── meta-tags/
│   ├── landing-page-meta.md
│   ├── blog-meta.md
│   └── producthunt-meta.md
└── content-calendar.md (updated)
```

## Automation Rules

1. **Trigger:** Новый файл в vault → SEO Agent запускается
2. **Frequency:** Ежедневно в 09:00 UTC
3. **Priority:** 
   - P0: ProductHunt launch content
   - P1: Blog posts (2/week)
   - P2: Social media (daily)
   - P3: Meta tags (as needed)

## Quality Checks

- [ ] Ключевое слово в заголовке
- [ ] Ключевое слово в первом параграфе
- [ ] Мета-описание 150-160 символов
- [ ] Title tag 50-60 символов
- [ ] Внутренние ссылки на продукт
- [ ] Источники данных из vault
- [ ] CTA в конце

## Metrics

| Metric | Target | Tool |
|--------|--------|------|
| Organic traffic | 1000/month | Google Analytics |
| Keyword ranking | Top 10 | Ahrefs |
| Backlinks | 50 | Ahrefs |
| Social shares | 500/month | Buffer |
| Conversion rate | 2% | Mixpanel |

---

*SEO Spec v1.0 — May 23, 2026*