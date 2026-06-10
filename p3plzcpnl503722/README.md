# Server Infrastructure: p3plzcpnl503722

**Last Updated**: June 10, 2026

## Executive Summary

This sub-repository is a preservation snapshot of the legacy GoDaddy shared-hosting server **`p3plzcpnl503722`**, which historically hosted a broad cross-section of Casey Lide / Axiamax / AxiaBA / Axialy portfolio work.

This environment is significant because it contains:

- the legacy public portfolio at **axiamax.com**
- the **AxiBA / Axialy** public and administrative web properties
- multiple AI-assisted product prototypes
- administrative systems such as **APRO** and **REELY**
- API surfaces and prompt/template libraries
- public-facing utilities, demos, and professional documentation

This snapshot is useful both as:
1. a **portfolio artifact** showing shipped and deployed work, and  
2. a **technical reference** showing how multiple products coexisted on one shared-hosting environment.

---

## Hosting Environment

### Server / Hosting Details

From the source hosting environment:

- **Hosting Package**: Deluxe1
- **Server Name**: `p3plzcpnl503722`
- **cPanel Version**: `134.0 (build 35)`
- **Apache Version**: `2.4.67`
- **Database Version**: `10.11.16-MariaDB-cll-lve`
- **Architecture**: `x86_64`
- **Operating System**: `linux`
- **Shared IP Address**: `192.169.174.218`
- **Home Directory**: `/home/i17z4s936h3j`
- **Primary cPanel User**: `i17z4s936h3j`
- **Primary Domain**: `axiamax.com`
- **SSL**: active
- **Sendmail Path**: `/usr/sbin/sendmail`
- **Perl Path**: `/usr/bin/perl`
- **Perl Version**: `5.26.3`

---

## Access Information

## Confirmed Public Domain Root

