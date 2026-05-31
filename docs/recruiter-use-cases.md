# Recruiter Use Cases

GitHub is not just a place to find usernames. It is a place to find technical evidence.

For recruiters, sourcers, and talent intelligence teams, the goal is not to memorize every operator. The goal is to know what kind of signal you are looking for and where that signal is likely to live.

---

## 1. Find project evidence before profile evidence

Most sourcing searches start too close to the person. On GitHub, start with the work.

Instead of searching only for:

```txt
location:"San Diego" "machine learning"
```

Try searching for projects first:

```txt
language:python ("pytorch" OR "tensorflow" OR "transformers") pushed:>2025-01-01
```

Then inspect:

- Repository contributors
- Commit history
- Pull requests
- Issues and discussions
- Project documentation
- Linked profiles and websites

Why this works: strong technical candidates may not optimize their GitHub profile for recruiter keywords, but their work can still reveal the signal.

---

## 2. Validate technical alignment

GitHub can help you move from "this person says they know X" to "this person has touched X in the wild."

Useful signals:

| Signal | What to look for |
|---|---|
| Language | Does their work match the role's core language? |
| Frameworks | Are they using the relevant ecosystem? |
| Recency | Is the work current or five years old? |
| Complexity | Is it a tutorial fork, toy project, or meaningful implementation? |
| Collaboration | Do they review, discuss, document, or maintain? |
| Domain vocabulary | Do they use terms specific to the technical area? |

Example:

```txt
language:systemverilog ("UVM" OR "PCIe" OR "AXI")
```

---

## 3. Build technical calibration with hiring managers

GitHub searches are useful even when they do not produce a candidate immediately.

Use searches to ask better calibration questions:

- Is this the right vocabulary?
- Are these the right adjacent skills?
- Which terms are must-have vs. nice-to-have?
- Are there open-source projects or companies that show the right kind of work?
- What would a strong project look like?
- What false positives should we avoid?

Example calibration search:

```txt
("serdes" OR "PAM4" OR "800G") ("RTL" OR "SystemVerilog" OR "signal integrity")
```

Then review sample results with the hiring manager.

---

## 4. Identify open-source contributors

Pull requests and issues can reveal contribution behavior that profiles often miss.

Examples:

```txt
is:pr is:merged merged:>2025-01-01 "kubernetes"
```

```txt
is:issue commenter:USERNAME
```

```txt
is:pr author:USERNAME
```

Look for:

- Meaningful PRs
- Maintainer comments
- Issue triage
- Documentation contributions
- Review behavior
- Consistency over time

A person does not have to maintain a famous project to be high-signal. Small, technical, specific contributions can be more relevant than flashy stars.

---

## 5. Find niche technical language

For hard-to-fill technical roles, niche vocabulary matters.

Instead of searching generic terms like:

```txt
software engineer
```

Search the technical environment:

```txt
("timing closure" OR "static timing analysis" OR "place and route")
```

```txt
("UVM" OR "SystemVerilog" OR "RTL verification")
```

```txt
("CUDA" OR "GPU kernel" OR "cuDNN")
```

This is where GitHub becomes especially useful for talent intelligence. You can map the language of a market before you map the people in it.

---

## 6. Create company or competitor research paths

GitHub can help you understand technical ecosystems around companies, products, and open-source communities.

Search examples:

```txt
org:COMPANY_NAME language:python
```

```txt
"COMPANY_NAME" "kubernetes"
```

```txt
"COMPANY_NAME" "open source" language:go
```

Use this to identify:

- Public repos owned by companies
- Open-source projects connected to target companies
- Contributor overlap
- Technology choices
- Engineering vocabulary

Be careful: not every GitHub signal maps cleanly to employment. Treat this as research, not proof.

---

## 7. Build reusable query libraries

Do not let good searches die in Slack.

Create query packs by role family:

- AI / ML
- Data engineering
- ASIC / RTL
- Verification
- Physical design
- Embedded systems
- Security
- DevOps / platform
- Frontend
- Backend

For each query, capture:

| Field | Example |
|---|---|
| Role | ASIC Verification Engineer |
| Search string | `language:systemverilog ("UVM" OR "PCIe")` |
| Search type | Code search |
| Why it works | Finds implementation-level evidence |
| False positives | Tutorials, coursework, vendor examples |
| Best next step | Inspect contributors and recent commits |

---

## 8. Use GitHub as one signal, not the whole story

GitHub can show evidence of technical work, but it has limits.

Do not assume:

- No GitHub means no skill
- High stars means job fit
- A repo proves employment
- A profile location is current
- A fork means authorship
- A tutorial repo means deep experience

GitHub is strongest when combined with human judgment, technical calibration, and cross-platform research.

---

## Practical sourcing flow

```txt
1. Translate role requirements into technical keywords
2. Search repositories and code for project evidence
3. Identify contributors and maintainers
4. Check recency and depth
5. Cross-reference with LinkedIn / portfolio / personal site
6. Save useful query patterns
7. Share findings with the hiring team
```

The win is not just finding one candidate. The win is building repeatable market intelligence.
