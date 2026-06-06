# Search Queries for Job Scraper

<!-- SETUP: Customize these queries based on your skills, target roles, and location -->

## Search Sites

Primary (Irish job market):
- **irishjobs.ie** - largest Irish job board
- **jobs.ie** - major Irish job board
- **linkedin.com/jobs** - LinkedIn job listings (filter: Ireland / Dublin)
- **indeed.ie** - Irish Indeed
- **recruit.ie** - Irish recruiter-focused board

Secondary (company career pages via Google):
- Direct Google searches with `site:` filters for known target companies

## Query Categories

Queries are grouped by priority. Each query should be combined with your location terms (e.g. "Dublin", "Leinster", "Remote Ireland") where the site supports it.

### Priority 1: Full Stack / Software Engineering (primary direction)

These match the strongest and most desired career direction.

```
site:irishjobs.ie "software engineer" React OR "Node.js" Dublin
site:irishjobs.ie "full stack engineer" Python OR TypeScript Dublin
site:jobs.ie "software engineer" React Dublin
site:linkedin.com/jobs "software engineer" "full stack" Dublin Ireland
site:linkedin.com/jobs "full stack developer" Python OR "Node.js" Dublin
```

### Priority 2: Healthtech / EHR domain expertise

Roles where healthcare SaaS background is a direct differentiator.

```
site:irishjobs.ie "software engineer" healthcare OR "health tech" Dublin OR "Remote Ireland"
site:irishjobs.ie FHIR OR "EHR" OR "electronic health record" software Dublin
site:jobs.ie healthtech OR "health tech" developer Dublin
site:linkedin.com/jobs "software engineer" healthcare FHIR Dublin Ireland
```

### Priority 3: Backend / Platform Engineering (adjacent pivot)

Roles that lean into cloud-native, distributed systems, and API engineering.

```
site:irishjobs.ie "backend engineer" Python OR FastAPI Dublin
site:irishjobs.ie "platform engineer" AWS OR Kubernetes Dublin
site:jobs.ie "backend developer" "Node.js" OR Python Dublin
site:linkedin.com/jobs "backend engineer" AWS Kafka Dublin Ireland
```

### Priority 4: AI / LLM Engineering (broader net)

Wider net for applied AI and data engineering roles.

```
site:irishjobs.ie "AI engineer" OR "LLM" Python Dublin
site:irishjobs.ie "data engineer" Kafka OR Elasticsearch Dublin
site:linkedin.com/jobs "AI engineer" Python "software engineer" Dublin Ireland
site:indeed.ie "software engineer" "machine learning" OR LLM Dublin
```

## Location Filter

When evaluating results, verify the job location is within reasonable commute distance from your home. Define acceptable areas:
- Dublin city centre (D08 and surrounding postcodes) — ideal
- Greater Dublin (Leinster commuter belt) — acceptable
- Remote (Ireland-based) — acceptable
- Hybrid with 1–2 days on-site Dublin — acceptable
- Outside Ireland / relocation required — too far

## Date Filter

Only include jobs posted within the last 14 days, or with an application deadline that has not yet passed. If a posting date cannot be determined, include it but flag as "date unknown".

## Adapting Queries

If the user specifies a focus area, select queries from the matching category and also generate 2-3 custom queries for that focus. For example:
- "/scrape [focus_area]" -> relevant category queries + custom focus-specific queries
