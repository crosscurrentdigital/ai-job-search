# Search Queries for Job Scraper

## Installed portal CLIs (primary for `/scrape`)

`/scrape` discovers every portal skill under `.agents/skills/*/SKILL.md` and runs its CLI first. Shipped country-agnostic CLIs include `linkedin-search` and `freehire-search`.

**Note:** Claton is US/South Dakota-based, so the Danish portal demos (`jobindex-search`, `jobbank-search`, `jobdanmark-search`, `jobnet-search`) do not apply to this market and should be skipped. Use `linkedin-search` and `freehire-search`, plus the WebSearch fallback queries below. Use `/add-portal` if a US-market portal CLI (e.g. Indeed) is wanted later.

The `site:` query templates in this file are the **WebSearch fallback** — for portals without a CLI, company career pages, or when a CLI fails.

## Search Sites

Primary:
- **indeed.com** - largest general US job board
- **linkedin.com/jobs** - LinkedIn job listings (filter: United States / remote); also covered by `linkedin-search` CLI
- **christianjobs.com** - niche board for faith-based/ministry-adjacent roles
- **weworkremotely.com** - remote-first roles, good fit for AI-first builder positions

Secondary (company career pages via Google):
- Direct Google searches with `site:` filters for known target companies (e.g. Hallow)

## Query Categories

### Priority 1: AI Transformation / AI-First Builder Roles

These match Claton's strongest and most desired career direction.

```
site:indeed.com "AI Transformation Lead" remote
site:indeed.com "AI Solutions Architect" remote
site:linkedin.com/jobs "AI Transformation" OR "AI Implementation Lead" remote
site:linkedin.com/jobs "Head of AI" OR "AI Strategy Lead" remote
```

### Priority 2: Faith-Based / Mission-Driven Organizations

These match Claton's strongly preferred target sector.

```
site:christianjobs.com "AI" OR "technology" OR "digital"
site:indeed.com "AI" "Christian" OR "faith-based" OR "ministry" remote
site:linkedin.com/jobs "AI" ministry OR nonprofit OR "faith-based" remote
```

### Priority 3: Adjacent Roles (Staff Engineer / Fractional CTO)

Adjacent roles Claton could pivot into.

```
site:indeed.com "Staff Engineer" "rapid prototyping" remote
site:indeed.com "Fractional CTO" AI remote
site:linkedin.com/jobs "Staff Engineer" "AI-first" remote
```

### Priority 4: Broader AI Consulting / Builder (full-time, part-time, or contract)

Wider net for general AI-first technical/consulting roles. Claton is open to part-time and contract/consulting work, not just full-time - part-time/contract pay is not expected to hit the $80k+ full-time floor, so don't filter these out on salary alone.

```
site:indeed.com "AI consultant" remote
site:linkedin.com/jobs "AI builder" OR "applied AI engineer" remote
site:linkedin.com/jobs "AI consultant" contract OR "part-time" remote
site:weworkremotely.com AI
```

### Priority 5: Denominational / Church Organization Roles

```
site:christianjobs.com "director of technology" OR "digital ministry" OR AI
site:linkedin.com/jobs "denominational" OR "conference office" OR "district office" technology remote
```

### Long-Shot Passion Search: Baseball Organizations

Low-priority, run occasionally rather than every scrape. Claton is a lifelong baseball fan and would take a fitting technical/AI role with a minor or major league organization if one ever surfaced, though this is recognized as a long shot given the career background.

```
site:teamworkonline.com AI OR technology OR "product"
site:linkedin.com/jobs "AI" OR "technology" "minor league baseball" OR "MiLB"
site:linkedin.com/jobs "AI" OR "technology" "major league baseball" OR "MLB"
```

## Location Filter

When evaluating results, verify the job is remote or within Rapid City, SD. Define acceptable areas:
- Remote (United States) - ideal
- Rapid City, SD and surrounding areas - acceptable (on-site/hybrid)
- Anywhere else on-site or requiring relocation - too far (deal-breaker, exclude)

## Date Filter

Only include jobs posted within the last 14 days, or with an application deadline that has not yet passed. If a posting date cannot be determined, include it but flag as "date unknown".

## Adapting Queries

If the user specifies a focus area, select queries from the matching category and also generate 2-3 custom queries for that focus. For example:
- "/scrape [focus_area]" -> relevant category queries + custom focus-specific queries

## Target Companies to Monitor

- **Hallow** (already applied to an AI Transformation Lead-type role, ~$120k-$200k) - check for additional openings or status
