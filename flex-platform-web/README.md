# Server Infrastructure: flex-platform-web

**Last Updated**: June 10, 2026

## Executive Summary

This sub-repository represents a preservation snapshot of the deployed live content from the **`flex-platform-web`** server. Based on the repository contents and the file-system analysis in `/flex-platform-web/README.FSA.md`, this is a **multi-role AWS EC2 web server** used to host several related Axiamax / MaxFlex surfaces at once.

Unlike the narrower production snapshots documented in `/axialy-production-admin/README.md` and `/axialy-production-ui/README.md`, this server is intentionally broad. It combines:

- the **APRO administrative workspace** used to manage files, AI workflows, and deployment operations
- the **AIFLEX model-discovery backend** at `api.maxflex.ai`
- the **AIFLEX public catalog UI** at `aiflex.info`
- at least one **public Axiamax / APRO-branded landing site** under `apro.maxflex.ai`
- a corresponding **admin shell** for APRO at `apro.maxflex.ai/admin/`
- an **APRO HTTPS agent** under `/opt/apro-agent/`
- additional prototype or placeholder surfaces such as `app.maxflex.ai`

Together, these surfaces demonstrate:

- cross-domain product hosting on one EC2 node
- file-aware AI-assisted administration
- secure admin/session architecture
- remote deployment and archive tooling
- GitHub / GoDaddy / remote-server publishing workflows
- AI model catalog discovery and normalization across multiple providers
- public informational product delivery backed by private server-to-server APIs
- practical portfolio utilities and landing pages

---

## Access Information

### Confirmed / Strongly Supported Public Hosts and Surfaces

The exact Route53 / Apache vhost export is not included here, but the filesystem and README/FSA evidence strongly support the following deployed surfaces:

