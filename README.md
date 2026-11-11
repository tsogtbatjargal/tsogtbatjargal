# Hi, I'm Tsogt

Data and platform engineer in Calgary, AB. I turn operational data into numbers people trust, and I build what sits underneath: ingestion, warehouse, quality checks, CI/CD, infrastructure and, lately, the delivery process that lets coding agents work safely. Before that I spent a decade at Rio Tinto's Oyu Tolgoi mine in IT/OT, process automation and analytics engineering.

Most recently I was the only data engineer at Summit Lithium Technologies, where I built and ran the Airflow and Snowflake data platform and rebuilt the compute platform behind the company's digital twin. That code is private, so the write-ups are on [tsogtb.com](https://tsogtb.com).

## Now: Cashmify, a platform built by agents and run by me

Cashmify, the next chapter of Bedoux, is a private operations platform for a small business. Coding agents write the code. I write the specs, merge every change and sign every production release. The repos are private, so the full story is in the [case study](https://tsogtb.com/projects/cashmify/).

| Step | How it works | What keeps it safe |
|---|---|---|
| Idea → spec | An agent interviews me, then writes the spec and decision records | I make every one-way decision myself |
| Spec → issues | Small slices, each with acceptance criteria and plain "try it" steps | Agents only build issues I've labelled ready |
| Build | Coding agents on an isolated machine that reaches only the internet and the code host | Their own identity, no admin rights, and root-owned hooks that block pushes to `main` |
| Review | CI, then a fresh agent session reviews the change against written rules | Only I merge, and only once the latest commit has a review |
| Try it | I promote a commit to staging and the business owner tries every screen | No release while a try-out is open |
| Release | Production deploys only releases I sign, from a repo only I can write to | Any change of the deployed release raises an alert |

When I broke these controls on purpose on staging, one passing test still exposed a gap: a valid signature proves who approved a release, not that deploying it now is right. [How that changed the design →](https://tsogtb.com/projects/cashmify/#breaking-the-release-controls-on-purpose)

Stack: Claude Code · TypeScript · PostgreSQL · k3s · Argo CD · Terraform · AWS · GitHub Actions · SOPS. Nightly encrypted backups, with a restore that has been tested.

Builder commits carry a co-author line, which is why this account shows activity in private repos. The same habits are public in [qr-simple](https://github.com/tsogtbatjargal/qr-simple): built with an agent, test-first, with an `AGENTS.md` handoff file.

## Projects

| Project | What it is | Stack |
|---|---|---|
| [energy-curve-platform](https://github.com/tsogtbatjargal/energy-curve-platform) | WTI and Brent price curves from public EIA data, published as versioned datasets with threshold alerts. [Case study](https://tsogtb.com/projects/energy-curve-platform/) · [Demo](https://youtu.be/amHBwjYUsYE) | Python, Polars, Postgres, AWS Step Functions, Glue, Redshift, Terraform |
| [bedoux-databricks](https://github.com/tsogtbatjargal/bedoux-databricks) | Two medallion pipelines on Databricks Free Edition with contracts, tests, CI/CD and Genie spaces. [Case study](https://tsogtb.com/projects/bedoux-databricks/) | Databricks, Delta Lake, PySpark, Unity Catalog, GitHub Actions |
| [bedoux-commerce-cloud-gitops](https://github.com/tsogtbatjargal/bedoux-commerce-cloud-gitops) | A commerce app taken from Docker Compose to a cost-capped EKS cluster with Helm, Terraform and Argo CD. [Case study](https://tsogtb.com/projects/bedoux-eks/) | Kubernetes, Helm, Terraform, AWS, FastAPI, React |
| [qr-simple](https://github.com/tsogtbatjargal/qr-simple) | Equipment tracking by QR code for field operators. [Live](https://qr-simple.fly.dev) · [Case study](https://tsogtb.com/projects/qr-simple/) | ASP.NET Core, Blazor, PostgreSQL, Fly.io |

## Day-to-day stack

Snowflake · Airflow · Azure (Data Factory, Functions, Blob/ADLS, DevOps) · Python · SQL · Terraform · CI/CD · Linux

Personal-project experience, not production: Databricks/Spark, AWS (Glue, Redshift, Step Functions), Kubernetes.

## Contact

Open to Senior Data Engineer, Data Platform Engineer and DataOps roles in Calgary or remote across Canada.

[tsogtb.com](https://tsogtb.com) · [Book a 15 minute call](https://tsogtb.com/book/) · [LinkedIn](https://www.linkedin.com/in/tsogt-batjargal/)