- **Primary Public Root**: [https://axiamax.com](https://axiamax.com)

## Other Confirmed Domains / Subdomains Present in This Server Snapshot

The user specifically called out the following as important and they are consistent with the filesystem snapshot and configuration/documentation context:

- **AxiBA public site**: `axiaba.com`
- **AxiBA admin site**: `admin.axiaba.com`
- **AxiBA / Axialy API surface**: `api.axiaba.com`
- **EZAPP UI / app builder surface**: `ezapp.axiaba.com`

## Important Caveat on URL Mapping

This repository contains the downloaded filesystem, but not the full Apache vhost/addon-domain mapping exported from cPanel. That means:

- the **presence of a directory** strongly indicates a deployed site or app,
- but the **exact public URL-to-directory mapping** for every addon domain/subdomain may depend on GoDaddy/cPanel configuration not shown directly here.

Where a mapping is well-supported by the snapshot, it is listed below as confirmed. Where exact routing is inferred from directory layout, that is stated explicitly.

---

## High-Level Site / Product Map

## 1. `axiamax.com` — Public Portfolio Root

**Confirmed role:** primary public portfolio / landing domain.

This is the root public website for the broader portfolio and company identity. The snapshot and root README establish it as the main public-facing entry point for legacy professional content.

### Notable public/demo-able utilities on the axiamax.com root

The user specifically identified these as important public resources:

- **Read Aloud Utility**  
  File:  
  `/p3plzcpnl503722/home/i17z4s936h3j/public_html/read_aloud_basic.html`  
  Public route likely:  
  `https://axiamax.com/read_aloud_basic.html`

  Purpose:
  - browser-based text-to-speech utility
  - allows pasted text to be spoken aloud
  - demonstrates practical browser-side UX utility work

- **Hands-Free Reader / Teleprompter Utility**  
  File:  
  `/p3plzcpnl503722/home/i17z4s936h3j/public_html/handsfree-reader.html`  
  Public route likely:  
  `https://axiamax.com/handsfree-reader.html`

  Purpose:
  - teleprompter / scrolling reading utility
  - adjustable reading speed and fullscreen-oriented UX
  - useful as a demo of ergonomic browser tooling

### Other portfolio/supporting root content confirmed in snapshot

Additional public root-level content includes items such as:

- `/contact-form.php`
- `/market-entry-strategy-sample.html`
- `/audacity-track-reference.html`
- root sitemap and general landing content

These support the portfolio by showing:
- consulting/marketing collateral
- practical utility tooling
- writing/presentation/documentation work

---

## 2. `axiaba.com` — Public Consulting / Product Marketing Site

**Confirmed role:** public AxiaBA consulting and marketing site.

The filesystem under:

- `/p3plzcpnl503722/home/i17z4s936h3j/public_html/axiaba.com/`

shows a full public website with:
- root marketing homepage
- service landing pages
- assets
- imagery tooling
- CAMPS
- SIMCHART
- resume and business documentation resources

### Confirmed public marketing / service pages

Examples present in the snapshot include:

- `axiaba.com/index.php`
- `axiaba.com/business-analysis-consulting/index.php`
- `axiaba.com/cbap-certified-consultant/index.php`
- `axiaba.com/digital-transformation-services/index.php`
- `axiaba.com/process-optimization-services/index.php`
- `axiaba.com/stakeholder-engagement-consulting/index.php`

These pages demonstrate:
- consulting positioning
- SEO-focused service landing pages
- professional service packaging
- business analysis / transformation / stakeholder engagement specialization

### Confirmed public professional resource

- **Resume Markdown-to-Preview/Export Tool**  
  File:  
  `/p3plzcpnl503722/home/i17z4s936h3j/public_html/axiaba.com/resume-resources/index.php`  
  Public route likely:  
  `https://axiaba.com/resume-resources/`

  Purpose:
  - browser-based resume markdown preview/export utility
  - supports rendering and export workflows
  - demonstrates practical document UX tooling

### Additional public AxiaBA assets and documents

The `axiaba.com` site also includes:
- standalone consulting overviews
- brand/color documentation
- strategic/architecture pages
- resume materials
- supporting assets and scripts

This area is a strong demonstration of:
- productized consulting presentation
- UX for information delivery
- public-facing business analysis content
- design/system thinking

---

## 3. `admin.axiaba.com` — Administrative Interface

**Confirmed role:** admin web application for AxiaBA operational/admin tasks.

The snapshot contains a dedicated application under:

- `/p3plzcpnl503722/home/i17z4s936h3j/public_html/admin.axiaba.com/`

### Confirmed admin capabilities from filesystem analysis

This admin application includes functionality for:

- authenticated admin login/logout
- environment-aware configuration
- database viewing / inspection
- document management
- promo code management
- issue / support-ticket management
- admin session handling

### Key confirmed files / areas

Examples include:
- `admin_login.php`
- `index.php`
- `docs_admin.php`
- `doc_ajax_actions.php`
- `promo_codes_admin.php`
- `promo_codes_ajax_actions.php`
- `issues_admin.php`
- `issues_ajax_actions.php`
- `db_viewer_admin.php`
- `db_viewer_ajax.php`

### Why it matters in the portfolio

This area demonstrates:
- admin application design
- CRUD-oriented operational tooling
- secure session patterns
- environment-based config loading
- internal back-office workflows

---

## 4. `api.axiaba.com` — API Surface / Backend Services

**Confirmed role:** API host containing multiple backend services, especially **EZAPP**.

The snapshot shows a substantial API codebase under:

- `/p3plzcpnl503722/home/i17z4s936h3j/public_html/api.axiaba.com/`

Most importantly, it contains:

- `/ezapp/` — a large API-driven app-builder / discovery / implementation-planning system

### Confirmed EZAPP backend capabilities

From the filesystem analysis, EZAPP includes endpoints and libraries for:

- authentication and session management
- project creation / loading
- discovery start / revise / accept
- discovery question refresh and commit
- implementation plan generation
- quick-fix plan generation
- build-run creation and stepping
- code review workflows
- runtime repair
- published app access
- AI execution and usage tracking
- generated app template publishing

### Why it matters in the portfolio

This is one of the strongest backend demonstrations in the repository because it shows:
- multi-endpoint API design
- AI-assisted workflow orchestration
- persistence and stateful pipeline design
- generated app infrastructure
- implementation planning and code review automation

---

## 5. `ezapp.axiaba.com` — EZAPP User Interface

**Confirmed role:** UI/frontend for the EZAPP application builder platform.

The snapshot contains a dedicated UI app under:

- `/p3plzcpnl503722/home/i17z4s936h3j/public_html/ezapp.axiaba.com/`

### Confirmed UI capabilities

This frontend includes:
- login/logout/dashboard flows
- project workspace UI
- discovery UI
- implementation-plan UI
- build/review state rendering
- modal-driven project workflows
- client-side state, rendering, and API orchestration modules

### Confirmed structural files

Examples include:
- `index.php`
- `login.php`
- `dashboard.php`
- `project.php`
- `views/project_detail.php`
- `views/discovery_spec_modal.php`
- `views/discovery_questions_modal.php`
- `views/implementation_plan_objective_modal.php`
- rich JS modules under `/assets/js/`

### Why it matters in the portfolio

This area demonstrates:
- frontend architecture on top of a PHP-backed UI
- modular browser-side state/rendering patterns
- admin/productivity UX design
- orchestration of AI-backed backend workflows from UI

---

## 6. `/public_html/admin/` — Shared Admin Root

**Confirmed role:** admin root for multiple admin tools.

This contains:
- main admin login/dashboard
- the **REELY** tool
- documentation indicating **APRO** also exists under the admin ecosystem

Examples:
- `/public_html/admin/index.php`
- `/public_html/admin/dashboard.php`
- `/public_html/admin/reely/...`

This area demonstrates:
- secure admin shell patterns
- multi-tool admin hosting under one domain/root

---

## 7. APRO — Administrative Prompt Routing Operations

**Confirmed role:** legacy file-aware administration and AI workflow suite.

The top-level README already mentioned APRO, and the large filesystem analysis confirms an APRO-oriented file-system analysis context (`README.FSA.md`) and administrative/prompt-library history.

### What APRO demonstrates

- file browsing / file awareness
- prompt and template management
- AI-assisted analysis workflows
- early implementation-planning and file-system reasoning patterns

Because the exact `/admin/apro/` files were not included in the truncated visible examples above, this README should describe APRO at the product level without overclaiming exact routes unless separately verified.

---

## 8. REELY — Automated Video Workflow / Media Automation Prototype

**Confirmed role:** advanced admin-side prototype for automated media generation and export.

The snapshot contains an extensive REELY application under:

- `/p3plzcpnl503722/home/i17z4s936h3j/public_html/admin/reely/`

### Confirmed capabilities from the filesystem

REELY includes:
- project/story/scene/beat/shot/entity workflows
- asset management
- overlay configuration
- narration generation stubs/workflows
- playlist and export workflows
- render jobs
- QA / review pipelines
- AI provider abstractions for OpenAI / Replicate / ElevenLabs
- prompt files and schemas
- test files and database schema dump

### Representative confirmed REELY features

Backend/API examples include:
- scene segmentation
- beat generation
- entity detection/review
- asset upload/gallery
- overlay preview/config
- playlist manifest/export
- QA run/log
- render job status
- automation pipeline orchestration

Frontend examples include:
- project dashboard
- automation panel
- entity manager
- beat panel
- scene manager
- asset gallery
- playlist UI
- export UI
- preferences / model-picker UI

### Why it matters in the portfolio

REELY is especially compelling for employers because it demonstrates:
- end-to-end product prototyping
- AI/media workflow orchestration
- backend + frontend integration
- provider abstraction layers
- asset pipelines
- export generation
- admin-tool UX

---

## 9. `axiaba.com/camps` — CAMPS Media/Story Workflow System

**Confirmed role:** structured story/media production workflow system under the public AxiaBA site.

The snapshot contains a substantial application under:

- `/p3plzcpnl503722/home/i17z4s936h3j/public_html/axiaba.com/camps/`

### Confirmed capabilities

- projects / stories / scenes / beats / shots / entities
- scene strategy and scene specification generation
- anchor analysis and generation
- render orchestration
- image import / revise / commit flows
- gallery and asset workflows
- model catalog / capability handling
- public/admin workbench UI

This product demonstrates:
- file-backed workflow systems
- prompt-driven content planning
- continuity-aware media orchestration
- operational UI + API layering

---

## 10. `axiaba.com/imagery` — Cinematic Imagery Production Tool

**Confirmed role:** image/narration/video generation workflow system.

The snapshot contains a major subsystem under:

- `/p3plzcpnl503722/home/i17z4s936h3j/public_html/axiaba.com/imagery/`

### Confirmed capabilities

- production / book / chapter hierarchy
- stylings generation
- anchor analysis and scoped anchor generation
- section A / CSV generation
- render job orchestration
- narration generation
- browser-side video assembly and upload
- image refine preview / commit / discard
- OpenAI image and text workflows
- ImageMagick diagnostics

This subsystem demonstrates:
- multi-step creative pipeline design
- AI-generated image workflow orchestration
- asset and manifest management
- job-step architecture
- browser-side media tooling

---

## 11. `axiaba.com/simchart` — Structured Data / AI Analysis Tool

**Confirmed role:** structured data extraction, dataset management, custom fields, package compilation, and charting.

The snapshot contains a substantial SimChart system under:

- `/p3plzcpnl503722/home/i17z4s936h3j/public_html/axiaba.com/simchart/`

### Confirmed capabilities

- raw text ingestion
- input-type detection (CSV/TSV/JSON/NDJSON/unstructured)
- field analysis
- structured dataset generation
- saved dataset versions
- custom field specification generation/revision/application
- package creation / compilation
- chart generation and CSV export
- session-aware frontend state and modular UI

This demonstrates:
- AI-assisted data structuring
- schema inference
- dataset versioning
- client-side state architecture
- backend job orchestration

---

## Shared Private Storage / Non-Public Infrastructure

## `private_axiaba/`

**Confirmed role:** shared private storage used across UI/API/Admin systems.

Contains:
- environment files (`.env.*`)
- shared includes/config classes
- uploads
- AI template libraries
- EZAPP prompt/config assets

### Notable confirmed shared areas

- `/private_axiaba/includes/`
- `/private_axiaba/api/templates/`
- `/private_axiaba/uploads/`
- `/private_axiaba/ezapp/config/`
- `/private_axiaba/ezapp/prompts/`

This is a key architectural indicator: the server hosted not just websites, but also a reusable internal platform layer for config, prompts, uploads, and AI assets.

---

## Portfolio Interpretation

This server snapshot demonstrates a strong blend of:

- **Business analysis**
- **product architecture**
- **AI workflow design**
- **frontend engineering**
- **backend/API engineering**
- **admin tool development**
- **content strategy and consulting presentation**
- **media/pipeline prototyping**
- **practical browser utilities**

### Particularly compelling portfolio talking points for employers

- Multi-product coexistence on one shared-hosting environment
- Real-world AI integration patterns, not just toy demos
- Admin tools with operational workflows
- Structured prompt libraries and schema-driven AI outputs
- Public-facing consulting sites and SEO landing pages
- Creative/media automation prototypes
- Data extraction and charting pipelines
- Utility pages that solve real user problems

---

## Limitations of This Snapshot

This repository is a **filesystem snapshot**, not a full infrastructure export. As a result:

- exact cPanel addon-domain mappings are not always visible
- database contents are only partially represented unless exported files exist
- some systems depend on `.env` files not committed here
- some runtime behavior depends on external APIs or platform binaries
- some products contain stubs/placeholders alongside more complete subsystems

Where possible, this README distinguishes:
- **confirmed product presence**
- **confirmed file-level capabilities**
- **inferred public routing**

---

## Suggested Public Demo Talking Points

If discussing this repository with employers, useful demo candidates include:

- `https://axiamax.com/read_aloud_basic.html`
- `https://axiamax.com/handsfree-reader.html`
- `https://axiaba.com/resume-resources/`
- AxiaBA consulting landing pages
- walkthrough of EZAPP architecture
- walkthrough of REELY workflow design
- walkthrough of CAMPS / Imagery / SimChart as AI-enabled prototypes
- discussion of shared prompt/config/template infrastructure in `private_axiaba/`

---

## Summary

`p3plzcpnl503722` was not a single-site host. It was a **multi-product legacy platform environment** containing:

- public consulting/portfolio websites
- administrative tools
- API services
- app-builder systems
- AI prompt libraries
- creative/media workflow prototypes
- structured data tooling
- practical public utilities

As a portfolio artifact, it demonstrates both **breadth** and **depth**: from consulting presentation and UX utilities to sophisticated AI-backed application workflows.
