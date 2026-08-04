---
framework_version: 1.1.0
---

# Job Evaluation Framework

<!-- SETUP: Skill match areas and career goals are personalized by running /setup -->

**Candidate work authorization on file: U.S. citizen.** No eligibility-gate concerns for US-based roles; skip straight to scoring for domestic postings. Still check this section for any role that names a security-clearance requirement or a non-US jurisdiction.

## Eligibility Gate — run before scoring

If the candidate is not a citizen or permanent resident of the country they are applying in, run this first. It is a hard filter, not a scoring dimension, and it is separate from work-permit *timing*: timing asks "can they work the required hours yet?", eligibility asks "are they permitted to hold this job at all?". A candidate can pass timing and still be categorically excluded.

Read the posting's eligibility / work rights / "who can apply" section **verbatim** and classify:

| Posting wording | Verdict |
|-----------------|---------|
| Names a **citizenship or permanent-residency requirement** ("must be a citizen of X", "permanent resident", "PR required", "full working rights" where the employer means citizen/PR) | **FAIL — hard stop.** Do not score, do not draft. Quote the exact wording back to the user. |
| Requires a **security clearance** at any level | **FAIL** in most countries, since clearance is normally gated on citizenship. Verify the specific scheme rather than assuming. |
| **Explicitly names** the candidate's permit class, or says "international applicants welcome", "visa holders considered", "we sponsor" | **PASS** — verified acceptance. Worth noting as a positive in the application. |
| **Silent** on citizenship or residency | **PROCEED, but mark unverified.** Check the employer's own careers or international-applicant page before drafting. |

**Two rules that are easy to get wrong:**

1. **Silence is not permission.** Large graduate programs frequently gate eligibility on their own website rather than in the job ad. Highest-risk categories: professional-services firms, government and defence, banking, telecommunications, and anything touching critical infrastructure.
2. **A company-wide "we accept international applicants" statement is not role-level permission.** The common pattern is a general welcome followed by a *named list* of the specific programs or service lines it covers. Confirm the **specific posting or stream** appears on that list before drafting.

**Report an eligibility failure to the user with the quoted source** rather than silently dropping the role. They may know something about their own status that the profile does not record.

If the candidate's permit also constrains *hours* or *start date* (a student visa with a term-time cap, a permit that begins on graduation), record that as a second gate under this section during `/setup`, with the specific dates. Do not merge it with the eligibility question above — they fail for different reasons and need different answers.

A role that fails this gate is not scored and not drafted. Everything below applies only to roles that pass it.

## Scoring Dimensions

Evaluate each job posting against these five dimensions:

### 1. Technical Skills Match (0-100)
How well do the required/preferred skills align with the candidate's capabilities?

| Score | Meaning |
|-------|---------|
| 80-100 | Core requirements are primary skills |
| 60-79 | Most requirements match, 1-2 gaps that are learnable |
| 40-59 | Partial match, significant upskilling needed |
| 0-39 | Fundamental mismatch |

**Strong match areas:** AI-assisted rapid development (Claude Code, Claude API, Cursor), full-cycle product/technical architecture, faith-based/Christian sector domain knowledge, bootstrapped multi-entity business operations
**Moderate match areas:** Formal engineering leadership at corporate scale (has led volunteers and retail staff, not large engineering orgs), enterprise process/compliance-heavy environments
**Weak match areas:** Deep classical software engineering/CS-theory background (no formal CS degree; skills are self-taught via AI-assisted tooling), large bureaucratic enterprise environments

### 2. Experience Match (0-100)
Does work history align with what they're looking for?

| Score | Meaning |
|-------|---------|
| 80-100 | Direct experience in the same domain and role type |
| 60-79 | Related experience, transferable skills clear |
| 40-59 | Adjacent experience, would need to make the case |
| 0-39 | Unrelated experience |

**Strong:** Building and shipping software products end-to-end with AI-assisted tools; Christian publishing/media operations; auditing workflows to find where AI/automation helps; direct experience teaching AI adoption to small business owners (runs a two-part workshop series on email/task triage and second-brain/marketing-agent workflows, using his own products as the working examples)
**Moderate:** People development and process training at scale (Vitamin World: promoted staff with no prior experience up to management level across ~10 stores); church/ministry leadership and volunteer coordination
**Entry-level:** N/A

