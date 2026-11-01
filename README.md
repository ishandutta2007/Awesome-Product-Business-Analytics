# Awesome-Product-Business-Analytics

# Top Product & Business Analytics Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on Product Analytics, Business Intelligence & Self-Hosted Data Platforms*  
**Last updated: November 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Product & Business Analytics**. These tools enable teams to understand user behavior, measure feature adoption, analyze retention and conversion, and build dashboards that turn raw event data into product and business decisions.

**Examples** include Atlassian Analytics, Mixpanel, Amplitude, Heap, Tableau, Power BI, Looker, ThoughtSpot, Pendo, and Sisense (the category leaders).

**Open-source emphasis**: Product & Business Analytics is a domain where open-source tooling is **genuinely mature and production-proven, but the right choice depends on whether you need product analytics or business intelligence**. **PostHog** is the standout all-in-one product analytics platform—MIT-licensed core, self-hostable, combining product analytics, session replay, feature flags, experiments, surveys, and error tracking on a single event database . **Jitsu** provides the event data pipeline layer—an MIT-licensed Segment alternative that collects events and delivers them to warehouses and SaaS tools with per-minute batching . For business intelligence and dashboards, **Apache Superset** and **Metabase** are the mature open-source BI platforms, connecting to any SQL database for charts and dashboards . The critical caveat: **no single open-source project matches the integrated product analytics + BI experience** of commercial suites—you either adopt PostHog for product analytics and pair it with a BI tool for business reporting, or assemble components based on your primary need.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-products)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **[Atlassian Analytics](https://www.atlassian.com/)**  
  Analytics and reporting within the Atlassian ecosystem; connects Jira, Confluence, and Bitbucket data for cross-product dashboards and insights.

- **[Mixpanel](https://mixpanel.com/)**  
  Product analytics platform focused on funnels, retention, and cohort analysis; known for polished UX and strong B2B SaaS adoption . **Free tier**: 1M events/month; **Growth**: $36/month . **Best for teams wanting pure product analytics** without the bloat of all-in-one platforms—but lacks native session replay, feature flags, or A/B testing .

- **[Amplitude](https://amplitude.com/)**  
  Enterprise product analytics with a deep behavioral graph and collaboration features (notebooks) for product and data teams . **Free tier**: 50K events/month (more limited than PostHog/Mixpanel); **Growth/Enterprise**: custom pricing . **Best for large tech companies** with dedicated data teams needing advanced behavioral analysis—but setup and adoption are heavier, and entry pricing is not publicly listed .

- **[Heap](https://heap.io/)**  
  Digital insights platform with autocapture and retroactive analysis; now part of Contentsquare.

- **[Tableau](https://www.tableau.com/)**  
  Enterprise visual analytics; widely used for business intelligence dashboards when connected to a data warehouse.

- **[Power BI](https://powerbi.microsoft.com/)**  
  Microsoft's BI platform; common for business reporting in Microsoft-centric organizations.

- **[Looker](https://looker.com/)**  
  Google Cloud BI platform built on LookML for governed metric definitions; strongest when standardized on BigQuery.

- **[ThoughtSpot](https://www.thoughtspot.com/)**  
  Search-driven analytics with natural language querying and AI-powered insights.

- **[Pendo](https://www.pendo.io/)**  
  Product analytics and in-app guidance platform; combines usage analytics, feature adoption, NPS, and guided onboarding.

- **[Sisense](https://www.sisense.com/)**  
  BI and analytics platform with embedded analytics capabilities and a fusion data model.

## Open-Source GitHub Projects

### All-in-One Product Analytics (PostHog)

- **[PostHog](https://github.com/PostHog/posthog)**  
  The **leading open-source product analytics platform** (MIT core, self-hostable) . Combines **product analytics** (trends, funnels, retention, user paths), **session replay** (record and replay user sessions linked to events), **feature flags**, **experiments (A/B testing)**, **surveys**, **error tracking**, a **data warehouse**, and a **CDP** on a single event database . **Key advantage**: no data export between tools—a user can be counted in a funnel, watched in a replay, targeted by a flag, and enrolled in an experiment from the same event store . **Free tier**: 1M events/month on cloud; self-hosted has no usage billing . **Best for SaaS teams wanting an all-in-one product toolkit** with self-hosting and GDPR-friendly data control—but onboarding is denser than Mixpanel, and performance degrades on very large volumes (10M+/month) .

### Event Data Pipeline (Jitsu)

- **[Jitsu](https://github.com/jitsucom/jitsu)**  
  Open-source **event data platform** positioned as a Segment alternative (MIT, self-hostable) . Collects events from web, mobile, and server via SDKs or a **drop-in Segment proxy** for migration without touching client code; delivers to ClickHouse, BigQuery, Snowflake, Redshift, Postgres, S3, GCS, and dozens of SaaS tools with **per-minute batching** (vs. Segment's daily/hourly warehouse loads) . Features JavaScript functions for per-event transformation, connector syncs (Airbyte-compatible), user identity graph, **Live Events** debugging, and an **MCP server** for AI agent configuration . **Acquired by Helium Ventures (October 2026)** with continued MIT licensing and no usage limits when self-hosted . **Best for teams needing a self-hosted event pipeline** to feed a warehouse or analytics tool—not a product analytics UI itself.

### Business Intelligence & Dashboards (Superset, Metabase)

- **[Apache Superset](https://github.com/apache/superset)**  
  Modern, enterprise-ready **business intelligence platform** (Apache 2.0) . Features: **no-code chart builder**, web-based **SQL Editor**, lightweight semantic layer for custom dimensions and metrics, support for nearly any SQL database, wide array of visualizations (bar charts to geospatial), caching layer, extensible security roles, and REST API . **Best for teams with SQL skills** wanting to build custom dashboards over product or business data—but requires data modeling and dashboard building from scratch.

- **[Metabase](https://github.com/metabase/metabase)**  
  Open-source **business intelligence platform** (AGPL) designed for non-technical users . Features: visual query builder, interactive dashboards, GUI and SQL editors, embeddable charts, and row/column security . Lighter to deploy than Superset and easier for business users to self-serve. **Best for mixed teams** where product managers need to build their own reports—but product-specific metrics (funnels, retention) must be defined manually.

### Additional Strong Open-Source Options

- **Matomo** — Open-source web analytics platform (PHP/MySQL, self-hosted) with 90+ plugins, heatmaps, session recordings, A/B testing, and form analytics . **Best for web analytics and marketing insights** with full data ownership—not a product analytics platform for in-app behavior.
- **Plausible Analytics** — Lightweight, privacy-focused web analytics (AGPL) without cookies; useful for traffic-level insights alongside dedicated product analytics.

**Frameworks for building custom systems**: For **product analytics with session replay, flags, and experiments**, PostHog is the most complete open-source option . For **event pipeline to warehouse**, Jitsu provides the Segment-like collection layer . For **business intelligence dashboards**, Superset (SQL-savvy teams) or Metabase (non-technical users) . No single open-source project matches the integrated product analytics + BI experience of commercial suites—choose based on whether your primary need is understanding user behavior (PostHog) or building business reports (Superset/Metabase).

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Product and business analytics platforms handling user behavior data must comply with applicable privacy regulations (GDPR, CCPA) and implement proper consent mechanisms for tracking; **self-hosted solutions place full responsibility for data security and retention on the operator**.
- **Open-source product and business analytics is mature but differentiated by purpose**—PostHog provides an all-in-one product toolkit , while Superset and Metabase provide BI dashboards . However, **no single open-source project matches the integrated product analytics + BI experience** of commercial suites. Choose based on whether your primary need is product behavior analysis (PostHog) or business reporting (Superset/Metabase).
- Verify license terms for commercial use; PostHog uses MIT for its core (with an `ee` directory under separate license) , Jitsu uses MIT , Superset uses Apache 2.0, and Metabase uses AGPL.

---

**Made for product managers, growth teams, data analysts, and organizations building analytics infrastructure.**  
Let's make product and business analytics more open, but with clear eyes about the purpose-specific trade-offs that define each path.
