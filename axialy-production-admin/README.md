# Server Infrastructure: axialy-production-admin

**Last Updated**: June 10, 2026

## Executive Summary

This sub-repository represents a preservation snapshot of the deployed live content from the **`axialy-production-admin`** server. It documents the production administrative environment used to operate the Axialy platform and related tooling.

Unlike the broader legacy shared-hosting repository documented in `/p3plzcpnl503722/README.md`, this repository is focused on a **single production administration server** hosted on AWS EC2. Its purpose is not public marketing content; its purpose is operational control.

Based on the repository contents and the file-system analysis in `/axialy-production-admin/README.FSA.md`, this server contains two major deployed surfaces:

1. **`admin.axialy.ai`** — the Axialy administrative web interface
2. **an admin API / APRO-style operational endpoint** under `/var/www/html/admin-api/`

Together, these components demonstrate:

- production admin dashboard design
- authenticated session management
- multi-environment database connectivity
- operational CRUD tooling
- document/version/file lifecycle management
- support issue workflows
- promotional code administration
- secure file-aware administrative API design

---

## Access Information

### Confirmed Public/Admin-Facing URL

- **Primary Admin URL**: [https://admin.axialy.ai](https://admin.axialy.ai)

### Important Access Caveat

This repository is a **filesystem snapshot**, not a full cloud/IaC export. The exact public routing, DNS records, TLS termination details, load balancer behavior, and security group rules are not fully represented here. The conclusions below are based on:

- the top-level server README
- the repository layout
- `/axialy-production-admin/README.FSA.md`
- the documented purpose of each analyzed file

Where routing is directly supported by the snapshot, it is described as confirmed. Where a behavior is inferred from file placement and purpose, it is labeled accordingly.

---

## Infrastructure Details

### AWS Instance Metadata

- **Instance ID**: `i-0c80eccdefd75a5ed`
- **Launch Time**: `Thu Sep 18 2025 16:40:11 GMT-0700`
- **Public IPv4 Address**: `44.246.21.165`
- **Private IPv4 Address**: `172.31.53.94`
- **Public DNS**: `ec2-44-246-21-165.us-west-2.compute.amazonaws.com`
- **Instance Type**: `t3.micro`
- **AMI**: `al2023-ami-2023.8.20250915.0-kernel-6.1-x86_64`
- **VPC**: `vpc-0b3c893e4f2a794f8`
- **Subnet**: `subnet-0cbad4bf03f7f08be`
- **Key Pair**: `axialy-admin-prod-key`
- **Virtualization**: `hvm`

### Hosting Interpretation

This is a compact AWS-hosted production admin node intended to provide a lightweight but capable control plane for the Axialy ecosystem. The repository contents suggest a pragmatic architecture:

- Apache/PHP-hosted administrative UI
- PHP-based administrative AJAX endpoints
- filesystem-aware operational API for deployment/file management
- database-backed authentication and admin session tracking
- environment-aware connections across production/test/dev-style systems

---

## Repository / Server Layout Overview

The file-system analysis indicates two primary web roots of interest:

- `/axialy-production-admin/var/www/html/admin-api/`
- `/axialy-production-admin/var/www/html/axialy-admin/`

There is also a diagnostic artifact:

- `/axialy-production-admin/var/www/html/archive-test.txt`

### What this means architecturally

The server appears to separate:

- a **browser-facing admin application** for authenticated operators
- a **backend administrative API** for secure file operations and environment/config management

This split is important from a portfolio perspective because it shows both:

- human-operated dashboard engineering, and
- infrastructure/ops-oriented API design

---

## High-Level Product Map

## 1. `admin.axialy.ai` — Axialy Administrative Control Panel

**Confirmed role:** primary administrative web interface for the Axialy platform.

The directory:

- `/axialy-production-admin/var/www/html/axialy-admin/`

contains the full admin application. According to the FSA, this application manages:

- admin authentication
- admin session persistence
- environment switching
- database viewing
- documentation and version management
- issue/support workflows
- promo code management
- initialization/bootstrap of the first admin user

### Key entry points and operational files

Confirmed files include:

- `/axialy-production-admin/var/www/html/axialy-admin/index.php`
- `/axialy-production-admin/var/www/html/axialy-admin/admin_login.php`
- `/axialy-production-admin/var/www/html/axialy-admin/admin_login.http.php`
- `/axialy-production-admin/var/www/html/axialy-admin/logout.php`
- `/axialy-production-admin/var/www/html/axialy-admin/init_user.php`
- `/axialy-production-admin/var/www/html/axialy-admin/desktop.php`

### Core capabilities demonstrated

From the analyzed files, this admin surface demonstrates:

- secure login workflow against an `admin_users` table
- persistent server-side session validation via `admin_user_sessions`
- bootstrap/initialization logic for first-time admin setup
- dashboard-driven navigation to operational tools
- environment selection across multiple deployment targets
- modular admin architecture with dedicated pages for each management function

### Why it matters in the portfolio

This is a strong demonstration of real administrative product work because it shows:

- secure session-backed admin application design
- practical back-office UX
- operational workflows beyond basic CRUD
- production-minded separation of concerns
- maintainable modular PHP architecture

---

## 2. Admin API / APRO-Style Operational Endpoint

**Confirmed role:** secure administrative API for file management, deployment support, archiving, and configuration operations.

The directory:

- `/axialy-production-admin/var/www/html/admin-api/`

contains:

- `.htaccess`
- `index.php`

According to `/axialy-production-admin/README.FSA.md`, this API acts as a front-controller-based administrative endpoint which provides secure, authenticated access to system and file operations.

### Confirmed referenced dependencies

The FSA identifies these external dependencies referenced by `admin-api/index.php`:

- `/etc/mfp/api_key`
- `/etc/mfp/allowed_root`
- `/var/www/html/.env.master`
- `/usr/local/sbin/mfp-apro-install-file`
- `/usr/local/sbin/mfp-apro-archive-file`

### Confirmed capabilities

The admin API is documented as supporting:

- filesystem tree navigation
- file reading
- archive/version history workflows
- deployment via `.tar.gz` archives
- environment configuration file management
- restoration of previous file versions
- strict allowed-root enforcement
- API-key-based authentication
- path normalization to mitigate traversal risks

### Why it matters in the portfolio

This endpoint is especially valuable as a portfolio artifact because it demonstrates:

- secure administrative API design
- production file management tooling
- deployment-support automation
- privilege-aware system integration with shell helpers
- defensive handling of high-risk operations like file replacement and restore

---

## Axialy Admin Application: Feature Breakdown

## 1. Authentication and Session Management

**Confirmed files:**

- `/axialy-production-admin/var/www/html/axialy-admin/admin_login.php`
- `/axialy-production-admin/var/www/html/axialy-admin/admin_login.http.php`
- `/axialy-production-admin/var/www/html/axialy-admin/logout.php`
- `/axialy-production-admin/var/www/html/axialy-admin/includes/admin_auth.php`
- `/axialy-production-admin/var/www/html/axialy-admin/includes/AdminDBConfig.php`

### Confirmed behavior from FSA

The authentication layer handles:

- secure session initialization
- credential verification against `admin_users`
- account status checks
- creation and validation of persistent `admin_user_sessions`
- logout invalidation of database-backed sessions
- redirect behavior for unauthorized users
- CSRF-aware login flow in `admin_login.php`

### Portfolio significance

This shows a real authenticated administration system rather than a mock interface. It reflects practical knowledge of:

- session-backed admin security
- database-driven authentication state
- logout/session revocation
- controlled access to privileged tools

---

## 2. Admin Database and Configuration Layer

**Confirmed files:**

- `/axialy-production-admin/var/www/html/axialy-admin/includes/AdminDBConfig.php`
- `/axialy-production-admin/var/www/html/axialy-admin/includes/Config.php`
- `/axialy-production-admin/var/www/html/axialy-admin/includes/db_connection.php`
- `/axialy-production-admin/var/www/html/axialy-admin/includes/ui_db_connection.php`
- `/axialy-production-admin/var/www/html/axialy-admin/includes/environment_selector.php`
- `/axialy-production-admin/var/www/html/axialy-admin/.env`

### Confirmed architecture from FSA

The server includes a substantial configuration and database abstraction layer capable of:

- loading environment configuration from `.env`
- managing separate admin and UI database connections
- selecting environment-specific UI connections dynamically
- defaulting environment state when not explicitly selected
- supporting production/test/dev-style switching
- automatically initializing required admin schema components

### Confirmed schema responsibilities

`AdminDBConfig.php` is documented as ensuring the existence of key admin tables such as:

- `admin_users`
- `admin_user_sessions`

### Portfolio significance

This demonstrates:

- multi-environment platform administration
- configuration abstraction for legacy/modern interoperability
- PDO-based database design
- operational resilience through schema bootstrapping

---

## 3. Main Admin Dashboard

**Confirmed files:**

- `/axialy-production-admin/var/www/html/axialy-admin/index.php`
- `/axialy-production-admin/var/www/html/axialy-admin/desktop.php`
- `/axialy-production-admin/var/www/html/axialy-admin/assets/js/dashboard.js`
- `/axialy-production-admin/var/www/html/axialy-admin/assets/css/styles.css`

### Confirmed dashboard capabilities

The dashboard is documented as providing:

- admin landing/entry point behavior
- system bootstrap checks for initial admin setup
- environment switching UI
- navigation to documentation, promo codes, issues, and DB viewer modules
- mobile-friendly frontend behavior and responsive styling

### Frontend engineering demonstrated

The CSS/JS layer shows:

- responsive/mobile-first layout support
- touch-friendly UI handling
- interface scripting for environment switching
- reusable administrative styling for forms, tables, buttons, pagination, and status states

### Portfolio significance

This provides a strong example of full-stack delivery:

- backend admin logic
- operational dashboard design
- practical UI/UX work for internal tools
- multi-module navigation and state handling

---

## 4. Database Viewer / Inspector

**Confirmed files:**

- `/axialy-production-admin/var/www/html/axialy-admin/db_viewer_admin.php`
- `/axialy-production-admin/var/www/html/axialy-admin/db_viewer_ajax.php`
- `/axialy-production-admin/var/www/html/axialy-admin/assets/js/db_viewer_admin.js`

### Confirmed capabilities from FSA

This subsystem supports:

- discovery/listing of database tables
- row-count display
- paginated table browsing
- column filtering
- CSV export
- safe handling/exclusion of binary or BLOB-heavy fields for serialization/export concerns
- dynamic, JS-driven table navigation and UI rendering
- modal-style inspection of long text content

### Portfolio significance

This is a compelling operational tool because it demonstrates:

- real database introspection workflows
- attention to export/reporting needs
- practical handling of messy data realities such as BLOB columns
- client/server coordination for admin analytics and inspection

---

## 5. Documentation and Asset Management

**Confirmed files:**

- `/axialy-production-admin/var/www/html/axialy-admin/docs_admin.php`
- `/axialy-production-admin/var/www/html/axialy-admin/doc_ajax_actions.php`
- `/axialy-production-admin/var/www/html/axialy-admin/assets/js/docs_admin.js`
- `/axialy-production-admin/var/www/html/axialy-admin/create_minimal_docx.php`

### Confirmed capabilities from FSA

This subsystem supports:

- creating and editing document metadata
- managing document versions
- setting active versions
- handling multiple content formats such as Markdown, HTML, JSON, and XML
- file upload workflows for documentation assets
- binary storage/download concerns for PDF/DOCX-like assets
- generation of DOCX output via a custom minimal DOCX builder

### Notable implementation detail

`create_minimal_docx.php` is explicitly documented as a utility for generating valid Word DOCX files using `ZipArchive` and Open XML package structure generation.

### Portfolio significance

This is strong evidence of:

- document lifecycle engineering
- versioned content management
- file/binary handling in admin systems
- practical automation around business/document deliverables

---

## 6. Support Issue Management

**Confirmed files:**

- `/axialy-production-admin/var/www/html/axialy-admin/issues_admin.php`
- `/axialy-production-admin/var/www/html/axialy-admin/issues_ajax_actions.php`
- `/axialy-production-admin/var/www/html/axialy-admin/assets/js/issues_admin.js`

### Confirmed capabilities from FSA

This subsystem supports:

- listing user-reported issues
- retrieving issue details
- editing issue metadata such as title, description, and status
- sending direct emails related to issues
- using both UI-system and internal admin-database data where required for workflows
- AJAX-driven admin interaction without full page reloads

### Portfolio significance

This demonstrates:

- support tooling design
- admin-side communication workflows
- blended operational data access patterns
- practical issue-resolution UX

---

## 7. Promotional Code Management

**Confirmed files:**

- `/axialy-production-admin/var/www/html/axialy-admin/promo_codes_admin.php`
- `/axialy-production-admin/var/www/html/axialy-admin/promo_codes_ajax_actions.php`
- `/axialy-production-admin/var/www/html/axialy-admin/assets/js/promo_codes_admin.js`

### Confirmed capabilities from FSA

This subsystem supports:

- listing promo codes
- retrieving promo code details
- creating and editing promo codes
- validating different promo code types
- handling unlimited, limited-duration, and discounted pricing models
- support for Stripe-oriented discounted pricing logic

### Portfolio significance

This demonstrates:

- operational marketing tooling
- validation-heavy admin workflows
- business-rule implementation in both frontend and backend layers
- product/commerce support capabilities

---

## 8. Internal Documentation Present in the Repository

**Confirmed documentation files:**

- `/axialy-production-admin/README.FSA.md`
- `/axialy-production-admin/var/www/html/axialy-admin/README.md`
- `/axialy-production-admin/var/www/html/axialy-admin/includes/README.md`

### Why this matters

This repository does not only preserve executable code. It also preserves technical documentation describing:

- component roles
- foundational includes
- module responsibilities
- architectural intent

For portfolio review, this is useful because it shows not just implementation ability, but also:

- system explanation ability
- maintainability mindset
- internal documentation discipline

---

## Referenced Sensitive / Runtime Dependencies

The FSA indicates several runtime dependencies or sensitive files that are part of the deployed system architecture but are not ordinary public application pages. These include:

- `/axialy-production-admin/var/www/html/axialy-admin/.env`
- `/var/www/html/.env.master`
- `/etc/mfp/api_key`
- `/etc/mfp/allowed_root`
- `/usr/local/sbin/mfp-apro-install-file`
- `/usr/local/sbin/mfp-apro-archive-file`

### Important caveat

These references are important for explaining system architecture, but they should be understood as **operational dependencies**, not public-facing portfolio routes. Their presence indicates:

- secret/config-driven deployment
- privileged helper integration
- controlled deployment and archive workflows
- environment-aware application behavior

---

## Public / Demo Discussion Value

Even though this repository centers on admin tooling rather than public marketing pages, it contains strong demo/discussion material for employers, especially around:

- secure admin login/session handling
- multi-environment operational dashboards
- DB inspection and export tooling
- issue management workflows
- documentation/version/file management
- promo code/business-rule administration
- secure admin API architecture for file and deployment operations

Good discussion/demo topics include:

- how environment switching is implemented across databases
- how admin sessions are persisted and validated
- how the DB viewer handles binary/BLOB complications
- how document versions and DOCX generation are structured
- how the admin API safely constrains file access to allowed roots
- how the system separates UI-facing admin workflows from low-level operational API tasks

---

## Relationship to `/p3plzcpnl503722/README.md`

This repository should be interpreted alongside the broader legacy hosting snapshot documented at:

- `/p3plzcpnl503722/README.md`

That repository documents the older multi-product GoDaddy environment containing:

- public portfolio sites
- AxiaBA domains/subdomains
- EZAPP
- APRO
- REELY
- CAMPS / Imagery / SimChart
- shared private infrastructure

By contrast, **`axialy-production-admin`** represents a more focused production administration environment. Together, the two repositories show a broader professional arc:

- public-facing consulting and product presentation on the legacy shared host
- more focused AWS-hosted operational/admin tooling on the production admin server

This relationship is important for portfolio interpretation because it shows both:

- breadth across multiple shipped products and domains, and
- depth in operational tooling and production admin architecture

---

## Limitations of This Snapshot

This repository is a **downloaded server snapshot**, not a full operational backup. As a result:

- cloud networking and DNS configuration are only partially visible
- live database contents are not fully represented here
- secrets and environment values may be omitted, redacted, or environment-specific
- helper binaries referenced by the admin API may not be included in this repository
- some runtime behavior depends on external infrastructure beyond what is stored in source form

Where this README makes strong claims, they are based on the explicit file purposes documented in `/axialy-production-admin/README.FSA.md`.

---

## Summary

`axialy-production-admin` is a focused production administration server snapshot that preserves the operational side of the Axialy platform.

It demonstrates:

- authenticated admin application architecture
- environment-aware database administration
- documentation/version/file lifecycle tooling
- support issue management
- promo code and business-rule administration
- secure file/deployment API design
- practical full-stack engineering for internal operations

As a portfolio artifact, it is especially valuable because it shows real-world administrative engineering rather than only public-facing presentation pages. It complements the broader legacy hosting snapshot by documenting the production-grade control plane side of the ecosystem.