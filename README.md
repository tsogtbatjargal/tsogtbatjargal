# Hi, I'm Tsogt

Data engineer in Calgary, AB. I build data platforms end to end: ingestion, warehouse, quality checks, CI/CD and the infrastructure underneath. Before that I spent a decade at Rio Tinto's Oyu Tolgoi mine in IT/OT, process automation and analytics engineering.

Most recently I was the only data engineer at Summit Lithium Technologies, where I built and ran the Airflow and Snowflake data platform and rebuilt the compute platform behind the company's digital twin. That code is private, so the write-ups are on [tsogtb.com](https://tsogtb.com).

## Projects

| Project | What it is | Stack |
|---|---|---|
| [energy-curve-platform](https://github.com/tsogtbatjargal/energy-curve-platform) | WTI and Brent price curves from public EIA data, published as versioned datasets with threshold alerts. [Case study](https://tsogtb.com/projects/energy-curve-platform/) · [Demo](https://youtu.be/amHBwjYUsYE) | Python, Polars, Postgres, AWS Step Functions, Glue, Redshift, Terraform |
| [bedoux-databricks](https://github.com/tsogtbatjargal/bedoux-databricks) | Two medallion pipelines on Databricks Free Edition with contracts, tests, CI/CD and Genie spaces. [Case study](https://tsogtb.com/projects/bedoux-databricks/) | Databricks, Delta Lake, PySpark, Unity Catalog, GitHub Actions |
| [bedoux-commerce-cloud-gitops](https://github.com/tsogtbatjargal/bedoux-commerce-cloud-gitops) | A commerce app taken from Docker Compose to a cost-capped EKS cluster with Helm, Terraform and Argo CD. [Case study](https://tsogtb.com/projects/bedoux-eks/) | Kubernetes, Helm, Terraform, AWS, FastAPI, React |
| [qr-simple](https://github.com/tsogtbatjargal/qr-simple) | Equipment tracking by QR code for field operators. [Live](https://qr-simple.fly.dev) · [Case study](https://tsogtb.com/projects/qr-simple/) | ASP.NET Core, Blazor, PostgreSQL, Fly.io |

## Agentic software factory

I run a small software factory for Cashmify (rebranded from Bedoux), a private operations platform I build and operate. Coding agents write the code. I own the specs, the reviews, the merges and the releases. The repos are private, so this is the short version.

| Step | How it works | What keeps it safe |
|---|---|---|
| Idea → spec | An agent interviews me, then writes the spec and decision records as a PR | I confirm every one-way decision myself |
| Spec → issues | Small slices, each with acceptance criteria and plain "try it" steps | Agents only pick up issues I've labelled ready |
| Build | Claude Code sessions on an isolated VM, each in its own git worktree, started from my terminal or from Telegram | The builder has its own GitHub account, no sudo, and root-owned git hooks that block pushes to `main` |
| Review | CI, then a fresh agent session reviews each PR against written rules | Only I merge |
| Release | Argo CD deploys `main` to staging on k3s, where the business owner tries every screen | Prod on AWS follows owner-signed release tags only |

Underneath: TypeScript and PostgreSQL for the platform; Terraform, k3s, Argo CD, SOPS-encrypted secrets and OIDC image pushes for the infrastructure; nightly encrypted backups with a tested restore. A delivery board is generated from issue labels, so it can't drift from the real state.

Builder commits carry a co-author line, which is why this account shows activity in private repos. The same habits are public in [qr-simple](https://github.com/tsogtbatjargal/qr-simple): built with an agent, test-first, with an `AGENTS.md` handoff file.

## Day-to-day stack

Snowflake · Airflow · Azure (Data Factory, Functions, Blob/ADLS, DevOps) · Python · SQL · Terraform · CI/CD · Linux

Personal-project experience, not production: Databricks/Spark, AWS (Glue, Redshift, Step Functions), Kubernetes.

## Contact

[tsogtb.com](https://tsogtb.com) · [Book a 15 minute call](https://tsogtb.com/book/) · [LinkedIn](https://www.linkedin.com/in/tsogt-batjargal/)
