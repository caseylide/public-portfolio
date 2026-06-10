# Server Infrastructure: axialy-production-ui

**Last Updated**: June 10, 2026

## Executive Summary

This sub-repository represents a preservation snapshot of the deployed live content from the **`axialy-production-ui`** server. It documents the production user-facing environment for the Axialy platform and adjacent marketing surfaces.

Unlike the legacy multi-domain shared-hosting environment documented in `/p3plzcpnl503722/README.md`, this repository is focused on a **single AWS-hosted production UI server**. Based on the repository contents and the file-system analysis in `/axialy-production-ui/README.FSA.md`, this server hosts three major surfaces:

1. **`ui.axialy.ai`** — the primary authenticated Axialy application UI
2. **Axialy marketing pages** under `/var/www/html/axialy-marketing/`
3. **an admin-style operational API** under `/var/www/html/admin-api/`

Together, these surfaces demonstrate:

- SaaS application delivery
- authenticated subscription-gated product UX
- AI-assisted business analysis workflows
- stakeholder feedback systems with PIN-based access
- organization-aware / multi-tenant data handling
- publication and stakeholder invitation workflows
- promotional offer and Stripe billing integration
- SEO/marketing landing-page engineering
- operational file/deployment API design

---

## Access Information

### Confirmed Public URLs

