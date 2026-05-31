# Troubleshooting GitHub Search

GitHub search is powerful, but it can get noisy fast. Use this guide when your results are too broad, too narrow, stale, weird, or full of tutorial sludge.

---

## Problem: The results are too broad

### Fix: Add technical specificity

Too broad:

```txt
machine learning
```

Better:

```txt
language:python ("pytorch" OR "tensorflow" OR "scikit-learn")
```

Stronger:

```txt
language:python ("torch.nn" OR "transformers") ("attention" OR "fine-tuning")
```

---

## Problem: The results are too narrow

### Fix: Remove one constraint at a time

Too narrow:

```txt
language:systemverilog "UVM" "PCIe" "San Diego" pushed:>2025-01-01 stars:>50
```

Try loosening in this order:

1. Remove location
2. Remove stars
3. Expand keywords with `OR`
4. Remove recency temporarily
5. Search repositories instead of users

Broader:

```txt
language:systemverilog ("UVM" OR "PCIe")
```

---

## Problem: Results are stale

### Fix: Add recency filters

For repositories:

```txt
pushed:>2025-01-01
```

For pull requests:

```txt
merged:>2025-01-01
```

For issues or PR activity:

```txt
updated:>2025-01-01
```

---

## Problem: Too many forks

Forks can be useful, but they can also create noise.

Try:

```txt
fork:false
```

Or, when you specifically want forks:

```txt
fork:true
```

If you are using code search, check the current GitHub docs because fork behavior differs by search surface.

---

## Problem: Too many tutorials

### Fix: Exclude obvious tutorial language

```txt
language:python "pytorch" NOT tutorial NOT course NOT homework
```

Also watch for:

- `awesome-*` lists
- bootcamp projects
- classroom assignments
- copied examples
- vendor demo repos

Tutorials are not useless, but they should not be treated the same as deeper project work.

---

## Problem: You are not finding people

### Fix: Search for work first

Instead of starting with user search:

```txt
location:"Austin" "rust"
```

Start with repos or code:

```txt
language:rust ("tokio" OR "async" OR "systems") pushed:>2025-01-01
```

Then inspect:

- Contributors
- Commit history
- Pull requests
- Maintainers
- Linked personal sites
- README credits

GitHub is often better at surfacing work than surfacing profiles.

---

## Problem: The search string looks right but results are bad

### Fix: Switch search type

You may be searching the wrong surface.

| If you want... | Search this |
|---|---|
| Projects | Repositories |
| Implementation evidence | Code |
| Recent contributors | Pull requests |
| Maintainers / helpers | Issues |
| Profile/location info | Users |

Example:

If repository search for `"torch.nn"` is weak, try code search instead.

---

## Problem: You have too many synonyms

### Fix: Cluster terms by concept

Messy:

```txt
python pytorch tensorflow keras sklearn huggingface transformers rag ml ai llm
```

Cleaner:

```txt
language:python ("pytorch" OR "tensorflow" OR "scikit-learn")
```

Then run a separate query for LLM work:

```txt
language:python ("huggingface" OR "transformers" OR "RAG")
```

Do not make one mega-string do every job.

---

## Problem: You are getting keyword matches without real skill evidence

### Fix: Search for implementation fingerprints

Generic:

```txt
"machine learning"
```

More evidence-based:

```txt
"torch.nn" language:python
```

Generic:

```txt
"verification engineer"
```

More evidence-based:

```txt
language:systemverilog ("scoreboard" OR "covergroup" OR "assert property")
```

---

## Problem: The hiring manager gave you vague terms

### Fix: Use GitHub to build the vocabulary map

Start broad:

```txt
"high speed interconnect"
```

Then collect related terms from results:

- PCIe
- SerDes
- PAM4
- 400G / 800G
- DSP
- RTL
- SystemVerilog
- signal integrity

Then build a better query:

```txt
("serdes" OR "PAM4" OR "PCIe" OR "800G") ("RTL" OR "SystemVerilog" OR "DSP")
```

---

## Problem: GitHub has no results for the exact role

### Fix: Search adjacent technical evidence

Some roles do not show up cleanly on GitHub.

For example, physical design engineers may not publish production work publicly. Search for adjacent signals instead:

```txt
("OpenROAD" OR "OpenLane" OR "Yosys")
```

```txt
("timing closure" OR "static timing analysis" OR "place and route")
```

You may use GitHub less for direct candidate finding and more for market vocabulary, project context, and sourcing calibration.

---

## Problem: You found a good repo but not candidate leads

### Fix: Inspect the repo graph

Look at:

- Contributors
- Commit authors
- Pull requests
- Issue commenters
- Forks
- Stargazers, when useful
- Linked organizations
- README credits
- Maintainer docs

One good repo can become a sourcing map.

---

## Best practice: save your iterations

Keep a simple search log:

| Search string | What worked | What was noisy | Next version |
|---|---|---|---|
| `language:python "pytorch"` | Found broad ML repos | Too many tutorials | Add `"torch.nn"` and recency |

The goal is not one perfect search. The goal is a repeatable search path.
