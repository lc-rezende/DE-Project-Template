DE-Project-Template is a data engineering project template for organizing pipelines, data tiers, and operational tooling.

Disclaimer: This structure was created using OpenAI Codex CLI.

Root Files:
- `.env.example`: Template of environment variables to copy into a local .env file (no secrets).
- `.gitignore`: Git ignore rules for virtual environments, data outputs, and local-only files.
- `.python-version`: Root-level file used by project tooling or documentation.
- `README.md`: Project overview, structure index, and repository guidance for contributors.
- `pyproject.toml`: Project metadata, dependency definitions, and tooling configuration for uv and Python.

Folders:
- `analytics`: Analyst-focused assets such as BI extracts, analysis specifications, and exploratory analysis outputs that are not production pipelines.
- `artifacts`: Build and run outputs such as compiled bundles, export packages, and generated delivery files ready for downstream use.
- `ci`: Continuous integration definitions, build scripts, and automation metadata used by the CI system.
- `configs`: Environment- and service-specific configuration files, connection profiles, and parameter defaults used by pipelines and tools.
- `data`: Root for all dataset storage tiers, organized by lifecycle stage and processing maturity.
- `data/curated`: Business-ready, validated datasets tailored for specific domains or products.
- `data/external`: Reference datasets and third-party inputs maintained outside primary ingestion pipelines.
- `data/interim`: Intermediate transformation outputs used to bridge raw inputs to processed models.
- `data/processed`: Cleaned and standardized datasets suitable for general analytical consumption.
- `data/raw`: Immutable raw ingestions exactly as received from source systems, with no transformations applied.
- `docker`: Container build contexts and related assets for local and production runtime images.
- `docs`: Project documentation such as architecture notes, onboarding guides, and operational runbooks.
- `experiments`: Temporary research and prototype work used to evaluate approaches before productionization.
- `infra`: Infrastructure as code, provisioning templates, and deployment descriptors for platform resources.
- `logs`: Operational and pipeline log outputs stored for debugging and auditing.
- `metadata`: Data catalog metadata, schema definitions, lineage references, and governance artifacts.
- `models`: Logical data model definitions, entity relationship references, and domain modeling assets.
- `monitoring`: Monitoring and alerting configurations, dashboards, and SLO definitions for pipeline health.
- `notebooks`: Jupyter and exploratory notebooks used for analysis, prototyping, and investigation.
- `pipelines`: Root directory for orchestrated workflows and tool-specific pipeline implementations.
- `pipelines/airflow`: Airflow DAGs, plugins, and configuration supporting Airflow-based orchestration.
- `pipelines/dagster`: Dagster pipelines, assets, resources, and configuration for Dagster-based orchestration.
- `pipelines/dbt`: dbt project assets including models, macros, snapshots, and configuration.
- `pipelines/orchestration`: Cross-tool orchestration assets such as schedules, triggers, and shared workflow utilities.
- `pipelines/spark`: Spark jobs, configurations, and related assets for distributed processing pipelines.
- `references`: External references, vendor docs, and supporting materials needed for implementation.
- `reports`: Generated reports and deliverables intended for stakeholders and business users.
- `scripts`: Operational scripts and utilities for local development, data ops, and maintenance tasks.
- `sql`: Reusable SQL queries, views, and migration scripts shared across pipelines and analyses.
- `tests`: Test suites, fixtures, and validation assets for data quality and pipeline correctness.
- `tmp`: Scratch space for transient files that should not be committed or relied upon.