### 3. Behavioral/Culture Fit (0-100)
Does the role and company culture match the behavioral profile?

| Score | Meaning |
|-------|---------|
| 80-100 | Culture strongly matches behavioral preferences |
| 60-79 | Mixed signals but mostly compatible |
| 40-59 | Some friction areas |
| 0-39 | Significant culture mismatch |

**Red flags to research:** Department disorganization, work dominated by maintenance over development, poor chemistry with leadership, culture mismatches. Check reviews, media coverage, LinkedIn connections, and network contacts for insider perspective.

### 4. Location & Logistics (Pass/Fail + Notes)
- Within commute range: PASS
- Remote with occasional office: PASS
- Requires relocation: FAIL (deal-breaker)
- Frequent international travel: FLAG (discuss with user)
- Amazon or an Amazon subsidiary: FAIL (hard exclude, see CLAUDE.md "Companies to Exclude")
- No health/dental insurance or PTO offered (full-time roles only): FLAG - weigh alongside salary, not just a nice-to-have
- Notice period: candidate can start within about a week of an offer; flag any role with an unusually fast or unusually slow expected start against that, and note the family-visit window (mid-August through start of September 2026) if scheduling falls there

### 5. Career Alignment & Motivation (0-100)
Does this role advance career goals and contain tasks that energize?

| Score | Meaning |
|-------|---------|
| 80-100 | Strongly aligned with career direction, clear growth path |
| 60-79 | Good role but only partially aligned with long-term goals |
| 40-59 | Decent job but doesn't build toward career goals |
| 0-39 | Dead end or backwards step |

**Career goals:**
- Move into an employed role (not another founder venture) at a mission-driven or faith-based organization - open to full-time, part-time, contract/consulting, or denominational-organization roles
- Serve as an AI transformation lead/consultant/builder: audit current services and procedures, identify where AI can help, build custom AI solutions, and guide the organization through adoption so AI is genuinely helpful rather than a burden or source of confusion
- For full-time roles, land in the $120k-$200k range (absolute floor: $80k); part-time/contract work is evaluated on whether the pay is genuinely worthwhile for the time, not against the $80k floor
- Long-shot passion sector: a minor or major league baseball organization, if a fitting technical/AI role ever appears

**Motivation filter:** Evaluate not just whether you *can* do the tasks, but whether the tasks will *energize* you. Consider:
- Tasks that energize: Building and shipping things, solving concrete problems, rapid AI-assisted prototyping, turning a messy process into a working AI-assisted solution
- Tasks that drain: *[Not yet directly confirmed by the candidate - infer cautiously: pure maintenance work with no building component, highly bureaucratic committee-driven decision-making. Verify with the candidate before treating as a scoring input.]*
- Non-task factors: must be able to genuinely stand behind the organization's mission and values (near-mandatory for faith-based/Christian-organization targets); autonomy over execution once a decision is made

**Life situation alignment:** Consider personal constraints:
- **Security**: Currently self-employed running multiple ventures (Crucible Lab, 102:18 INC, Two Words Publishing group). Steady, predictable income is now a high priority - family is in the process of adopting another child, which raises the weight on stable full-time employment over further founder-style risk. *(Internal fit-evaluation context only - never surface family/adoption details in a CV or cover letter.)* Operationally, day-to-day work on the publishing companies and CrossCurrent Digital is already handled by a contract worker (via ClickUp, custom software, and OrganizeMe.click), so those ventures do not require his ongoing hands-on time and do not block taking on a full-time role.
- **Flexibility**: Remote-only, or on-site/hybrid in Rapid City, SD; not open to relocation. Actively looking to move away from the grueling, self-imposed hours of solo-founder work toward a sustainable workload - weight roles with reasonable hours and healthy boundaries higher, and flag postings that signal always-on/crunch culture
- **Professional development**: Wants to grow further into AI transformation/builder work at a mission-aligned organization, ideally with more structural support (team, process) than solo founding provides