- **Server landing / public web root**: [http://34.222.211.191](http://34.222.211.191)
- **AIFLEX public catalog site**: `aiflex.info`
- **AIFLEX API / model discovery service**: `api.maxflex.ai`
- **APRO public site / landing surface**: `apro.maxflex.ai`
- **APRO administrative suite**: `apro.maxflex.ai/admin/`
- **APRO admin workspace**: `apro.maxflex.ai/admin/apro/`
- **Application placeholder surface**: `app.maxflex.ai`

### Important Access Caveat

This repository is a **filesystem snapshot**, not a full cloud/IaC export. That means exact DNS records, TLS configuration, Apache vhost definitions, reverse proxy details, and security-group rules are not fully visible here. The conclusions below are based on:

- `/flex-platform-web/README.FSA.md`
- the repository directory structure
- the documented purposes of analyzed files
- host/domain names embedded directly in paths and code

Where a hostname is clearly supported by directory layout and file intent, it is described as confirmed or strongly supported. Where final routing depends on unseen vhost config, that limitation is called out implicitly through cautious wording.

---

## Infrastructure Details

### AWS Instance Metadata

- **Instance ID**: `i-08ccd78947c4ca9fa`
- **Launch Time**: `Thu May 07 2026 23:13:40 GMT-0700`
- **Public IPv4 Address**: `34.222.211.191`
- **Private IPv4 Address**: `172.31.62.110`
- **Public DNS**: `ec2-34-222-211-191.us-west-2.compute.amazonaws.com`
- **Instance Type**: `t3.large`
- **AMI**: `ami-05aa7270b4bf13f94` (`al2023-ami-2023.11.20260505.0`)
- **VPC**: `vpc-0b3c893e4f2a794f8`
- **Subnet**: `subnet-0cbad4bf03f7f08be`
- **Virtualization**: `hvm`

### Hosting Interpretation

This is a comparatively capable EC2 node intended to support **multiple related Axiamax / MaxFlex products at once**. The repository contents suggest a mixed architecture consisting of:

- Apache-hosted PHP web applications
- a public/private split between landing sites, admin suites, and APIs
- SQLite-backed and filesystem-backed operational tooling
- server-to-server API authentication via shared environment/master config
- remote-agent administration for deployment/file management
- AI provider integrations spanning OpenAI, Anthropic, Gemini, Replicate, and ElevenLabs

This server is important from a portfolio perspective because it shows not just one application, but an **ecosystem host** combining:

- public product presentation,
- internal administration,
- private API services,
- deployment infrastructure,
- and AI model intelligence systems.

---

## Repository / Server Layout Overview

The FSA identifies several major areas of interest across this server snapshot:

- `/flex-platform-web/opt/apro-agent/`
- `/flex-platform-web/var/www/api.maxflex.ai/`
- `/flex-platform-web/var/www/aiflex.info/`
- `/flex-platform-web/var/www/apro.maxflex.ai/`
- `/flex-platform-web/var/www/app.maxflex.ai/`
- `/flex-platform-web/var/www/maxflex.ai/`
- `/flex-platform-web/var/www/README.md`

### Architectural interpretation

This server appears to separate responsibilities into at least five layers:

1. **public informational UI surfaces** (`aiflex.info`, `apro.maxflex.ai`, portions of `maxflex.ai`)
2. **private/service APIs** (`api.maxflex.ai`)
3. **authenticated administrative tooling** (`apro.maxflex.ai/admin/` and `/admin/apro/`)
4. **remote deployment/file-management agent infrastructure** (`/opt/apro-agent/`)
5. **shared runtime configuration under `/var/www`** (including `.env.master` referenced by multiple apps)

That combination is especially valuable in a portfolio because it shows both:

- product/interface engineering, and
- the operations/infrastructure tooling required to run and update those products.

---

## High-Level Product Map

## 1. APRO HTTPS Agent — `/opt/apro-agent/`

**Confirmed role:** lightweight administrative agent for secure remote filesystem and deployment operations.

The FSA identifies:

- `/flex-platform-web/opt/apro-agent/.htaccess`
- `/flex-platform-web/opt/apro-agent/index.php`
- `/flex-platform-web/opt/apro-agent/README.md`

### Confirmed capabilities

According to the FSA, this agent provides:

- directory/tree traversal
- file reading
- archive creation and restoration
- software package publishing via `.tar.gz`
- environment configuration file management
- allowed-root enforcement
- API-key authentication
- helper-binary integration for privileged install/archive operations

### Confirmed external/runtime dependencies

Referenced by the agent:

- `/etc/flex/api_key`
- `/etc/flex/allowed_root`
- `/etc/flex/default_dest_root`
- `/usr/local/sbin/flex-apro-install-file`
- `/usr/local/sbin/flex-apro-archive-file`

### Portfolio significance

This is one of the strongest infrastructure artifacts in the repository because it demonstrates:

- secure agent-based administration
- constrained remote deployment tooling
- defensive path handling
- archive/restore workflows for safer publishing
- practical separation between UI/admin clients and privileged execution helpers

---

## 2. `api.maxflex.ai` — AI Model Discovery and File-Generation API

**Confirmed role:** private or controlled-access backend service for model discovery, model catalog refresh, pricing normalization, and AI-driven file generation support.

The API surface lives under:

- `/flex-platform-web/var/www/api.maxflex.ai/`

### Confirmed major responsibilities

From the FSA, this service includes:

- discovery of AI model catalogs across providers
- provider normalization into a shared internal schema
- curated metadata enrichment
- multi-source pricing aggregation
- refresh jobs with SQLite persistence
- async refresh execution/job tracking
- authentication for protected endpoints
- AI-driven `generate-files` orchestration
- dedicated provider runtimes for OpenAI and Gemini

### Confirmed provider/model coverage

The metadata and provider layers explicitly cover:

- **OpenAI**
- **Anthropic**
- **Gemini**
- **Replicate**
- **ElevenLabs**

Representative files include:

- `/flex-platform-web/var/www/api.maxflex.ai/index.php`
- `/flex-platform-web/var/www/api.maxflex.ai/src/bootstrap.php`
- `/flex-platform-web/var/www/api.maxflex.ai/src/Database.php`
- `/flex-platform-web/var/www/api.maxflex.ai/src/CatalogRepository.php`
- `/flex-platform-web/var/www/api.maxflex.ai/src/RefreshService.php`
- `/flex-platform-web/var/www/api.maxflex.ai/src/AiGenerationService.php`
- `/flex-platform-web/var/www/api.maxflex.ai/src/runtime/OpenAiRuntime.php`
- `/flex-platform-web/var/www/api.maxflex.ai/src/runtime/GeminiRuntime.php`
- curated metadata files under `/metadata/*.json`

### Pricing and normalization architecture

The pricing subsystem includes:

- curated Gemini pricing collection
- Gemini official-doc parsing
- Gemini legacy pricing fallbacks
- OpenAI official-doc pricing parsing
- aggregator-based precedence handling across sources

This is particularly notable because it shows a **nontrivial data-fusion architecture**, not merely a pass-through proxy.

### Data persistence and ops design

The FSA indicates SQLite-backed storage for:

- refresh jobs
- provider runs
- run models
- published catalog state

This demonstrates:

- job lifecycle tracking
- reproducible catalog refreshes
- asynchronous operational workflows
- durable internal service state

### Portfolio significance

`api.maxflex.ai` is a standout artifact because it demonstrates:

- backend architecture
- API design
- provider abstraction
- schema normalization across heterogeneous AI vendors
- pricing reconciliation logic
- operational telemetry/job processing
- AI-assisted file generation orchestration for admin tooling

---

## 3. `aiflex.info` — Public AI Model Discovery Catalog

**Confirmed role:** public-facing informational site for browsing AI model metadata.

The site is located at:

- `/flex-platform-web/var/www/aiflex.info/`

### Confirmed purpose

The FSA describes this as a secure, read-only PHP frontend that:

- authenticates server-to-server against the private discovery service
- fetches AI model catalog data from `api.maxflex.ai`
- applies server-side filtering
- renders an interactive dashboard for public browsing

Representative files include:

- `/flex-platform-web/var/www/aiflex.info/index.php`
- `/flex-platform-web/var/www/aiflex.info/README.md`

### Confirmed user-facing capabilities

The catalog UI supports filtering on dimensions such as:

- search text
- numeric pricing/limit ranges
- date cutoffs
- category/facet filtering
- model capabilities and limits

### Portfolio significance

This site is important because it shows the ability to pair:

- a private/internal backend service, with
- a public-facing, user-friendly discovery interface.

It also demonstrates thoughtful security boundaries, since the public UI does **not** expose private credentials directly and instead uses authenticated server-side fetches.

---

## 4. `apro.maxflex.ai` — Public APRO / Axiamax Landing Surface

**Confirmed role:** public-facing landing surface for the APRO / Axiamax presence, including demo-able utilities.

The site root is under:

- `/flex-platform-web/var/www/apro.maxflex.ai/`

### Confirmed public pages and utilities

The FSA identifies several public/demo-able resources, including:

- `/flex-platform-web/var/www/apro.maxflex.ai/index.php`
- `/flex-platform-web/var/www/apro.maxflex.ai/handsfree-reader.html`
- `/flex-platform-web/var/www/apro.maxflex.ai/read_aloud_basic.html`
- `/flex-platform-web/var/www/apro.maxflex.ai/market-entry-strategy-sample.html`
- `/flex-platform-web/var/www/apro.maxflex.ai/sitemap.php`

### Public utility examples

#### Hands-Free Reader

- standalone teleprompter/scrolling-reader utility
- adjustable speed and text sizing
- fullscreen-oriented reading UX
- persistent local browser preferences

#### Read Aloud Basic

- browser-native text-to-speech utility
- voice/rate/pitch/volume controls
- speak/pause/resume/stop workflow
- local persistence of user settings

#### Market Entry Strategy Sample

- standalone presentation/demo artifact
- business strategy / executive-summary style deliverable
- interactive financial projection elements

### Public landing-page significance

The root landing page also acts as a brand/portal page directing visitors toward:

- consulting-oriented surfaces
- Axialy-related work
- hidden/admin entry points for internal operations

### Portfolio significance

This area demonstrates:

- public-facing presentation work
- lightweight but useful browser utilities
- practical HTML/CSS/JS craftsmanship
- ability to ship self-contained tools and supporting demo artifacts

---

## 5. `apro.maxflex.ai/admin/` — Admin Shell

**Confirmed role:** authenticated administrative root for the APRO site.

Representative files include:

- `/flex-platform-web/var/www/apro.maxflex.ai/admin/index.php`
- `/flex-platform-web/var/www/apro.maxflex.ai/admin/login.php`
- `/flex-platform-web/var/www/apro.maxflex.ai/admin/logout.php`
- `/flex-platform-web/var/www/apro.maxflex.ai/admin/dashboard.php`
- `/flex-platform-web/var/www/apro.maxflex.ai/admin/includes/bootstrap.php`
- `/flex-platform-web/var/www/apro.maxflex.ai/admin/includes/auth.php`

### Confirmed responsibilities

The admin shell provides:

- secure admin login/logout
- session initialization and cookie hardening
- authenticated routing to dashboard/admin tools
- shared bootstrap/env helper logic
- safe redirects and JSON-aware auth behavior for admin APIs

### Portfolio significance

This shows practical knowledge of:

- secure session-based admin access
- separation between public and privileged routes
- reusable admin bootstrap/auth utility design

---

## 6. `apro.maxflex.ai/admin/apro/` — APRO Administrative Workspace

**Confirmed role:** the core APRO application, described by the FSA and internal README as a file-aware AI workspace and admin suite.

This is one of the most important parts of the entire repository.

### Confirmed functional scope

The APRO workspace demonstrates:

- local filesystem browsing
- GitHub repository browsing and publishing
- GoDaddy/cPanel browsing and publishing
- remote HTTPS-agent browsing and publishing
- AI prompt submission against selected files/paths
- file-system analysis
- feature analysis
- implementation plan generation
- file publish analysis / tile extraction workflows
- archive browsing/restoration
- AI model discovery integration
- request history tracking
- publish/merge/approval workflows for generated files

### Key top-level files

Representative files include:

- `/flex-platform-web/var/www/apro.maxflex.ai/admin/apro/index.php`
- `/flex-platform-web/var/www/apro.maxflex.ai/admin/apro/README.md`
- `/flex-platform-web/var/www/apro.maxflex.ai/admin/apro/api/*.php`
- `/flex-platform-web/var/www/apro.maxflex.ai/admin/apro/assets/js/*.js`
- `/flex-platform-web/var/www/apro.maxflex.ai/admin/apro/includes/*.php`
- `/flex-platform-web/var/www/apro.maxflex.ai/admin/apro/prompts/*.txt`

---

## 6A. APRO: File and Source-Navigation Capabilities

The workspace supports multiple source types:

- **Local server filesystem**
- **GitHub repositories**
- **Remote servers via HTTPS agent**
- **GoDaddy/cPanel-hosted environments**

This is reflected in both backend APIs and frontend modules such as:

- `tree.php`, `github_tree.php`, `server/tree.php`, `godaddy/tree.php`
- `tree.js`, `treeServer.js`, `treeGoDaddy.js`, `githubConnections.js`, `godaddyAccounts.js`

### Portfolio significance

This is unusually strong evidence of:

- multi-target file orchestration
- practical deployment tooling UX
- unified control-plane design across heterogeneous storage/runtime targets

---

## 6B. APRO: AI Request Submission and Analysis Workflows

The API and UI layers support multiple AI-assisted workflows, including:

- generic request submission (`submit.php`)
- prompt preview generation (`preview_payload.php`)
- file system analysis (`file_analysis.php` + `fileSystemAnalysis.js`)
- feature analysis (`feature_analysis.php` + `featureAnalysis.js`)
- implementation plan generation (`implementation_plan.php` + `implementationPlanAnalysis.js`)

### Confirmed prompt/template support

The APRO prompt library includes templates such as:

- `base_request.txt`
- `file_system_analysis.txt`
- `feature_analysis.txt`
- `implementation_plan.txt`
- `file_publish_analysis.txt`
- `file_publish_merge.txt`
- `use_case_request.txt`

This is significant because it shows explicit **prompt engineering as a product/system capability**, not just ad hoc API calling.

---

## 6C. APRO: File Publish / Generated-Files Workflows

The workspace includes a substantial file-publishing subsystem with modular frontend and backend components.

### Confirmed backend/API workflows

Representative backend files include:

- `publish_analyze.php`
- `generate_files.php`
- `publish_commit.php`
- `publish_merge.php`
- `publish_tiles.php`
- `github_publish.php`
- `github_publish_bulk.php`
- `godaddy/publish.php`
- `server/publish.php`
- `server/env_publish.php`

### Confirmed frontend/panel workflows

Representative JS modules include:

- `assets/js/filePublish/actions.js`
- `analyze.js`
- `api.js`
- `approval.js`
- `clipboard.js`
- `createFromAiResponse.js`
- `createFromCurrent.js`
- `generate.js`
- `githubForm.js`
- `merge.js`
- `panel.js`
- `publishGithub.js`
- `publishGoDaddy.js`
- `publishLocal.js`
- `publishServer.js`
- `renderTiles.js`
- `reviewModal.js`
- `serverForm.js`
- `state.js`
- `tileHydration.js`
- `utils.js`

### Confirmed architectural significance

This subsystem demonstrates:

- AI-generated file proposal parsing
- approval/review state management
- merge assistance for REPLACE operations
- diff/review modal UX
- publishing to multiple destinations
- chunking and payload-size handling
- archive-before-overwrite deployment safety

This is one of the strongest engineering artifacts in the repository because it combines:

- AI orchestration,
- admin UX,
- file safety controls,
- and real deployment workflows.

---

## 6D. APRO: Archive and Restore Management

Archive handling appears in both local and remote workflows.

Representative files include:

- `archives.php`
- `archive_file.php`
- `file_archives.php`
- `server/archive.php`
- `server/archives.php`
- `godaddy/archives.php`
- `assets/js/archiveManager.js`
- `assets/js/fileArchives.js`

### Confirmed capabilities

These modules support:

- listing archive versions
- reading archive contents
- comparing live vs archived versions
- restoring prior versions
- rehoming/exporting archive groups
- archive handling across local, remote, and GoDaddy targets

### Portfolio significance

This demonstrates production-minded safety design:

- not just “publish new file,” but
- “publish with rollback and archive-aware operational controls.”

---

## 6E. APRO: AI Model Discovery Integration

The APRO admin workspace integrates directly with the AIFLEX catalog service.

Representative files include:

- `api/ai_model_discovery.php`
- `assets/js/aiModelDiscovery.js`

### Confirmed capabilities

This integration supports:

- browsing shared model catalogs
- filtering by provider/capability/pricing
- selecting runtime models for admin workflows
- triggering catalog refreshes and polling refresh status

This demonstrates cohesive system design between:

- the dedicated discovery API (`api.maxflex.ai`), and
- the consuming operational/admin client (`APRO`).

---

## 7. `app.maxflex.ai` — Placeholder Application Surface

**Confirmed role:** simple under-construction application placeholder.

The FSA identifies:

- `/flex-platform-web/var/www/app.maxflex.ai/index.php`

### Confirmed behavior

This file returns a simple “under construction” page and injects the current host into the output.

### Portfolio interpretation

This is not itself a major portfolio artifact, but it does show:

- reserved/deployed host management,
- incremental product rollout practices,
- and multi-app hosting on one server.

---

## 8. `maxflex.ai` Surface Present in Snapshot

The FSA also documents a parallel `maxflex.ai` tree containing admin/APRO-related structures similar to `apro.maxflex.ai`.

Because the top-level README and selected repository framing focus more explicitly on `apro.maxflex.ai`, and because vhost/export context is incomplete, the safest interpretation is:

- this server snapshot preserves **multiple closely related host trees**,
- including both `apro.maxflex.ai` and `maxflex.ai`,
- with overlapping or mirrored administrative/APRO structures.

This is useful to mention because it suggests the server was used not only for one public hostname but for **multiple related brand/application contexts**.

---

## 9. Shared Runtime / Environment Dependencies

Multiple applications on this host reference shared runtime dependencies such as:

- `/var/www/.env.master`
- `/var/www/.user.ini`
- `/usr/local/sbin/flex-apro-install-file`
- `/usr/local/sbin/flex-apro-archive-file`
- `/etc/flex/api_key`
- `/etc/flex/allowed_root`
- `/etc/flex/default_dest_root`

### Important caveat

These are **runtime and operational dependencies**, not public-facing routes. They are important because they show:

- centralized environment management
- shared admin/runtime configuration across multiple apps
- privileged helper integration for safe install/archive workflows
- a practical production/security model beyond plain PHP pages alone

---

## Internal Documentation Present in the Repository

This server snapshot preserves not only executable code but also substantial internal documentation, including:

- `/flex-platform-web/README.FSA.md`
- `/flex-platform-web/var/www/api.maxflex.ai/README.md`
- `/flex-platform-web/var/www/apro.maxflex.ai/README.md`
- `/flex-platform-web/var/www/apro.maxflex.ai/admin/README.md`
- `/flex-platform-web/var/www/apro.maxflex.ai/admin/apro/README.md`
- `/flex-platform-web/opt/apro-agent/README.md`
- `/flex-platform-web/var/www/README.md`

This matters from a portfolio perspective because it demonstrates:

- technical writing discipline
- system explanation ability
- maintainability thinking
- operational clarity around how products fit together

---

## Relationship to Other Repository Snapshots

This repository should be interpreted alongside:

- `/p3plzcpnl503722/README.md`
- `/axialy-production-admin/README.md`
- `/axialy-production-ui/README.md`

### Relationship to `/p3plzcpnl503722/README.md`

`p3plzcpnl503722` shows older shared-hosting breadth across many public and prototype systems. By contrast, `flex-platform-web` shows a more AWS-oriented operational environment with:

- APRO as a serious admin/deployment workspace
- AIFLEX as a structured model-discovery service
- public/private surfaces split across dedicated hosts
- stronger evidence of platform-style infrastructure thinking

### Relationship to `axialy-production-admin` and `axialy-production-ui`

The APRO tooling and agent-based patterns on this server help explain how broader Axialy/MaxFlex infrastructure can be managed across nodes. The top-level README already notes that APRO enables administration of connected infrastructure such as:

- `axialy-production-admin`
- `axialy-production-ui`

That relationship is valuable because it shows:

- breadth across multiple servers and products, and
- depth in the tooling used to inspect, generate, publish, and manage code/configuration across environments.

---

## Public / Demo Discussion Value

Strong employer/demo discussion topics from this repository include:

- how APRO unifies local, GitHub, GoDaddy, and remote-server workflows
- how the APRO agent/HTTPS-agent model constrains privileged file access safely
- how AIFLEX normalizes model metadata and pricing across multiple AI vendors
- how the public `aiflex.info` site consumes private discovery infrastructure securely
- how archive/restore safety was integrated into publishing workflows
- how AI-generated file changes are converted into reviewable/publishable tiles
- how multi-surface systems (public site, admin suite, private API, remote agent) can coexist on a single host
- how lightweight browser utilities and public demo artifacts complement heavier backend/admin tooling

---

## Limitations of This Snapshot

This repository is a **downloaded filesystem snapshot**, not a full operational export. As a result:

- Apache vhost mappings are only partially inferable
- DNS/TLS/load balancer details are not fully represented
- some dependencies are runtime-only and not included in-repo
- some mirrored host trees may reflect deployment staging, alternate domains, or parallel surfaces not fully distinguishable without infra config
- at least some files in the FSA lacked content and therefore cannot support strong file-level claims
- secrets and live environment values are not suitable for assumption from the snapshot alone

Where this README makes strong statements, they are grounded in the explicit file purposes documented in `/flex-platform-web/README.FSA.md` and in clearly named host-path structures visible in the repository.

---

## Summary

`flex-platform-web` is a broad, technically rich AWS-hosted server snapshot showing a **multi-surface Axiamax / MaxFlex ecosystem**.

It demonstrates:

- APRO as a file-aware AI admin and deployment workspace
- secure agent-based remote file and publish operations
- AIFLEX as a normalized AI model discovery backend
- `aiflex.info` as a public-facing model catalog frontend
- public landing/demo utilities under `apro.maxflex.ai`
- authenticated admin-shell architecture
- GitHub, GoDaddy, local, and remote-server orchestration
- archive-aware publishing and rollback support
- real platform thinking across public UI, private API, and operational tooling

As a portfolio artifact, it is especially valuable because it shows both **ecosystem breadth** and **operational depth**: public sites, private APIs, model intelligence, admin tooling, deployment infrastructure, and AI-assisted implementation workflows all preserved in one server snapshot.