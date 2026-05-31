# GitHub Advanced Search for Talent Sourcing

**A practical GitHub search toolkit for finding technical talent, open-source contributors, technical projects, and real evidence of skill.**

Learning how to search GitHub is not exactly intuitive. It is powerful, weirdly specific, occasionally humbling, and absolutely worth learning if you source technical talent.

This repo turns GitHub's advanced search operators into practical workflows for recruiters, sourcers, talent intelligence teams, OSINT researchers, and curious nerds who want better signal than keyword-stuffed resumes.

Originally created by **Sofia Broberger** and **Susanna Conway** as *The Big List of GitHub Search Operators* plus a cheat sheet. This version expands the project into a more usable sourcing and research toolkit.

---

## What you can do with this

Use this repo to:

- Search GitHub more precisely using operators, qualifiers, and filters
- Find engineers through project evidence, not just profile keywords
- Identify open-source contributors, maintainers, and active builders
- Build stronger sourcing strings for technical roles
- Understand the difference between repository search, code search, issue search, pull request search, and user search
- Translate technical hiring needs into practical GitHub searches

GitHub search can cover repositories, code, issues, pull requests, users, commits, discussions, packages, wikis, and topics. The trick is knowing which search surface to use for the signal you actually need.

---

## Start here

| Resource | Use it when you want to... |
|---|---|
| [GitHub Search Recipes](docs/github-search-recipes.md) | Copy practical search strings by sourcing use case |
| [Recruiter Use Cases](docs/recruiter-use-cases.md) | Understand how GitHub signals map to talent research |
| [Technical Role Query Packs](docs/technical-role-query-packs.md) | Search by role type: AI/ML, ASIC, RTL, embedded, data engineering, security, and more |
| [Search Types Guide](docs/github-search-types.md) | Know when to use repo search vs. code search vs. issues/PRs/users |
| [Troubleshooting GitHub Search](docs/troubleshooting.md) | Fix searches that are too broad, too narrow, stale, or noisy |
| [Original Cheat Sheet PDF](GitHub%20Advanced%20Search%20Cheat%20Sheet.pdf) | Keep a fast reference nearby |
| [Big List PDF](The%20BIG%20List%20of%20GitHub%20Search%20Operators.pdf) | Browse the original operator list |
| [Collaborative XLSX](The%20BIG%20Collaborative%20List%20of%20GitHub%20Search%20Operators.xlsx) | Explore or expand the operator library |

---

## Quick-start searches

### Find active Python machine learning projects

```txt
language:python ("pytorch" OR "tensorflow" OR "scikit-learn") pushed:>2025-01-01
```

### Find LLM / Hugging Face project work

```txt
language:python ("huggingface" OR "transformers" OR "fine-tuning") pushed:>2025-01-01
```

### Find SystemVerilog / UVM examples

```txt
language:systemverilog ("UVM" OR "universal verification methodology")
```

### Find PCIe / RTL project evidence

```txt
("PCIe" OR "PCI Express") ("RTL" OR "Verilog" OR "SystemVerilog")
```

### Find recent merged pull requests

```txt
is:pr is:merged merged:>2025-01-01
```

### Find active repositories by topic

```txt
topic:machine-learning stars:>50 pushed:>2025-01-01
```

### Find contributors in a location signal

```txt
location:"San Diego" language:python
```

---

## GitHub search mindset

Most recruiters search GitHub like it is LinkedIn with worse lighting.

Do not do that.

GitHub is not just a people database. It is an evidence database. The real value is not always in the profile. It is in the repos, code, commits, issues, pull requests, comments, project names, documentation, and technical fingerprints people leave behind.

Think in signals:

| Signal | What it may suggest | Example search |
|---|---|---|
| Recent repo activity | Active hands-on builder | `pushed:>2025-01-01` |
| Niche language | Technical specialization | `language:systemverilog` |
| Domain keyword | Relevant technical context | `"serdes" OR "PCIe" OR "CUDA"` |
| Merged PRs | Contribution credibility | `is:pr is:merged` |
| Issues answered | Maintainer / collaborator behavior | `is:issue commenter:USERNAME` |
| Stars / forks | Community interest or reuse | `stars:>100 forks:>25` |
| Topics | Project category signal | `topic:llm` |

---

## Suggested workflow for sourcing

1. **Start with the technical problem, not the job title.**  
   Search for the language, tool, architecture, framework, or domain signal.

2. **Search repos and code before people.**  
   Repositories often reveal stronger evidence than profiles.

3. **Look for recency.**  
   Add date filters like `pushed:>2025-01-01`, `created:>2024-01-01`, or `merged:>2025-01-01` depending on what you are searching.

4. **Use technical synonyms.**  
   Engineers do not all describe the same skill the same way. Search the ecosystem, not just one keyword.

5. **Cross-reference outside GitHub.**  
   GitHub is a signal source, not the full story. Validate with LinkedIn, portfolios, papers, company pages, conference talks, or other open web sources.

6. **Save the good patterns.**  
   The best GitHub searches are reusable. Build your own query library by role family.

---

## What this repo is not

This is not a magic candidate finder. It will not replace judgment, technical calibration, or human context.

It is a toolkit for asking GitHub better questions.

That matters because better questions produce better sourcing paths.

---

## Good searches start messy

A strong GitHub search usually takes iteration:

```txt
language:python "pytorch"
```

Then sharpen it:

```txt
language:python ("pytorch" OR "torch.nn") ("transformer" OR "attention") pushed:>2025-01-01
```

Then add sourcing context:

```txt
language:python ("pytorch" OR "torch.nn") ("transformer" OR "attention") location:"San Francisco" pushed:>2025-01-01
```

Then check whether you are searching the right surface: repositories, code, users, issues, or pull requests.

---

## Contributing

Have a useful GitHub search string, sourcing workflow, or technical role query pack?

Open an issue or pull request with:

- The role or use case
- The search string
- Why it works
- Any caveats or false positives

Useful contributions are practical, specific, and tested.

---

## Official GitHub search references

- [GitHub Advanced Search](https://github.com/search/advanced)
- [GitHub search syntax documentation](https://docs.github.com/en/search-github)
- [Understanding GitHub Code Search syntax](https://docs.github.com/en/search-github/github-code-search/understanding-github-code-search-syntax)
- [Searching for repositories](https://docs.github.com/en/search-github/searching-on-github/searching-for-repositories)
- [Searching issues and pull requests](https://docs.github.com/en/search-github/searching-on-github/searching-issues-and-pull-requests)

---

## Credit

Created by **Sofia Broberger** and **Susanna Conway**.

Expanded as a practical GitHub sourcing toolkit for recruiters, sourcers, talent intelligence teams, and researchers who like their search strings with a little more substance.