## Calibration from Past Applications
- Applied to **Hallow** for an AI Transformation Lead-type role (~$120k-$200k); outcome not yet known. Treat this as a reference example of an ideal-fit target role and title when scoring similar postings.
- **Organization size preference:** Mid-size orgs and startups/small teams are the primary target, but large enterprise is genuinely open too - the deciding factor is the role's nature, not company size. **Hallow** (large-scale, already applied to) is the candidate's own reference example of a great fit, so company size alone is not a scoring signal - what matters is whether the role itself is hands-on/builder-focused versus multi-year corporate governance-program administration (see Cordia note below).
- **Enterprise-scale "Transformation Lead" postings are a poor fit, even when the title matches.** A `/scrape` result for Cordia's "Principal AI Transformation Lead" (8-12+ years IT/data/digital-transformation experience, cross-functional program leadership, proven track record standing up governance programs) was flagged by the candidate as exceeding his actual qualifications - his background is hands-on solo-founder building and small-business AI audits, not multi-year corporate governance-program leadership at large-enterprise scale. When scoring: a posting titled "AI Transformation Lead" that also asks for "Principal"-level seniority, a specific multi-year corporate tenure requirement, or standing up formal governance programs across a large enterprise should score **lower on Experience Match** than the title alone suggests - weight the seniority/scale signals in the requirements text, not just the title match. Better-fit signals: smaller or mid-size organizations, startup-scale AI roles, consulting/fractional engagements, or postings that emphasize hands-on building and audit-then-build work over enterprise program governance.

### 6. Salary Benchmark (Optional)

If the salary lookup tool is configured (`salary_data.json` exists), look up the company:
```
python salary_lookup.py "<Company Name>" --json
```

If a city is known from the posting, add `--city "<City>"` to narrow results.

Present findings as:
```
### Salary Benchmark
| Metric | Value |
|--------|-------|
| [Category] index | XX.X (+/-X.X% vs baseline) |
| Overall index | XX.X (+/-X.X% vs baseline) |
```

Interpret results relative to the baseline defined in the data file's metadata. For index-based data, higher typically means above-market compensation.

If the salary tool is not configured, skip this section.

## Output Format

Present the evaluation as:

```
## Job Fit Evaluation: [Role] at [Company]

| Dimension | Score | Notes |
|-----------|-------|-------|
| Technical Skills | XX/100 | [brief note] |
| Experience Match | XX/100 | [brief note] |
| Behavioral Fit | XX/100 | [brief note] |
| Location | PASS/FAIL | [brief note] |
| Career Alignment | XX/100 | [brief note] |

**Overall Score: XX/100** (weighted average of scored dimensions)

### Verdict: [Strong Fit / Good Fit / Moderate Fit / Weak Fit / Poor Fit]

### Key Strengths for This Role
- [bullet points]

### Gaps to Address
- [bullet points]

### Recommendation
[1-2 sentences: apply/skip/apply with caveats]

### Company Research Checklist
- [ ] Checked company website (mission, values, recent news)
- [ ] Checked review sites (Glassdoor, Jobindex, etc.)
- [ ] Checked LinkedIn for team size, recent hires, connections
- [ ] Checked media for restructuring, growth, or workplace issues
- [ ] Identified network contacts who may know the team/manager
```

## Weighting
- Technical Skills: 30%
- Experience Match: 25%
- Behavioral Fit: 15%
- Career Alignment: 30%

(Location is pass/fail, not weighted)

## Thresholds
- **Strong Fit** (75+): Definitely apply, tailor everything
- **Good Fit** (60-74): Apply, address gaps in cover letter
- **Moderate Fit** (45-59): Consider carefully, discuss with user
- **Weak Fit** (30-44): Probably skip unless strategic reasons
- **Poor Fit** (<30): Skip

## Pre-Application: Call the Employer (Best Practice)

Before writing the application, consider whether the candidate should call the contact person listed in the posting. **Only call if there are substantive questions** - never call just to "be remembered."

### When to Suggest Calling
- The posting has unclear or ambiguous requirements
- It's unclear which competencies are essential vs. nice-to-have
- The role description is vague about day-to-day tasks
- There's a named contact person who invites questions

### Good Questions to Ask
- "What are the primary challenges in this role?"
- "How is time typically divided across the listed responsibilities?"
- "Which competencies are most critical for success in this position?"
- "What does success look like in the first 6-12 months?"

### Rules for the Call
- Prepare a 30-second "elevator pitch" about your background in case they ask
- The call's purpose is **gathering information**, not delivering a pitch
- Take notes - use what you learn to tailor the application
- Reference the conversation naturally in the cover letter ("After speaking with [name], I was especially drawn to...")
