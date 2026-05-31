# GitHub Search Recipes

Copy, adapt, and iterate. These are practical starting points for sourcing, recruiting research, talent intelligence, and open-source discovery.

GitHub search works best when you search for evidence first: languages, tools, frameworks, project names, domain terms, issues, pull requests, and repository activity.

---

## Active technical projects

### Active Python machine learning projects

```txt
language:python ("pytorch" OR "tensorflow" OR "scikit-learn") pushed:>2025-01-01
```

### Active LLM projects

```txt
language:python ("huggingface" OR "transformers" OR "fine-tuning" OR "RAG") pushed:>2025-01-01
```

### Active TypeScript projects

```txt
language:typescript stars:>25 pushed:>2025-01-01
```

### Active Rust systems projects

```txt
language:rust ("systems" OR "compiler" OR "runtime") pushed:>2025-01-01
```

---

## Open-source contributor discovery

### Recent merged pull requests

```txt
is:pr is:merged merged:>2025-01-01
```

### Recent PRs mentioning a skill or framework

```txt
is:pr is:merged merged:>2025-01-01 "kubernetes"
```

### Issues answered by a specific user

```txt
is:issue commenter:USERNAME
```

### Pull requests authored by a specific user

```txt
is:pr author:USERNAME
```

---

## Repository quality signals

### Repositories with meaningful community signal

```txt
stars:>100 forks:>25 pushed:>2025-01-01
```

### Recently updated repos in a specific topic

```txt
topic:machine-learning pushed:>2025-01-01 stars:>50
```

### Non-archived repositories

```txt
archived:false pushed:>2025-01-01
```

### Repos created recently

```txt
created:>2025-01-01 stars:>10
```

---

## Location-adjacent people search

GitHub user search is imperfect, but location can still be useful when combined with technical evidence.

### Python users in San Diego

```txt
location:"San Diego" language:python
```

### Rust users in Austin

```txt
location:"Austin" language:rust
```

### ML users in New York

```txt
location:"New York" ("machine learning" OR "ML" OR "AI")
```

---

## Semiconductor and hardware signals

### SystemVerilog / UVM

```txt
language:systemverilog ("UVM" OR "universal verification methodology")
```

### PCIe / RTL

```txt
("PCIe" OR "PCI Express") ("RTL" OR "Verilog" OR "SystemVerilog")
```

### SerDes / high-speed interconnect

```txt
("serdes" OR "serializer deserializer" OR "PAM4" OR "400G" OR "800G")
```

### Physical design

```txt
("physical design" OR "place and route" OR "timing closure" OR "STA")
```

---

## AI / ML signals

### PyTorch implementation evidence

```txt
language:python ("torch.nn" OR "pytorch")
```

### Transformers / attention

```txt
language:python ("transformer" OR "attention") ("pytorch" OR "torch.nn")
```

### RAG projects

```txt
language:python ("RAG" OR "retrieval augmented generation" OR "vector database")
```

### CUDA / GPU work

```txt
("CUDA" OR "cuDNN" OR "GPU kernel") language:cpp
```

---

## DevOps / platform signals

### Kubernetes

```txt
("kubernetes" OR "k8s") language:go pushed:>2025-01-01
```

### Terraform

```txt
language:hcl "terraform" pushed:>2025-01-01
```

### CI/CD

```txt
("GitHub Actions" OR "Jenkins" OR "CircleCI") "pipeline"
```

---

## Security signals

### Security tooling

```txt
("static analysis" OR "vulnerability scanner" OR "SAST") language:go
```

### Detection engineering

```txt
("sigma rules" OR "yara" OR "suricata")
```

### AppSec

```txt
("OWASP" OR "XSS" OR "SQL injection") language:python
```

---

## Search sharpening patterns

### Add recency

```txt
pushed:>2025-01-01
```

### Add community signal

```txt
stars:>50 forks:>10
```

### Add exact phrases

```txt
"timing closure"
```

### Add alternatives

```txt
("RTL" OR "Verilog" OR "SystemVerilog")
```

### Remove noise

```txt
NOT tutorial
```

---

## Reminder

A GitHub search string is a hypothesis. Run it, inspect the results, then adjust. The first search rarely needs to be perfect. It needs to teach you what to try next.
