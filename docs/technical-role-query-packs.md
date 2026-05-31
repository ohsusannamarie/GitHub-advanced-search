# Technical Role Query Packs

These are starter query packs by role family. Treat them as sourcing hypotheses, not finished answers.

Use them to:

- Calibrate with hiring managers
- Find technical vocabulary
- Identify repos, contributors, and projects
- Build repeatable sourcing paths
- Create Boolean strings for other platforms

---

## AI / ML Engineer

### Core ML frameworks

```txt
language:python ("pytorch" OR "tensorflow" OR "scikit-learn") pushed:>2025-01-01
```

### Transformers / LLMs

```txt
language:python ("transformers" OR "attention" OR "fine-tuning" OR "LoRA")
```

### Hugging Face ecosystem

```txt
language:python ("huggingface" OR "transformers" OR "datasets")
```

### RAG / vector search

```txt
language:python ("RAG" OR "retrieval augmented generation" OR "vector database" OR "embeddings")
```

### MLOps

```txt
("mlflow" OR "kubeflow" OR "model registry" OR "feature store") language:python
```

---

## Data Engineer

### Airflow / orchestration

```txt
language:python ("airflow" OR "dag" OR "data pipeline")
```

### dbt / analytics engineering

```txt
("dbt" OR "data build tool") language:sql
```

### Spark / Databricks

```txt
("spark" OR "pyspark" OR "databricks") language:python
```

### Snowflake

```txt
"snowflake" ("warehouse" OR "schema" OR "pipeline")
```

---

## ASIC / RTL Engineer

### RTL design

```txt
("RTL" OR "register transfer level") ("Verilog" OR "SystemVerilog")
```

### Verilog

```txt
language:verilog ("pipeline" OR "state machine" OR "fifo")
```

### SystemVerilog

```txt
language:systemverilog ("interface" OR "modport" OR "clocking block")
```

### PCIe / interconnect

```txt
("PCIe" OR "PCI Express" OR "AXI" OR "NoC") ("RTL" OR "SystemVerilog")
```

---

## Verification Engineer

### UVM

```txt
language:systemverilog ("UVM" OR "universal verification methodology")
```

### Testbench

```txt
language:systemverilog ("testbench" OR "scoreboard" OR "sequence" OR "sequencer")
```

### Functional coverage

```txt
language:systemverilog ("functional coverage" OR "covergroup" OR "coverpoint")
```

### Assertions

```txt
language:systemverilog ("assert property" OR "SVA" OR "SystemVerilog assertions")
```

---

## Physical Design Engineer

GitHub may be less rich for physical design than software roles, so use GitHub to map vocabulary and adjacent open-source tooling.

### Timing closure / STA

```txt
("timing closure" OR "static timing analysis" OR "STA")
```

### Place and route

```txt
("place and route" OR "floorplan" OR "floorplanning")
```

### OpenROAD ecosystem

```txt
("OpenROAD" OR "OpenLane" OR "Yosys")
```

### EDA scripting

```txt
("Tcl" OR "EDA" OR "synthesis") ("timing" OR "floorplan")
```

---

## Embedded Systems Engineer

### Embedded C

```txt
language:c ("embedded" OR "firmware" OR "microcontroller")
```

### RTOS

```txt
language:c ("FreeRTOS" OR "RTOS" OR "Zephyr")
```

### Device drivers

```txt
("device driver" OR "driver") language:c
```

### ARM / MCU

```txt
("ARM" OR "STM32" OR "Cortex-M") language:c
```

---

## Security Engineer

### AppSec

```txt
("OWASP" OR "XSS" OR "SQL injection" OR "CSRF")
```

### Detection engineering

```txt
("sigma rules" OR "yara" OR "suricata" OR "snort")
```

### Vulnerability research

```txt
("CVE" OR "exploit" OR "proof of concept") language:python
```

### Cloud security

```txt
("IAM" OR "cloud security" OR "least privilege") ("AWS" OR "GCP" OR "Azure")
```

---

## DevOps / Platform Engineer

### Kubernetes

```txt
("kubernetes" OR "k8s") language:go pushed:>2025-01-01
```

### Terraform

```txt
language:hcl "terraform"
```

### Observability

```txt
("prometheus" OR "grafana" OR "opentelemetry")
```

### CI/CD

```txt
("GitHub Actions" OR "Jenkins" OR "CircleCI" OR "ArgoCD")
```

---

## Backend Engineer

### Go services

```txt
language:go ("grpc" OR "microservice" OR "api") pushed:>2025-01-01
```

### Java / Spring

```txt
language:java ("spring boot" OR "microservices")
```

### Node / API

```txt
language:typescript ("express" OR "nestjs" OR "api")
```

### Distributed systems

```txt
("distributed systems" OR "consensus" OR "raft" OR "event-driven")
```

---

## Frontend Engineer

### React / TypeScript

```txt
language:typescript ("react" OR "next.js" OR "vite")
```

### Design systems

```txt
("design system" OR "storybook" OR "component library") language:typescript
```

### Accessibility

```txt
("a11y" OR "accessibility" OR "ARIA") language:typescript
```

---

## How to adapt a query pack

For each role, adjust:

| Dimension | Add this kind of filter |
|---|---|
| Recency | `pushed:>2025-01-01` |
| Language | `language:python`, `language:go`, `language:systemverilog` |
| Community signal | `stars:>50`, `forks:>10` |
| Organization | `org:ORGNAME` |
| User | `user:USERNAME` |
| Exact phrase | `"timing closure"` |
| Alternatives | `("PCIe" OR "AXI" OR "NoC")` |

---

## False positive watchlist

Common noise patterns:

- Coursework
- Tutorials
- Forks with no original contribution
- Archived repos
- Old projects with no recent activity
- Vendor examples copied into personal repos
- Keyword stuffing in README files

Use GitHub search as the first pass. Human judgment still gets the final vote.