- **Primary Product UI**: [https://ui.axialy.ai](https://ui.axialy.ai)

### Additional Public/Deployed Surfaces Strongly Supported by Snapshot

The exact DNS and virtual-host routing are not fully exported here, but the filesystem strongly supports the presence of:

- **Axialy marketing site / landing-page surface** associated with `/var/www/html/axialy-marketing/`
- **admin-style operational API surface** associated with `/var/www/html/admin-api/`

### Important Access Caveat

This repository is a **filesystem snapshot**, not a full cloud/IaC export. Exact DNS records, reverse-proxy/load-balancer configuration, security groups, ACM/TLS wiring, and final Apache vhost mappings are not fully represented here. The conclusions below are based on:

- `/axialy-production-ui/README.FSA.md`
- the repository directory structure
- file names and documented file purposes
- consistent route and asset references embedded in the analyzed files

Where routing is directly supported by code or file placement, it is described as confirmed. Where final hostnames are inferred from server layout and route references, that is stated implicitly through cautious wording.

---

## Infrastructure Details

### AWS Instance Metadata

- **Instance ID**: `i-0d426542af80eccbd`
- **Launch Time**: `Mon Aug 18 2025 14:08:40 GMT-0700`
- **Public IPv4 Address**: `35.80.117.149`
- **Private IPv4 Address**: `172.31.50.206`
- **Public DNS**: `ec2-35-80-117-149.us-west-2.compute.amazonaws.com`
- **Instance Type**: `t3.small`
- **AMI**: `al2023-ami-2023.8.20250818.0-kernel-6.1-x86_64`
- **VPC**: `vpc-0b3c893e4f2a794f8`
- **Subnet**: `subnet-0cbad4bf03f7f08be`
- **Key Pair**: `axialy-admin-prod-key`
- **Virtualization**: `hvm`

### Hosting Interpretation

This is a production AWS node dedicated primarily to the **user-facing side** of the Axialy ecosystem. Compared with the smaller admin node documented in `/axialy-production-admin/README.md`, this server carries broader frontend and customer-facing responsibility. The repository contents suggest a practical architecture combining:

- Apache/PHP delivery for the application shell and server-rendered pages
- modular JavaScript-driven SPA-style tab loading inside the main product UI
- authenticated JSON endpoints for platform workflows
- Stripe-backed subscription/billing flows
- database-backed stakeholder collaboration features
- S3-backed organization asset/logo handling
- supporting marketing/SEO surfaces on the same host
- an operational `admin-api` for deployment/file-management concerns

---

## Repository / Server Layout Overview

The file-system analysis identifies these major directories of interest:

- `/axialy-production-ui/var/www/html/axialy-ui/`
- `/axialy-production-ui/var/www/html/axialy-marketing/`
- `/axialy-production-ui/var/www/html/admin-api/`
- `/axialy-production-ui/var/www/html/archive-test.txt`

### What this means architecturally

The server appears to combine three complementary responsibilities:

- a **customer/product application** (`axialy-ui`)
- a **public marketing/SEO content layer** (`axialy-marketing`)
- a **secure operational file/deployment API** (`admin-api`)

This is valuable from a portfolio perspective because it shows not only a product interface, but also:

- customer acquisition surfaces,
- subscription and onboarding mechanics,
- external stakeholder collaboration,
- and deployment-aware operational tooling.

---

## High-Level Product Map

## 1. `ui.axialy.ai` — Main Axialy Product UI

**Confirmed role:** primary authenticated user-facing application for the Axialy platform.

The directory:

- `/axialy-production-ui/var/www/html/axialy-ui/`

contains the core application. According to `/axialy-production-ui/README.FSA.md`, this environment supports:

- user authentication and session management
- subscription validation and billing access control
- AI-assisted business analysis package creation
- focus-area generation and refinement
- stakeholder feedback collection and review
- organization management
- publication generation and stakeholder invitations
- support-ticket workflows
- promotional offer flows
- user documentation delivery

### Core entry points and important pages

Confirmed key files include:

- `/axialy-production-ui/var/www/html/axialy-ui/index.php`
- `/axialy-production-ui/var/www/html/axialy-ui/login.php`
- `/axialy-production-ui/var/www/html/axialy-ui/logout.php`
- `/axialy-production-ui/var/www/html/axialy-ui/subscription.php`
- `/axialy-production-ui/var/www/html/axialy-ui/manage-subscription.php`
- `/axialy-production-ui/var/www/html/axialy-ui/accept_tos.php`
- `/axialy-production-ui/var/www/html/axialy-ui/user-documentation.php`

### Portfolio significance

This is a substantial SaaS-style product surface rather than a simple website. It demonstrates:

- real account/session architecture
- subscription-gated application behavior
- modular client/server coordination
- sustained multi-feature product design
- customer-facing platform UX beyond a basic CRUD app

---

## 2. Axialy Marketing Surface

**Confirmed role:** public marketing and SEO landing-page system for Axialy AI products and services.

The directory:

- `/axialy-production-ui/var/www/html/axialy-marketing/`

contains the public marketing site and multiple SEO-oriented landing pages.

### Confirmed public-facing marketing pages

The FSA identifies these representative pages:

- `/axialy-production-ui/var/www/html/axialy-marketing/index.php`
- `/axialy-production-ui/var/www/html/axialy-marketing/demo/index.php`
- `/axialy-production-ui/var/www/html/axialy-marketing/ai-stakeholder-feedback-platform/index.php`
- `/axialy-production-ui/var/www/html/axialy-marketing/automated-business-planning/index.php`
- `/axialy-production-ui/var/www/html/axialy-marketing/business-analysis-software/index.php`
- `/axialy-production-ui/var/www/html/axialy-marketing/collaborative-analysis-platform/index.html`
- `/axialy-production-ui/var/www/html/axialy-marketing/requirements-gathering-tools/index.php`
- `/axialy-production-ui/var/www/html/axialy-marketing/team/index.html`
- `/axialy-production-ui/var/www/html/axialy-marketing/casey-lide/index.html`
- `/axialy-production-ui/var/www/html/axialy-marketing/sitemap.php`

### Confirmed marketing-site capabilities

From the analyzed files, this surface demonstrates:

- SEO landing-page authoring
- structured JSON-LD/schema integration
- product/value-proposition messaging
- campaign/demo pages
- embedded metrics and Tableau-oriented presentation support
- founder/team profile pages
- dynamic sitemap generation for discovery/indexing

### Portfolio significance

This matters because it shows the surrounding commercialization layer of the platform, including:

- product positioning
- conversion-focused landing pages
- technical SEO awareness
- cohesive public-facing brand delivery

---

## 3. Admin API / APRO-Style Operational Endpoint

**Confirmed role:** secure operational API for file, deployment, archive, and environment management.

The directory:

- `/axialy-production-ui/var/www/html/admin-api/`

contains:

- `.htaccess`
- `index.php`

The FSA describes this as a front-controller API that provides authenticated filesystem and deployment operations.

### Confirmed referenced dependencies

The FSA identifies these external/runtime references:

- `/etc/mfp/api_key`
- `/etc/mfp/allowed_root`
- `/var/www/html/.env.master`
- `/var/www/html`
- `/srv/maxflex/public_html`
- `/usr/local/sbin/mfp-apro-install-file`
- `/usr/local/sbin/mfp-apro-archive-file`

### Confirmed capabilities

This API supports:

- filesystem browsing/navigation
- file reads
- directory management support
- archive/versioning workflows
- deployment of `.tar.gz` packages
- constrained file replacement under allowed roots
- environment configuration management
- restore/archive helper integration
- API-key authentication and path normalization defenses

### Portfolio significance

Although not a public marketing feature, this endpoint is technically important because it demonstrates:

- secure operational API design
- deployment-support tooling
- privileged helper integration
- defensive handling of high-risk file operations

---

## Axialy UI Application: Feature Breakdown

## 1. Authentication, Sessions, and Terms/Subscription Enforcement

**Confirmed files:**

- `/axialy-production-ui/var/www/html/axialy-ui/login.php`
- `/axialy-production-ui/var/www/html/axialy-ui/logout.php`
- `/axialy-production-ui/var/www/html/axialy-ui/includes/auth.php`
- `/axialy-production-ui/var/www/html/axialy-ui/includes/api_auth.php`
- `/axialy-production-ui/var/www/html/axialy-ui/includes/validate_subscription.php`
- `/axialy-production-ui/var/www/html/axialy-ui/accept_tos.php`

### Confirmed behavior from FSA

This layer handles:

- secure session initialization and validation
- persistent database-backed UI sessions
- subscription checks for monthly, promo, and day-pass access
- Terms of Service acceptance gating
- API-specific access control with JSON error responses
- logout invalidation and session cleanup

### Portfolio significance

This demonstrates production-grade access management rather than a toy login system.

---

## 2. Account Creation, Verification, and Recovery

**Confirmed files:**

- `/axialy-production-ui/var/www/html/axialy-ui/start_verification.php`
- `/axialy-production-ui/var/www/html/axialy-ui/verify_email.php`
- `/axialy-production-ui/var/www/html/axialy-ui/start_account_recovery.php`
- `/axialy-production-ui/var/www/html/axialy-ui/reset_password.php`
- `/axialy-production-ui/var/www/html/axialy-ui/includes/account_creation.php`
- `/axialy-production-ui/var/www/html/axialy-ui/includes/Mailer.php`

### Confirmed capabilities

The onboarding/recovery system supports:

- email verification token generation
- uniqueness checks for new accounts
- final account provisioning after verification
- password reset flows with expiring tokens
- transactional email dispatch via Postmark-oriented mail infrastructure

### Portfolio significance

This is strong evidence of end-to-end account lifecycle engineering.

---

## 3. Main Application Shell and SPA-Style Tab Loading

**Confirmed files:**

- `/axialy-production-ui/var/www/html/axialy-ui/index.php`
- `/axialy-production-ui/var/www/html/axialy-ui/js/layout.js`
- `/axialy-production-ui/var/www/html/axialy-ui/config/control-panel-menu.json`
- `/axialy-production-ui/var/www/html/axialy-ui/config/account-actions.json`
- `/axialy-production-ui/var/www/html/axialy-ui/config/support-actions.json`

### Confirmed architecture

The FSA indicates a modular application shell with:

- dynamic tab/content loading into an overview panel
- menu-driven navigation configuration via JSON
- coordinated CSS/JS asset loading per feature area
- shared account/support actions
- page-title and view synchronization utilities

### Portfolio significance

This demonstrates maintainable frontend architecture inside a PHP-hosted application shell.

---

## 4. AI-Driven Home / Generate Workflow

**Confirmed files:**

- `/axialy-production-ui/var/www/html/axialy-ui/content/home-tab.html`
- `/axialy-production-ui/var/www/html/axialy-ui/content/generate-tab.html`
- `/axialy-production-ui/var/www/html/axialy-ui/js/home/home-tab.js`
- `/axialy-production-ui/var/www/html/axialy-ui/js/process-feedback.js`
- `/axialy-production-ui/var/www/html/axialy-ui/js/input-text.js`
- `/axialy-production-ui/var/www/html/axialy-ui/js/focus-areas.js`
- `/axialy-production-ui/var/www/html/axialy-ui/js/dynamic-ribbons.js`
- `/axialy-production-ui/var/www/html/axialy-ui/store_summary.php`
- `/axialy-production-ui/var/www/html/axialy-ui/save_analysis_package.php`

### Confirmed capabilities from FSA

This workflow supports:

- collecting freeform user analysis input
- invoking AI-backed processing helpers
- choosing focus-area templates
- rendering structured ribbon/table outputs
- storing summary metadata
- saving generated content into reusable analysis packages

### Portfolio significance

This is one of the strongest product workflows in the repository because it demonstrates:

- AI-assisted workflow orchestration
- frontend stateful interaction design
- structured data capture from generative outputs
- persistence of generated work into versioned application entities

---

## 5. Analysis Package Management and Versioning

**Confirmed files:**

- `/axialy-production-ui/var/www/html/axialy-ui/save_analysis_package.php`
- `/axialy-production-ui/var/www/html/axialy-ui/save_data_existing_package.php`
- `/axialy-production-ui/var/www/html/axialy-ui/update_analysis_package.php`
- `/axialy-production-ui/var/www/html/axialy-ui/remove_analysis_package.php`
- `/axialy-production-ui/var/www/html/axialy-ui/recover_analysis_package.php`
- `/axialy-production-ui/var/www/html/axialy-ui/store_analysis_package_header.php`
- `/axialy-production-ui/var/www/html/axialy-ui/store_analysis_package_focus_area_version.php`
- `/axialy-production-ui/var/www/html/axialy-ui/get_analysis_packages_for_publish.php`
- `/axialy-production-ui/var/www/html/axialy-ui/get_package_data_for_revision.php`

### Confirmed capabilities

This subsystem demonstrates:

- package header creation/update
- soft delete and recovery patterns
- organization-aware package filtering
- focus-area version creation and tracking
- persistence of nested records under packages/focus areas/versions

### Portfolio significance

This shows deliberate data modeling, versioning, and lifecycle design.

---

## 6. Refine Workflow: Review, Edit, Enhance, Recover

**Confirmed files:**

- `/axialy-production-ui/var/www/html/axialy-ui/content/refine-tab.html`
- `/axialy-production-ui/var/www/html/axialy-ui/js/refine/index.js`
- `/axialy-production-ui/var/www/html/axialy-ui/js/refine/api.js`
- `/axialy-production-ui/var/www/html/axialy-ui/js/refine/ui.js`
- `/axialy-production-ui/var/www/html/axialy-ui/js/refine/events.js`
- `/axialy-production-ui/var/www/html/axialy-ui/js/refine/actions.js`
- `/axialy-production-ui/var/www/html/axialy-ui/js/refine/edit-record-overlay.js`
- `/axialy-production-ui/var/www/html/axialy-ui/js/refine/new-record-overlay.js`
- `/axialy-production-ui/var/www/html/axialy-ui/js/refine/augment-focus-area.js`
- `/axialy-production-ui/var/www/html/axialy-ui/js/refine/recover-focus-area.js`
- `/axialy-production-ui/var/www/html/axialy-ui/js/enhance-content.js`
- `/axialy-production-ui/var/www/html/axialy-ui/process_content_revision.php`
- `/axialy-production-ui/var/www/html/axialy-ui/process_delete_focus_area_data.php`
- `/axialy-production-ui/var/www/html/axialy-ui/process_recover_focus_area.php`
- `/axialy-production-ui/var/www/html/axialy-ui/save_enhanced_records.php`
- `/axialy-production-ui/var/www/html/axialy-ui/save_revised_records.php`

### Confirmed capabilities

The refine subsystem supports:

- browsing analysis packages with metrics
- editing existing focus-area records
- adding new records
- AI-assisted enhancement of existing content
- deletion with revision history preservation
- restoring historical focus-area versions
- resolving stakeholder feedback into revised records

### Portfolio significance

This is a rich example of version-controlled editorial tooling layered on top of AI-generated or AI-assisted content.

---

## 7. Axialy Advisor / Assessment Interfaces

**Confirmed files:**

- `/axialy-production-ui/var/www/html/axialy-ui/js/refine/axialyAssessmentModule.js`
- `/axialy-production-ui/var/www/html/axialy-ui/js/refine/axialyPackageAdvisorModule.js`
- `/axialy-production-ui/var/www/html/axialy-ui/api/get_analysis_packages_with_metrics.php`

### Confirmed capabilities

These modules demonstrate:

- package metric aggregation
- external AI analysis/assessment requests
- overlay-based presentation of recommendations
- actionable advisor outputs connected back into refinement workflows

### Portfolio significance

This shows how AI can be integrated not just for content generation, but for advisory/meta-analysis over user-created package data.

---

## 8. Stakeholder Feedback System

**Confirmed files:**

- `/axialy-production-ui/var/www/html/axialy-ui/process_content_review_request.php`
- `/axialy-production-ui/var/www/html/axialy-ui/receive_stakeholder_feedback.php`
- `/axialy-production-ui/var/www/html/axialy-ui/stakeholder-feedback/stakeholder-content-review.php`
- `/axialy-production-ui/var/www/html/axialy-ui/stakeholder-feedback/feedback-confirmation.php`
- `/axialy-production-ui/var/www/html/axialy-ui/stakeholder-feedback/feedback-form-request.php`
- `/axialy-production-ui/var/www/html/axialy-ui/send_stakeholder_reminder.php`
- `/axialy-production-ui/var/www/html/axialy-ui/cancel_stakeholder_feedback_request.php`
- `/axialy-production-ui/var/www/html/axialy-ui/fetch_stakeholder_feedback.php`
- `/axialy-production-ui/var/www/html/axialy-ui/fetch_feedback_details.php`
- `/axialy-production-ui/var/www/html/axialy-ui/get_survey_stakeholder_feedback_requests.php`
- `/axialy-production-ui/var/www/html/axialy-ui/fetch_survey_feedback_details.php`
- `/axialy-production-ui/var/www/html/axialy-ui/fetch_survey_feedback_details_responses.php`

### Confirmed capabilities from FSA

This subsystem supports:

- secure token + PIN-based stakeholder access
- no-account-required stakeholder participation
- general and itemized feedback forms
- pending-request tracking
- reminder email workflows
- cancellation of requests
- post-submission confirmation and UX feedback collection
- aggregation of stakeholder responses back into the product UI

### Portfolio significance

This is an especially strong portfolio artifact because it demonstrates a friction-reducing collaboration pattern that is both product-minded and technically implemented.

---

## 9. Survey / Dashboard Analytics Interfaces

**Confirmed files:**

- `/axialy-production-ui/var/www/html/axialy-ui/content/survey-tab.html`
- `/axialy-production-ui/var/www/html/axialy-ui/js/survey/api.js`
- `/axialy-production-ui/var/www/html/axialy-ui/js/survey/ui.js`
- `/axialy-production-ui/var/www/html/axialy-ui/js/survey/events.js`
- `/axialy-production-ui/var/www/html/axialy-ui/js/survey/modals.js`
- `/axialy-production-ui/var/www/html/axialy-ui/js/survey-collate-feedback.js`
- `/axialy-production-ui/var/www/html/axialy-ui/api/feedback_requests/organization.php`
- `/axialy-production-ui/var/www/html/axialy-ui/api/feedback_requests/status.php`
- `/axialy-production-ui/var/www/html/axialy-ui/api/stakeholder_feedback/data.php`

### Confirmed capabilities

The survey/dashboard tooling includes:

- filterable feedback-request tables
- organization/package/focus-area filtering
- modal inspection of feedback details
- reminder/cancel actions from dashboard workflows
- collated feedback processing
- chart-ready metrics APIs grouped by organization/status/stakeholder group

### Portfolio significance

This shows practical analytics and support/operations UX for a live stakeholder collaboration product.

---

## 10. Settings / Organization Management

**Confirmed files:**

- `/axialy-production-ui/var/www/html/axialy-ui/content/settings-tab.html`
- `/axialy-production-ui/var/www/html/axialy-ui/js/settings/api.js`
- `/axialy-production-ui/var/www/html/axialy-ui/js/settings/ui.js`
- `/axialy-production-ui/var/www/html/axialy-ui/js/settings/events.js`
- `/axialy-production-ui/var/www/html/axialy-ui/create_custom_organization.php`
- `/axialy-production-ui/var/www/html/axialy-ui/update_custom_organization.php`
- `/axialy-production-ui/var/www/html/axialy-ui/get_custom_organizations.php`
- `/axialy-production-ui/var/www/html/axialy-ui/get_focus_organization.php`
- `/axialy-production-ui/var/www/html/axialy-ui/update_focus_organization.php`
- `/axialy-production-ui/var/www/html/axialy-ui/serve_logo.php`

### Confirmed capabilities

This subsystem supports:

- custom organization creation/update
- organization context switching
- logo upload/storage and secure retrieval
- user-specific organization scoping across the app

### Notable implementation detail

The FSA explicitly describes S3-backed organization asset handling and access-controlled logo serving.

### Portfolio significance

This demonstrates multi-tenant / context-aware platform design rather than a single-tenant personal app.

---

## 11. Publish Workflow and Artifact Sharing

**Confirmed files:**

- `/axialy-production-ui/var/www/html/axialy-ui/content/publish-tab.html`
- `/axialy-production-ui/var/www/html/axialy-ui/js/publish/index.js`
- `/axialy-production-ui/var/www/html/axialy-ui/js/publish/api.js`
- `/axialy-production-ui/var/www/html/axialy-ui/js/publish/ui.js`
- `/axialy-production-ui/var/www/html/axialy-ui/js/publish/events.js`
- `/axialy-production-ui/var/www/html/axialy-ui/js/publish/events/expiry-management-events.js`
- `/axialy-production-ui/var/www/html/axialy-ui/js/publish/events/publication-settings-events.js`
- `/axialy-production-ui/var/www/html/axialy-ui/js/publish/events/stakeholder-invitation-events.js`
- `/axialy-production-ui/var/www/html/axialy-ui/process_html_for_publication.php`
- `/axialy-production-ui/var/www/html/axialy-ui/generate_publication_suggestions.php`
- `/axialy-production-ui/var/www/html/axialy-ui/generate_publication_artifact.php`
- `/axialy-production-ui/var/www/html/axialy-ui/publish_artifact.php`
- `/axialy-production-ui/var/www/html/axialy-ui/send_publication_invitations.php`
- `/axialy-production-ui/var/www/html/axialy-ui/get_published_artifacts.php`
- `/axialy-production-ui/var/www/html/axialy-ui/update_publication_expiry.php`
- `/axialy-production-ui/var/www/html/axialy-ui/view_publication.php`
- `/axialy-production-ui/var/www/html/axialy-ui/clone_published_artifact.php`

### Confirmed capabilities

The publication system supports:

- selecting packages/focus areas for publication
- generating publication suggestions/artifacts
- accepting raw custom HTML inputs for publication workflows
- sanitizing and preparing HTML for public delivery
- publishing artifacts with metadata and optional expiration
- inviting stakeholders via email with access tokens/PINs
- viewing artifacts as authenticated users or external invitees
- clone/reuse of published artifacts
- expiry management and publication metrics

### Portfolio significance

This is a compelling example of transforming internal structured analysis data into externally shareable deliverables.

---

## 12. Billing, Promo, and Offer Flows

**Confirmed files:**

- `/axialy-production-ui/var/www/html/axialy-ui/subscription.php`
- `/axialy-production-ui/var/www/html/axialy-ui/manage-subscription.php`
- `/axialy-production-ui/var/www/html/axialy-ui/create_subscription.php`
- `/axialy-production-ui/var/www/html/axialy-ui/redeem_promo_code.php`
- `/axialy-production-ui/var/www/html/axialy-ui/api/check-default-promo.php`
- `/axialy-production-ui/var/www/html/axialy-ui/js/promo-modal.js`
- `/axialy-production-ui/var/www/html/axialy-ui/offer/index.php`
- `/axialy-production-ui/var/www/html/axialy-ui/offer/api/validate_promo.php`
- `/axialy-production-ui/var/www/html/axialy-ui/offer/api/send_verification.php`
- `/axialy-production-ui/var/www/html/axialy-ui/offer/api/verify_code.php`
- `/axialy-production-ui/var/www/html/axialy-ui/offer/api/check_existing_user.php`
- `/axialy-production-ui/var/www/html/axialy-ui/offer/api/create_promo_subscription.php`
- `/axialy-production-ui/var/www/html/axialy-ui/offer/api/reactivate_subscription.php`
- `/axialy-production-ui/var/www/html/axialy-ui/webhooks/stripe.php`
- `/axialy-production-ui/var/www/html/axialy-ui/webhook.php`

### Confirmed capabilities from FSA

This billing layer demonstrates:

- Stripe-backed monthly subscriptions and day passes
- promotional code validation/redemption
- offer-specific signup/reactivation flows
- verification-code-based offer onboarding
- webhook-driven synchronization of subscription state
- account management and cancellation handling

### Portfolio significance

This shows production monetization plumbing rather than a hypothetical checkout demo.

---

## 13. Support Tickets and User Documentation

**Confirmed files:**

- `/axialy-production-ui/var/www/html/axialy-ui/issue_ajax_actions.php`
- `/axialy-production-ui/var/www/html/axialy-ui/submit_issue.php`
- `/axialy-production-ui/var/www/html/axialy-ui/js/support-tickets.js`
- `/axialy-production-ui/var/www/html/axialy-ui/user-documentation.php`
- `/axialy-production-ui/var/www/html/axialy-ui/docs/view_document.php`
- `/axialy-production-ui/var/www/html/axialy-ui/content/user-documentation.html`

### Confirmed capabilities

These areas provide:

- support-ticket listing/viewing/submission workflows
- in-app support overlays
- authenticated documentation portal delivery
- document rendering in multiple formats including Markdown/HTML/JSON/text and file delivery support for PDF/DOCX-like assets

### Portfolio significance

This demonstrates maturity in customer enablement and internal support tooling.

---

## 14. Marketing-Site Implementation Details Worth Discussing

**Confirmed files:**

- `/axialy-production-ui/var/www/html/axialy-marketing/js/main.js`
- `/axialy-production-ui/var/www/html/axialy-marketing/js/simple-metrics.js`
- `/axialy-production-ui/var/www/html/axialy-marketing/api/tableau-proxy.php`
- `/axialy-production-ui/var/www/html/axialy-marketing/data/schema.json`
- `/axialy-production-ui/var/www/html/axialy-marketing/sitemap.php`

### Confirmed implementation notes from FSA

The marketing surface includes:

- dynamic schema injection for SEO
- Tableau-related visualization support
- hardcoded server-side metrics proxying for quick dashboard figures
- JS-driven interaction effects and demo presentation
- dynamic sitemap generation

### Caveat

The FSA notes a duplicate `closeTableauDashboard` declaration in `axialy-marketing/js/main.js`, which may be worth discussing as a maintenance issue identified during documentation.

---

## Internal Documentation Present in the Repository

**Confirmed documentation files include:**

- `/axialy-production-ui/README.FSA.md`
- `/axialy-production-ui/var/www/html/axialy-ui/README.md`
- `/axialy-production-ui/var/www/html/axialy-ui/api/README.md`
- `/axialy-production-ui/var/www/html/axialy-ui/assets/README.md`
- `/axialy-production-ui/var/www/html/axialy-ui/assets/css/README.md`
- `/axialy-production-ui/var/www/html/axialy-ui/config/README.md`
- `/axialy-production-ui/var/www/html/axialy-ui/content/README.md`
- `/axialy-production-ui/var/www/html/axialy-ui/docs/README.md`
- `/axialy-production-ui/var/www/html/axialy-ui/includes/README.md`
- `/axialy-production-ui/var/www/html/axialy-ui/js/README.md`
- module-specific READMEs under `js/generate/`, `js/home/`, `js/modules/`, `js/publish/`, `js/refine/`, `js/settings/`
- `/axialy-production-ui/var/www/html/axialy-ui/stakeholder-feedback/README.md`
- `/axialy-production-ui/var/www/html/axialy-ui/vendor/README.md`
- `/axialy-production-ui/var/www/html/axialy-ui/webhooks/README.md`

### Why this matters

This repository preserves not only implementation artifacts but also a large amount of technical explanation. That is valuable from a portfolio perspective because it demonstrates:

- maintainability discipline
- system explanation skills
- modular architectural thinking
- developer-facing documentation habits

---

## Referenced Sensitive / Runtime Dependencies

The FSA identifies several runtime-sensitive or environment-driven files/services, including:

- `/axialy-production-ui/var/www/html/axialy-ui/.env`
- `/var/www/html/.env.master`
- `/etc/mfp/api_key`
- `/etc/mfp/allowed_root`
- Stripe/Postmark credentials loaded through config/env files
- S3/AWS CLI interactions for logo storage
- helper binaries such as `/usr/local/sbin/mfp-apro-install-file` and `/usr/local/sbin/mfp-apro-archive-file`

### Important caveat

These should be understood as **architectural/runtime dependencies**, not public-facing routes or ordinary portfolio pages.

---

## Public / Demo Discussion Value

Strong demo or discussion topics for employers include:

- the PIN-based stakeholder engagement architecture
- AI-assisted package generation and refinement flows
- how focus-area versioning preserves historical records
- how publication artifacts are generated and shared externally
- how organization context affects filtering and permissions
- how Stripe subscriptions, promos, and offers are handled
- how documentation and support are embedded into the product
- how marketing pages complement the main SaaS application
- how the operational `admin-api` supports deployment/file workflows

---

## Relationship to `/axialy-production-admin/README.md`

This repository should be interpreted alongside:

- `/axialy-production-admin/README.md`

The two repositories describe complementary production surfaces:

- **`axialy-production-ui`** = customer-facing platform, marketing, stakeholder collaboration, billing, publication
- **`axialy-production-admin`** = administrative control plane, operational CRUD workflows, document/promo/support management, deployment/file API

Together they show both:

- product-facing SaaS delivery, and
- operational/admin infrastructure required to run that product.

---

## Relationship to `/p3plzcpnl503722/README.md`

This repository also complements the broader legacy hosting snapshot documented at:

- `/p3plzcpnl503722/README.md`

That legacy repository demonstrates multi-product breadth across Axiamax, AxiaBA, EZAPP, APRO, REELY, CAMPS, Imagery, and SimChart on shared hosting. By contrast, **`axialy-production-ui`** shows a more focused, modern AWS-hosted production product environment for Axialy AI.

This progression is valuable in a portfolio context because it shows:

- earlier breadth across many products and prototypes, and
- later depth in a productionized, subscription-aware, collaboration-focused SaaS platform.

---

## Limitations of This Snapshot

This repository is a **downloaded server snapshot**, not a full operational backup. As a result:

- exact cloud networking and DNS details are only partially visible
- secrets and live environment values may be omitted/redacted
- some behavior depends on external APIs and runtime services
- some referenced endpoints/modules may rely on global JS loading order not obvious from isolated file views
- a few files in the snapshot are clearly diagnostic/test-oriented rather than core product files
- at least one analyzed file (`fetch_stakeholder_details.php`) was not available in content form in the FSA and therefore is not suitable for strong claims

Where this README makes strong statements, they are grounded in the explicit purposes documented in `/axialy-production-ui/README.FSA.md`.

---

## Summary

`axialy-production-ui` is a substantial production UI/server snapshot for the Axialy platform.

It demonstrates:

- authenticated SaaS application architecture
- AI-assisted business analysis generation and refinement
- versioned package/focus-area lifecycle management
- PIN-based external stakeholder collaboration
- publication/share workflows for analysis artifacts
- multi-tenant organization management
- Stripe-based billing and promo flows
- embedded documentation and support tooling
- public marketing/SEO delivery on the same host
- operational file/deployment API support

As a portfolio artifact, it is especially valuable because it shows a real product ecosystem: acquisition, onboarding, usage, collaboration, billing, support, and publish/share workflows all preserved in one production-oriented server snapshot.