# GitHub Search Types Guide

GitHub has multiple search surfaces. The same idea can behave differently depending on whether you search repositories, code, issues, pull requests, users, discussions, commits, or topics.

The practical question is not "What can GitHub search?" It is "Where does the signal I need actually live?"

---

## Quick comparison

| Search type | Best for | Example |
|---|---|---|
| Repository search | Finding projects, tech stacks, topics, active repos | `topic:machine-learning stars:>100 pushed:>2025-01-01` |
| Code search | Finding exact implementation evidence | `"torch.nn" language:python` |
| Issue search | Finding maintainers, triagers, community support, problem solving | `is:issue label:bug commenter:USERNAME` |
| Pull request search | Finding contributors, reviewers, merged work, collaboration | `is:pr is:merged merged:>2025-01-01` |
| User search | Finding people by profile-level signals | `location:"San Diego" language:python` |
| Discussion search | Finding community knowledge and participation | `"architecture" "kubernetes"` |
| Topic search | Finding technology communities and repo clusters | `topic:llm` |

---

## Repository search

Use repository search when you want to find projects.

Good for:

- Technology ecosystems
- Active repos
- Open-source projects
- Topic clusters
- Repos by language
- Repos by stars, forks, or recency

Examples:

```txt
topic:machine-learning stars:>100 pushed:>2025-01-01
```

```txt
language:go "kubernetes" stars:>50
```

```txt
language:systemverilog "UVM"
```

Repository search is often the best starting point for talent intelligence because it reveals where work is happening before you narrow in on people.

---

## Code search

Use code search when you want evidence that a concept appears in actual implementation.

Good for:

- Exact phrases
- API usage
- Framework evidence
- File path patterns
- Language-specific implementation
- Technical fingerprints

Examples:

```txt
"torch.nn" language:python
```

```txt
"assert property" language:systemverilog
```

```txt
"FreeRTOS" language:c
```

Code search is high-signal when you know the exact technical phrase, function, library, or pattern you want.

---

## Issue search

Use issue search when you want to understand collaboration, maintenance, support, or problem-solving behavior.

Good for:

- Maintainers
- Bug triage
- Product thinking
- Community support
- People who explain technical problems clearly

Examples:

```txt
is:issue label:bug "kubernetes"
```

```txt
is:issue commenter:USERNAME
```

```txt
is:issue "memory leak" language:go
```

Issue search can be especially useful when technical communication matters as much as code.

---

## Pull request search

Use pull request search when you want contribution evidence.

Good for:

- Recent contributors
- Merged work
- Review behavior
- Collaboration patterns
- Maintainer activity

Examples:

```txt
is:pr is:merged merged:>2025-01-01
```

```txt
is:pr author:USERNAME
```

```txt
is:pr reviewed-by:USERNAME
```

```txt
is:pr "kubernetes" merged:>2025-01-01
```

Pull requests can be one of the strongest GitHub signals because they show work moving through review and merge paths.

---

## User search

Use user search when you want profile-level discovery.

Good for:

- Location signals
- Profile keywords
- Language signals
- Username/name matching

Examples:

```txt
location:"San Diego" language:python
```

```txt
location:"Austin" language:rust
```

```txt
"machine learning" location:"New York"
```

User search is useful, but do not over-rely on it. Many strong engineers have sparse GitHub profiles. The work may be richer than the bio.

---

## How to choose the right search type

Ask yourself:

| Question | Search where? |
|---|---|
| Do I need projects? | Repositories |
| Do I need exact implementation evidence? | Code |
| Do I need recent contributors? | Pull requests |
| Do I need maintainers or support behavior? | Issues |
| Do I need profile/location signals? | Users |
| Do I need technology communities? | Topics |

---

## Recommended recruiter flow

```txt
1. Repository search to find relevant projects
2. Code search to validate technical specificity
3. PR search to identify contributors
4. Issue search to understand collaboration and maintenance
5. User/profile review to collect contact and context clues
6. Cross-reference outside GitHub
```

Start broad enough to learn the market, then narrow based on what the results teach you.
