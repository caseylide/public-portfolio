File System Analysis (APRO):

Analyzed file count: 306 / 310

-------------------------------------------------
File #1
Path: /axialy-production-ui/var/www/html/admin-api/.htaccess

Referenced files:
  - /axialy-production-ui/var/www/html/admin-api/index.php

Purpose:
This .htaccess file serves as the front-controller configuration for the admin-api directory. It instructs the Apache web server to route all incoming requests that do not map to an existing physical file or directory to 'index.php'. This pattern is standard for implementing a single-entry-point architecture, where all API requests are handled by the application logic contained within index.php.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/admin-api/index.php"
  ],
  "purpose": "This .htaccess file serves as the front-controller configuration for the admin-api directory. It instructs the Apache web server to route all incoming requests that do not map to an existing physical file or directory to 'index.php'. This pattern is standard for implementing a single-entry-point architecture, where all API requests are handled by the application logic contained within index.php."
}
```

-------------------------------------------------
File #2
Path: /axialy-production-ui/var/www/html/admin-api/index.php

Referenced files:
  - /etc/mfp/api_key
  - /etc/mfp/allowed_root
  - /var/www/html/.env.master
  - /var/www/html
  - /srv/maxflex/public_html
  - /usr/local/sbin/mfp-apro-install-file
  - /usr/local/sbin/mfp-apro-archive-file

Purpose:
This file acts as a centralized administrative API gateway for the system, responsible for managing file operations, application deployments, and environment configurations. Its core functionality includes: 1) Providing an authenticated JSON-based interface (via API key verification) to navigate the file system, read files, and manage directory structures. 2) Facilitating safe deployment by extracting tar.gz packages to a staging area and installing them to specific destination paths, often utilizing privileged system helpers (/usr/local/sbin/...) for file operations requiring elevated permissions. 3) Providing versioning support by automatically creating timestamped or versioned archives of files before modification or during manual archival. 4) Managing environment settings by allowing the atomic update of the '.env.master' file. The script enforces strict security measures, including path normalization to prevent directory traversal and restricting access to an allowed root directory defined in /etc/mfp/allowed_root.

Raw AI response:
{
  "referenced_files": [
    "/etc/mfp/api_key",
    "/etc/mfp/allowed_root",
    "/var/www/html/.env.master",
    "/var/www/html",
    "/srv/maxflex/public_html",
    "/usr/local/sbin/mfp-apro-install-file",
    "/usr/local/sbin/mfp-apro-archive-file"
  ],
  "purpose": "This file acts as a centralized administrative API gateway for the system, responsible for managing file operations, application deployments, and environment configurations. Its core functionality includes: 1) Providing an authenticated JSON-based interface (via API key verification) to navigate the file system, read files, and manage directory structures. 2) Facilitating safe deployment by extracting tar.gz packages to a staging area and installing them to specific destination paths, often utilizing privileged system helpers (/usr/local/sbin/...) for file operations requiring elevated permissions. 3) Providing versioning support by automatically creating timestamped or versioned archives of files before modification or during manual archival. 4) Managing environment settings by allowing the atomic update of the '.env.master' file. The script enforces strict security measures, including path normalization to prevent directory traversal and restricting access to an allowed root directory defined in /etc/mfp/allowed_root."
}

-------------------------------------------------
File #3
Path: /axialy-production-ui/var/www/html/axialy-marketing/ai-stakeholder-feedback-platform/index.php

Referenced files:
  - /favicon.ico

Purpose:
This file serves as a public-facing SEO landing page for the 'Axialy AI Stakeholder Feedback Platform.' Its primary function is to capture traffic for keywords related to stakeholder feedback tools by highlighting the pain points of traditional systems and promoting the platform's key features, specifically its PIN-based, no-account-required access model. It includes structural marketing content (features, benefits, use cases) and technical metadata (JSON-LD) to improve search engine visibility and drive conversions via call-to-action links.

Raw AI response:
```json
{
  "referenced_files": [
    "/favicon.ico"
  ],
  "purpose": "This file serves as a public-facing SEO landing page for the 'Axialy AI Stakeholder Feedback Platform.' Its primary function is to capture traffic for keywords related to stakeholder feedback tools by highlighting the pain points of traditional systems and promoting the platform's key features, specifically its PIN-based, no-account-required access model. It includes structural marketing content (features, benefits, use cases) and technical metadata (JSON-LD) to improve search engine visibility and drive conversions via call-to-action links."
}
```

-------------------------------------------------
File #4
Path: /axialy-production-ui/var/www/html/axialy-marketing/api/tableau-proxy.php

Referenced files:
  (none)

Purpose:
This file acts as a lightweight, static API endpoint that serves hardcoded business metrics (use cases, user actions, and user types) related to the 'AxialyAIPlatformRolesandCapabilities' Tableau workbook. It is designed to provide quick, cached access to these figures for the frontend without requiring a live connection to Tableau Server. The metrics are manually maintained within the code, and the file includes CORS headers to allow cross-origin requests.

Raw AI response:
```json
{
  "referenced_files": [],
  "purpose": "This file acts as a lightweight, static API endpoint that serves hardcoded business metrics (use cases, user actions, and user types) related to the 'AxialyAIPlatformRolesandCapabilities' Tableau workbook. It is designed to provide quick, cached access to these figures for the frontend without requiring a live connection to Tableau Server. The metrics are manually maintained within the code, and the file includes CORS headers to allow cross-origin requests."
}
```

-------------------------------------------------
File #5
Path: /axialy-production-ui/var/www/html/axialy-marketing/assets/img/axialy_icon.png

Referenced files:
  (none)

Purpose:
This file is a PNG image file containing the Axialy brand icon. Within the system, it serves as a static visual asset, likely used for branding in the production marketing interface, such as a site favicon, header logo, or UI element.

Raw AI response:
{
  "referenced_files": [],
  "purpose": "This file is a PNG image file containing the Axialy brand icon. Within the system, it serves as a static visual asset, likely used for branding in the production marketing interface, such as a site favicon, header logo, or UI element."
}

-------------------------------------------------
File #6
Path: /axialy-production-ui/var/www/html/axialy-marketing/assets/img/README.md

Referenced files:
  (none)

Purpose:
This file is a README document located within the assets/img directory of the axialy-marketing project. Based on its location, it likely serves as documentation for developers or designers regarding the image assets, such as guidelines for image formats, compression standards, naming conventions, or copyright information for the media stored in this directory.

Raw AI response:
{
  "referenced_files": [],
  "purpose": "This file is a README document located within the assets/img directory of the axialy-marketing project. Based on its location, it likely serves as documentation for developers or designers regarding the image assets, such as guidelines for image formats, compression standards, naming conventions, or copyright information for the media stored in this directory."
}

-------------------------------------------------
File #7
Path: /axialy-production-ui/var/www/html/axialy-marketing/automated-business-planning/index.php

Referenced files:
  - /favicon.ico

Purpose:
This file serves as a public-facing marketing landing page for the 'Axialy AI Automated Business Planning' software. It is designed to explain the value proposition of the product, detail its core features (such as AI-driven plan generation and stakeholder collaboration), and convert visitors into trial users or consulting leads. The file uses PHP to set cache headers and provides structured JSON-LD data to improve SEO, while utilizing internal CSS for layout and styling.

Raw AI response:
{
  "referenced_files": [
    "/favicon.ico"
  ],
  "purpose": "This file serves as a public-facing marketing landing page for the 'Axialy AI Automated Business Planning' software. It is designed to explain the value proposition of the product, detail its core features (such as AI-driven plan generation and stakeholder collaboration), and convert visitors into trial users or consulting leads. The file uses PHP to set cache headers and provides structured JSON-LD data to improve SEO, while utilizing internal CSS for layout and styling."
}

-------------------------------------------------
File #8
Path: /axialy-production-ui/var/www/html/axialy-marketing/business-analysis-software/index.php

Referenced files:
  (none)

Purpose:
This file serves as a public-facing landing page for the 'Business Analysis Software' product provided by Axialy. It is a static HTML document designed for marketing and search engine optimization (SEO). Its primary purpose is to outline the features of the AI-powered platform, provide social proof, and drive conversions by encouraging users to sign up for a free trial or seek expert implementation consulting through the partner domain 'axiaba.com'. The file includes structured JSON-LD data to assist search engines in indexing the application as a software product.

Raw AI response:
{
  "referenced_files": [],
  "purpose": "This file serves as a public-facing landing page for the 'Business Analysis Software' product provided by Axialy. It is a static HTML document designed for marketing and search engine optimization (SEO). Its primary purpose is to outline the features of the AI-powered platform, provide social proof, and drive conversions by encouraging users to sign up for a free trial or seek expert implementation consulting through the partner domain 'axiaba.com'. The file includes structured JSON-LD data to assist search engines in indexing the application as a software product."
}

-------------------------------------------------
File #9
Path: /axialy-production-ui/var/www/html/axialy-marketing/casey-lide/index.html

Referenced files:
  - https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap
  - https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css
  - https://axiaba.com/assets/img/axialy_icon.png

Purpose:
This file is a standalone static HTML bio/profile page for Casey Lide, the Founder & CEO of Axialy AI. Its primary purpose is to serve as a marketing and professional landing page that highlights Casey's expertise, accomplishments, and professional background. It links to external organizational sites (Axialy AI, AxiaBA Consulting, and Axiamax LLC) and provides contact information, functioning as a professional digital resume within the Axialy marketing web directory.

Raw AI response:
```json
{
  "referenced_files": [
    "https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap",
    "https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css",
    "https://axiaba.com/assets/img/axialy_icon.png"
  ],
  "purpose": "This file is a standalone static HTML bio/profile page for Casey Lide, the Founder & CEO of Axialy AI. Its primary purpose is to serve as a marketing and professional landing page that highlights Casey's expertise, accomplishments, and professional background. It links to external organizational sites (Axialy AI, AxiaBA Consulting, and Axiamax LLC) and provides contact information, functioning as a professional digital resume within the Axialy marketing web directory."
}
```

-------------------------------------------------
File #10
Path: /axialy-production-ui/var/www/html/axialy-marketing/collaborative-analysis-platform/index.html

Referenced files:
  - /favicon.ico

Purpose:
This file is the public-facing marketing landing page for the 'Axialy Collaborative Analysis Platform.' Its primary function is to educate potential users on the value proposition of the platform—specifically its ability to increase stakeholder participation through PIN-based access—and to drive user acquisition via 'Free Trial' and 'Schedule Demo' calls-to-action. It utilizes SEO metadata, JSON-LD for search engine indexing, and structured feature comparisons to position the software as a solution to common business analysis inefficiencies.

Raw AI response:
{
  "referenced_files": [
    "/favicon.ico"
  ],
  "purpose": "This file is the public-facing marketing landing page for the 'Axialy Collaborative Analysis Platform.' Its primary function is to educate potential users on the value proposition of the platform—specifically its ability to increase stakeholder participation through PIN-based access—and to drive user acquisition via 'Free Trial' and 'Schedule Demo' calls-to-action. It utilizes SEO metadata, JSON-LD for search engine indexing, and structured feature comparisons to position the software as a solution to common business analysis inefficiencies."
}

-------------------------------------------------
File #11
Path: /axialy-production-ui/var/www/html/axialy-marketing/css/styles.css

Referenced files:
  (none)

Purpose:
This file is a central CSS stylesheet for the Axialy marketing landing page. It defines the visual identity of the site, including a modern 'dark mode' color palette using CSS custom properties, responsive layout structures, and specific styles for key UI components like a fixed navigation bar, hero section with animated background, feature grids, embedded video containers, and a modal for Tableau dashboard integration. It also includes media queries for mobile responsiveness and utility classes for scroll-triggered animations.

Raw AI response:
{
  "referenced_files": [],
  "purpose": "This file is a central CSS stylesheet for the Axialy marketing landing page. It defines the visual identity of the site, including a modern 'dark mode' color palette using CSS custom properties, responsive layout structures, and specific styles for key UI components like a fixed navigation bar, hero section with animated background, feature grids, embedded video containers, and a modal for Tableau dashboard integration. It also includes media queries for mobile responsiveness and utility classes for scroll-triggered animations."
}

-------------------------------------------------
File #12
Path: /axialy-production-ui/var/www/html/axialy-marketing/data/schema.json

Referenced files:
  (none)

Purpose:
This file serves as a structured JSON-LD (Linked Data) document defining the organizational metadata for 'Axialy AI'. It is designed to be injected into the website's frontend to provide search engines with semantic information, including the organization's identity, contact points, parent company, and service nature. By adhering to the schema.org vocabulary, it improves the search engine optimization (SEO) and representation of the platform in search results. No internal file paths are referenced within this JSON structure.

Raw AI response:
```json
{
  "referenced_files": [],
  "purpose": "This file serves as a structured JSON-LD (Linked Data) document defining the organizational metadata for 'Axialy AI'. It is designed to be injected into the website's frontend to provide search engines with semantic information, including the organization's identity, contact points, parent company, and service nature. By adhering to the schema.org vocabulary, it improves the search engine optimization (SEO) and representation of the platform in search results. No internal file paths are referenced within this JSON structure."
}
```

-------------------------------------------------
File #13
Path: /axialy-production-ui/var/www/html/axialy-marketing/demo/index.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-marketing/favicon.ico
  - /axialy-production-ui/var/www/html/axialy-marketing/assets/img/axialy_icon.png
  - /axialy-production-ui/var/www/html/axialy-marketing/css/styles.css
  - /axialy-production-ui/var/www/html/axialy-marketing/team/index.php

Purpose:
This file serves as a dedicated landing page for the Axialy AI platform, designed specifically for marketing campaigns. It hosts an embedded YouTube demo video (configured via PHP variables) and provides a conversion-focused interface that includes a Call-to-Action (CTA) section for starting a free trial or scheduling a personalized demo. The file relies on external assets (CSS and images) located in parent directories and uses internal PHP logic to dynamically control the video display parameters.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-marketing/favicon.ico",
    "/axialy-production-ui/var/www/html/axialy-marketing/assets/img/axialy_icon.png",
    "/axialy-production-ui/var/www/html/axialy-marketing/css/styles.css",
    "/axialy-production-ui/var/www/html/axialy-marketing/team/index.php"
  ],
  "purpose": "This file serves as a dedicated landing page for the Axialy AI platform, designed specifically for marketing campaigns. It hosts an embedded YouTube demo video (configured via PHP variables) and provides a conversion-focused interface that includes a Call-to-Action (CTA) section for starting a free trial or scheduling a personalized demo. The file relies on external assets (CSS and images) located in parent directories and uses internal PHP logic to dynamically control the video display parameters."
}
```

-------------------------------------------------
File #14
Path: /axialy-production-ui/var/www/html/axialy-marketing/js/main.js

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-marketing/data/schema.json
  - https://public.tableau.com/javascripts/api/viz_v1.js

Purpose:
The file acts as the primary client-side JavaScript controller for the Axialy AI marketing website. Its core responsibilities include managing UI-level interactive features such as scroll animations (IntersectionObserver), smooth navigation, and a simulated typing effect for product demonstrations. Furthermore, it handles the dynamic loading of structured SEO data from a local JSON file and manages the lifecycle of a Tableau-based data dashboard, including modal visibility, responsive sizing of embedded visualizations, and integration with an external metrics-tracking object (AxialyMetricsUpdater). Note: The file contains a duplicate declaration of the 'closeTableauDashboard' function, which may cause unexpected behavior in some environments.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-marketing/data/schema.json",
    "https://public.tableau.com/javascripts/api/viz_v1.js"
  ],
  "purpose": "The file acts as the primary client-side JavaScript controller for the Axialy AI marketing website. Its core responsibilities include managing UI-level interactive features such as scroll animations (IntersectionObserver), smooth navigation, and a simulated typing effect for product demonstrations. Furthermore, it handles the dynamic loading of structured SEO data from a local JSON file and manages the lifecycle of a Tableau-based data dashboard, including modal visibility, responsive sizing of embedded visualizations, and integration with an external metrics-tracking object (AxialyMetricsUpdater). Note: The file contains a duplicate declaration of the 'closeTableauDashboard' function, which may cause unexpected behavior in some environments."
}
```

-------------------------------------------------
File #15
Path: /axialy-production-ui/var/www/html/axialy-marketing/js/simple-metrics.js

Referenced files:
  (none)

Purpose:
The file defines a JavaScript class, 'ServerMetricsUpdater', responsible for updating specific HTML elements on a webpage with hardcoded numerical data representing 'Axialy AI Metrics'. The system is designed to display metrics derived from a Tableau workbook. It provides an initialization method that runs on page load and exposes global functions to allow for manual updates of these metrics (use cases, user actions, and user types) after the initial render.

Raw AI response:
```json
{
  "referenced_files": [],
  "purpose": "The file defines a JavaScript class, 'ServerMetricsUpdater', responsible for updating specific HTML elements on a webpage with hardcoded numerical data representing 'Axialy AI Metrics'. The system is designed to display metrics derived from a Tableau workbook. It provides an initialization method that runs on page load and exposes global functions to allow for manual updates of these metrics (use cases, user actions, and user types) after the initial render."
}
```

-------------------------------------------------
File #16
Path: /axialy-production-ui/var/www/html/axialy-marketing/requirements-gathering-tools/index.php

Referenced files:
  - /favicon.ico

Purpose:
This file acts as a public-facing marketing landing page for the 'Axialy AI' requirements gathering platform. It is designed to educate potential users on the pain points of traditional requirements gathering and how the platform's AI-driven features (such as PIN-based stakeholder access and automated documentation) solve these issues. It includes SEO metadata, JSON-LD structured data for business software, and various call-to-action buttons to convert visitors into platform users or consulting clients via external links.

Raw AI response:
```json
{
  "referenced_files": [
    "/favicon.ico"
  ],
  "purpose": "This file acts as a public-facing marketing landing page for the 'Axialy AI' requirements gathering platform. It is designed to educate potential users on the pain points of traditional requirements gathering and how the platform's AI-driven features (such as PIN-based stakeholder access and automated documentation) solve these issues. It includes SEO metadata, JSON-LD structured data for business software, and various call-to-action buttons to convert visitors into platform users or consulting clients via external links."
}
```

-------------------------------------------------
File #17
Path: /axialy-production-ui/var/www/html/axialy-marketing/team/index.html

Referenced files:
  - https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap
  - https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css
  - https://axiaba.com/assets/img/axialy_icon.png
  - /casey-lide/
  - /

Purpose:
This file is a static HTML page serving as a 'Leadership Team' profile page for the Axialy AI marketing site. It provides information about the founder, Casey Lide, highlighting his role in developing the platform and his background in business analysis. The page is styled using a modern, dark-themed UI with responsive CSS and utilizes external libraries for fonts and icons.

Raw AI response:
{
  "referenced_files": [
    "https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap",
    "https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css",
    "https://axiaba.com/assets/img/axialy_icon.png",
    "/casey-lide/",
    "/"
  ],
  "purpose": "This file is a static HTML page serving as a 'Leadership Team' profile page for the Axialy AI marketing site. It provides information about the founder, Casey Lide, highlighting his role in developing the platform and his background in business analysis. The page is styled using a modern, dark-themed UI with responsive CSS and utilizes external libraries for fonts and icons."
}

-------------------------------------------------
File #18
Path: /axialy-production-ui/var/www/html/axialy-marketing/.htaccess

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-marketing/sitemap.php

Purpose:
This .htaccess file serves as a configuration file for the Apache web server within the axialy-marketing directory. Its primary functional purpose is to perform URL rewriting, specifically intercepting requests for 'sitemap.xml' and internally routing them to 'sitemap.php', allowing the application to dynamically generate sitemap content while exposing a static-looking URL to search engines and users.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-marketing/sitemap.php"
  ],
  "purpose": "This .htaccess file serves as a configuration file for the Apache web server within the axialy-marketing directory. Its primary functional purpose is to perform URL rewriting, specifically intercepting requests for 'sitemap.xml' and internally routing them to 'sitemap.php', allowing the application to dynamically generate sitemap content while exposing a static-looking URL to search engines and users."
}
```

-------------------------------------------------
File #19
Path: /axialy-production-ui/var/www/html/axialy-marketing/favicon.ico

Referenced files:
  (none)

Purpose:
This file is a favicon.ico, which serves as the visual icon for the website displayed in the browser's tab, address bar, or bookmarks menu. It is a standard binary resource file used for branding and site identification within the /axialy-marketing/ directory.

Raw AI response:
{
  "referenced_files": [],
  "purpose": "This file is a favicon.ico, which serves as the visual icon for the website displayed in the browser's tab, address bar, or bookmarks menu. It is a standard binary resource file used for branding and site identification within the /axialy-marketing/ directory."
}

-------------------------------------------------
File #20
Path: /axialy-production-ui/var/www/html/axialy-marketing/index.php

Referenced files:
  - /css/styles.css
  - js/main.js
  - js/simple-metrics.js

Purpose:
This file serves as the main landing page and marketing site for the Axialy AI platform. It provides a public-facing overview of the product's features, serves as a hub for directing users to the application UI, and highlights consulting and investment opportunities related to the Axiamax LLC ecosystem. The file includes a PHP-driven configuration for a YouTube video embed and integrates a Tableau dashboard for visual demonstration of platform capabilities. Note that while this file references local assets like 'css/styles.css' and 'js/main.js', the actual contents of those files were not provided.

Raw AI response:
```json
{
  "referenced_files": [
    "/css/styles.css",
    "js/main.js",
    "js/simple-metrics.js"
  ],
  "purpose": "This file serves as the main landing page and marketing site for the Axialy AI platform. It provides a public-facing overview of the product's features, serves as a hub for directing users to the application UI, and highlights consulting and investment opportunities related to the Axiamax LLC ecosystem. The file includes a PHP-driven configuration for a YouTube video embed and integrates a Tableau dashboard for visual demonstration of platform capabilities. Note that while this file references local assets like 'css/styles.css' and 'js/main.js', the actual contents of those files were not provided."
}
```

-------------------------------------------------
File #21
Path: /axialy-production-ui/var/www/html/axialy-marketing/README.md

Referenced files:
  (none)

Purpose:
The file is an empty README.md document located in the marketing directory of the production UI environment. As it currently contains no text, it provides no documentation, configuration, or structural instructions for the system.

Raw AI response:
{
  "referenced_files": [],
  "purpose": "The file is an empty README.md document located in the marketing directory of the production UI environment. As it currently contains no text, it provides no documentation, configuration, or structural instructions for the system."
}

-------------------------------------------------
File #22
Path: /axialy-production-ui/var/www/html/axialy-marketing/sitemap.php

Referenced files:
  (none)

Purpose:
The file acts as a dynamic sitemap generator for the axialy.ai marketing website. It programmatically scans the filesystem within its directory to identify subdirectories containing 'index.php' or 'index.html' files, excluding common assets and hidden folders. It then generates an XML-formatted sitemap (compatible with search engine indexing standards) on-the-fly, including the homepage and all discovered page directories with appropriate SEO metadata like priority, change frequency, and last modification dates. It does not explicitly include or require external files, relying solely on native PHP directory traversal functions.

Raw AI response:
```json
{
  "referenced_files": [],
  "purpose": "The file acts as a dynamic sitemap generator for the axialy.ai marketing website. It programmatically scans the filesystem within its directory to identify subdirectories containing 'index.php' or 'index.html' files, excluding common assets and hidden folders. It then generates an XML-formatted sitemap (compatible with search engine indexing standards) on-the-fly, including the homepage and all discovered page directories with appropriate SEO metadata like priority, change frequency, and last modification dates. It does not explicitly include or require external files, relying solely on native PHP directory traversal functions."
}
```

-------------------------------------------------
File #23
Path: /axialy-production-ui/var/www/html/axialy-marketing/test.php

Referenced files:
  (none)

Purpose:
This file serves as a simple diagnostic script to verify that the PHP environment is correctly configured and operational within the axialy.ai web server context. It outputs a confirmation message and the current server system time.

Raw AI response:
```json
{
  "referenced_files": [],
  "purpose": "This file serves as a simple diagnostic script to verify that the PHP environment is correctly configured and operational within the axialy.ai web server context. It outputs a confirmation message and the current server system time."
}
```

-------------------------------------------------
File #24
Path: /axialy-production-ui/var/www/html/axialy-ui/api/feedback_requests/organization.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/api_auth.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/debug_utils.php

Purpose:
This file serves as a JSON API endpoint that provides aggregated feedback request counts grouped by organization. It supports optional filtering by status ('Sent' or 'Responded') via a query parameter. The script validates user authentication through internal include files, executes SQL queries to join feedback header data with organization definitions, and returns the data in a format suitable for charting (labels and values arrays).

Raw AI response:
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/api_auth.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/debug_utils.php"
  ],
  "purpose": "This file serves as a JSON API endpoint that provides aggregated feedback request counts grouped by organization. It supports optional filtering by status ('Sent' or 'Responded') via a query parameter. The script validates user authentication through internal include files, executes SQL queries to join feedback header data with organization definitions, and returns the data in a format suitable for charting (labels and values arrays)."
}

-------------------------------------------------
File #25
Path: /axialy-production-ui/var/www/html/axialy-ui/api/feedback_requests/README.md

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/api/feedback_requests/organization.php
  - /axialy-production-ui/var/www/html/axialy-ui/api/feedback_requests/status.php

Purpose:
This file serves as documentation for the /api/feedback_requests API directory. It outlines the functionality of the two included PHP scripts, which provide aggregated, chart-ready data concerning stakeholder feedback requests—categorized by either organization or request status—for use by the frontend dashboard.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/api/feedback_requests/organization.php",
    "/axialy-production-ui/var/www/html/axialy-ui/api/feedback_requests/status.php"
  ],
  "purpose": "This file serves as documentation for the /api/feedback_requests API directory. It outlines the functionality of the two included PHP scripts, which provide aggregated, chart-ready data concerning stakeholder feedback requests—categorized by either organization or request status—for use by the frontend dashboard."
}
```

-------------------------------------------------
File #26
Path: /axialy-production-ui/var/www/html/axialy-ui/api/feedback_requests/status.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/api_auth.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/debug_utils.php

Purpose:
This script functions as a JSON API endpoint that provides aggregated statistics on stakeholder feedback requests. It classifies feedback as either 'Sent' or 'Responded' based on the presence of a timestamp in the 'responded_at' column of the 'stakeholder_feedback_headers' table. The endpoint supports filtering these counts by a specific organization via a query parameter, or returning the global totals if no organization is specified.

Raw AI response:
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/api_auth.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/debug_utils.php"
  ],
  "purpose": "This script functions as a JSON API endpoint that provides aggregated statistics on stakeholder feedback requests. It classifies feedback as either 'Sent' or 'Responded' based on the presence of a timestamp in the 'responded_at' column of the 'stakeholder_feedback_headers' table. The endpoint supports filtering these counts by a specific organization via a query parameter, or returning the global totals if no organization is specified."
}

-------------------------------------------------
File #27
Path: /axialy-production-ui/var/www/html/axialy-ui/api/stakeholder_feedback/data.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/api_auth.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/debug_utils.php

Purpose:
This file serves as a JSON API endpoint that provides aggregated stakeholder feedback data. It queries the database to count feedback records grouped by 'stakeholder_group' and returns the results as a pair of labels and values, suitable for visualization (e.g., in a chart). The script enforces API access control and includes error handling/logging mechanisms.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/api_auth.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/debug_utils.php"
  ],
  "purpose": "This file serves as a JSON API endpoint that provides aggregated stakeholder feedback data. It queries the database to count feedback records grouped by 'stakeholder_group' and returns the results as a pair of labels and values, suitable for visualization (e.g., in a chart). The script enforces API access control and includes error handling/logging mechanisms."
}
```

-------------------------------------------------
File #28
Path: /axialy-production-ui/var/www/html/axialy-ui/api/stakeholder_feedback/README.md

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/api/stakeholder_feedback/data.php

Purpose:
This README file acts as documentation for the `/api/stakeholder_feedback` directory. Its primary purpose is to define the interface and data structure provided by the `data.php` endpoint, which aggregates stakeholder feedback records for use in UI visualizations such as pie or bar charts.

Raw AI response:
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/api/stakeholder_feedback/data.php"
  ],
  "purpose": "This README file acts as documentation for the `/api/stakeholder_feedback` directory. Its primary purpose is to define the interface and data structure provided by the `data.php` endpoint, which aggregates stakeholder feedback records for use in UI visualizations such as pie or bar charts."
}

-------------------------------------------------
File #29
Path: /axialy-production-ui/var/www/html/axialy-ui/api/check-default-promo.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/Config.php
  - /axialy-production-ui/var/www/html/axialy-ui/vendor/autoload.php

Purpose:
This file serves as a backend API endpoint that validates promotional codes provided via a POST request. It checks for the existence, activity status, expiration dates, and usage limits of a promo code within the local `promo_codes` database table. If valid, it fetches corresponding pricing details from Stripe—specifically comparing a promotional price ID against a standard subscription price ID—and returns a JSON response containing pricing info, potential savings, and relevant legal/disclosure text to be displayed in a UI modal.

Raw AI response:
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/Config.php",
    "/axialy-production-ui/var/www/html/axialy-ui/vendor/autoload.php"
  ],
  "purpose": "This file serves as a backend API endpoint that validates promotional codes provided via a POST request. It checks for the existence, activity status, expiration dates, and usage limits of a promo code within the local `promo_codes` database table. If valid, it fetches corresponding pricing details from Stripe—specifically comparing a promotional price ID against a standard subscription price ID—and returns a JSON response containing pricing info, potential savings, and relevant legal/disclosure text to be displayed in a UI modal."
}

-------------------------------------------------
File #30
Path: /axialy-production-ui/var/www/html/axialy-ui/api/get_analysis_packages_with_metrics.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/api_auth.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/auth.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/focus_org_session.php

Purpose:
This PHP script serves as an API endpoint to retrieve a list of 'analysis packages' (from the `analysis_package_headers` table) filtered by a user-provided search term and scoped to the user's current organization. For every retrieved package, the script executes multiple analytical queries to aggregate metrics including counts of focus areas, records, data objects, total inputs, stakeholder feedback requests, responses, unique responding stakeholders, and unreviewed feedback items. It returns the combined header data and these calculated metrics as a JSON response.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/api_auth.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/auth.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/focus_org_session.php"
  ],
  "purpose": "This PHP script serves as an API endpoint to retrieve a list of 'analysis packages' (from the `analysis_package_headers` table) filtered by a user-provided search term and scoped to the user's current organization. For every retrieved package, the script executes multiple analytical queries to aggregate metrics including counts of focus areas, records, data objects, total inputs, stakeholder feedback requests, responses, unique responding stakeholders, and unreviewed feedback items. It returns the combined header data and these calculated metrics as a JSON response."
}
```

-------------------------------------------------
File #31
Path: /axialy-production-ui/var/www/html/axialy-ui/api/README.md

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/api/get_analysis_packages_with_metrics.php
  - /axialy-production-ui/var/www/html/axialy-ui/api/feedback_requests/README.md
  - /axialy-production-ui/var/www/html/axialy-ui/api/stakeholder_feedback/README.md

Purpose:
This README serves as the primary documentation for the API layer of the Axialy UI. It provides an overview of backend endpoints responsible for fetching and aggregating data, specifically for analysis packages, feedback request summaries, and raw stakeholder feedback metrics. The file acts as a manifest for the directory's functionality and guides developers to sub-directories for more granular API documentation.

Raw AI response:
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/api/get_analysis_packages_with_metrics.php",
    "/axialy-production-ui/var/www/html/axialy-ui/api/feedback_requests/README.md",
    "/axialy-production-ui/var/www/html/axialy-ui/api/stakeholder_feedback/README.md"
  ],
  "purpose": "This README serves as the primary documentation for the API layer of the Axialy UI. It provides an overview of backend endpoints responsible for fetching and aggregating data, specifically for analysis packages, feedback request summaries, and raw stakeholder feedback metrics. The file acts as a manifest for the directory's functionality and guides developers to sub-directories for more granular API documentation."
}

-------------------------------------------------
File #32
Path: /axialy-production-ui/var/www/html/axialy-ui/assets/css/account-actions.css

Referenced files:
  (none)

Purpose:
This CSS file defines the visual styling for the account-related interaction components within the AxiaBA production UI. Specifically, it provides styling for global header icons (such as settings and help), including their hover states, tooltips, and associated dropdown menus. The file implements the project's brand guidelines (e.g., specific color palettes, transitions, and gradients) and includes responsive design adjustments for smaller screens, support for system-level dark mode, and high-contrast accessibility settings. It does not contain any direct file references (e.g., imports or assets), functioning as a standalone stylesheet.

Raw AI response:
{
  "referenced_files": [],
  "purpose": "This CSS file defines the visual styling for the account-related interaction components within the AxiaBA production UI. Specifically, it provides styling for global header icons (such as settings and help), including their hover states, tooltips, and associated dropdown menus. The file implements the project's brand guidelines (e.g., specific color palettes, transitions, and gradients) and includes responsive design adjustments for smaller screens, support for system-level dark mode, and high-contrast accessibility settings. It does not contain any direct file references (e.g., imports or assets), functioning as a standalone stylesheet."
}

-------------------------------------------------
File #33
Path: /axialy-production-ui/var/www/html/axialy-ui/assets/css/account-modal.css

Referenced files:
  (none)

Purpose:
This file is a CSS stylesheet responsible for the visual styling and layout of an 'Account Management' interface. It defines the appearance of an overlay modal, including a subscription management card, status badges (active, trialing, expired), call-to-action buttons (such as cancellation), and a nested confirmation modal for cancellation operations. It includes media queries to ensure responsiveness across mobile devices.

Raw AI response:
{
  "referenced_files": [],
  "purpose": "This file is a CSS stylesheet responsible for the visual styling and layout of an 'Account Management' interface. It defines the appearance of an overlay modal, including a subscription management card, status badges (active, trialing, expired), call-to-action buttons (such as cancellation), and a nested confirmation modal for cancellation operations. It includes media queries to ensure responsiveness across mobile devices."
}

-------------------------------------------------
File #34
Path: /axialy-production-ui/var/www/html/axialy-ui/assets/css/analysis-package-header.css

Referenced files:
  (none)

Purpose:
This CSS file provides the styling and layout definitions for a modal/overlay component titled 'Analysis Package Header'. It governs the visual appearance of the overlay container, its content form (including input fields, labels, and select boxes), call-to-action buttons, and a loading state indicator. It is designed with a mobile-first approach, incorporating responsive breakpoints, accessibility features (such as keyboard focus indicators and support for reduced motion preferences), and print-specific visibility settings to align with the Axialy system's branding guidelines.

Raw AI response:
{
  "referenced_files": [],
  "purpose": "This CSS file provides the styling and layout definitions for a modal/overlay component titled 'Analysis Package Header'. It governs the visual appearance of the overlay container, its content form (including input fields, labels, and select boxes), call-to-action buttons, and a loading state indicator. It is designed with a mobile-first approach, incorporating responsive breakpoints, accessibility features (such as keyboard focus indicators and support for reduced motion preferences), and print-specific visibility settings to align with the Axialy system's branding guidelines."
}

-------------------------------------------------
File #35
Path: /axialy-production-ui/var/www/html/axialy-ui/assets/css/content-review.css

Referenced files:
  (none)

Purpose:
This CSS file provides the styling for a 'content review' interface within the application. Its primary functions are to define the visual presentation of a modal overlay (including a dimmed background), a centered form for submitting reviews, selectable record tiles, and a 'processing' spinner/mask overlay used to provide user feedback during asynchronous operations.

Raw AI response:
```json
{
  "referenced_files": [],
  "purpose": "This CSS file provides the styling for a 'content review' interface within the application. Its primary functions are to define the visual presentation of a modal overlay (including a dimmed background), a centered form for submitting reviews, selectable record tiles, and a 'processing' spinner/mask overlay used to provide user feedback during asynchronous operations."
}
```

-------------------------------------------------
File #36
Path: /axialy-production-ui/var/www/html/axialy-ui/assets/css/content-revision.css

Referenced files:
  (none)

Purpose:
This CSS file defines the visual styling and layout for a 'content revision' UI component. It specifically provides styles for a modal overlay, a scrollable form container, form input elements, individual record fieldsets (including specific error/deletion styling), a sticky button footer, and a page-mask loading spinner. It ensures the interface is responsive and provides clear visual feedback for administrative content editing workflows.

Raw AI response:
```json
{
  "referenced_files": [],
  "purpose": "This CSS file defines the visual styling and layout for a 'content revision' UI component. It specifically provides styles for a modal overlay, a scrollable form container, form input elements, individual record fieldsets (including specific error/deletion styling), a sticky button footer, and a page-mask loading spinner. It ensures the interface is responsive and provides clear visual feedback for administrative content editing workflows."
}
```

-------------------------------------------------
File #37
Path: /axialy-production-ui/var/www/html/axialy-ui/assets/css/dashboard-tab.css

Referenced files:
  (none)

Purpose:
This file is a CSS stylesheet responsible for defining the visual presentation and layout of the 'dashboard-tab' component within the user interface. It provides styling for key UI elements including the main dashboard container, a filter form (#feedback-filters-form), a data table for feedback requests (#feedback-requests-table), pagination controls, toast notifications, and responsive design adjustments for mobile devices. It relies on standard CSS and integrates with existing Bootstrap classes (e.g., .form-select, .btn-primary) to maintain consistent styling across the application.

Raw AI response:
```json
{
  "referenced_files": [],
  "purpose": "This file is a CSS stylesheet responsible for defining the visual presentation and layout of the 'dashboard-tab' component within the user interface. It provides styling for key UI elements including the main dashboard container, a filter form (#feedback-filters-form), a data table for feedback requests (#feedback-requests-table), pagination controls, toast notifications, and responsive design adjustments for mobile devices. It relies on standard CSS and integrates with existing Bootstrap classes (e.g., .form-select, .btn-primary) to maintain consistent styling across the application."
}
```

-------------------------------------------------
File #38
Path: /axialy-production-ui/var/www/html/axialy-ui/assets/css/desktop.css

Referenced files:
  - /assets/img/AxiaBA-Umbrella.png

Purpose:
This file serves as the core stylesheet for the desktop and mobile responsive layout of the AxiaBA application. It defines the global visual identity through CSS variables (branding colors, spacing, and sizing), establishes the main application structure (page container, header, overview panel, control panel, and footer), and implements responsive design adjustments to ensure functionality across various screen sizes. It also includes styling for interactive components like ribbons, dropdowns, buttons, and form inputs.

Raw AI response:
```json
{
  "referenced_files": [
    "/assets/img/AxiaBA-Umbrella.png"
  ],
  "purpose": "This file serves as the core stylesheet for the desktop and mobile responsive layout of the AxiaBA application. It defines the global visual identity through CSS variables (branding colors, spacing, and sizing), establishes the main application structure (page container, header, overview panel, control panel, and footer), and implements responsive design adjustments to ensure functionality across various screen sizes. It also includes styling for interactive components like ribbons, dropdowns, buttons, and form inputs."
}
```

-------------------------------------------------
File #39
Path: /axialy-production-ui/var/www/html/axialy-ui/assets/css/feedback-confirmation.css

Referenced files:
  (none)

Purpose:
This file is a CSS stylesheet designed to provide styling for a feedback confirmation page and associated UI modal components. It defines layout rules for containers, success/error messaging, and specific visual treatments for overlays (modals), tables, and action buttons. Notably, it contains specific styles for a '#pending-requests-overlay', implying that this CSS supports an interface where users can view and interact with pending requests via a pop-up modal within the application.

Raw AI response:
{
  "referenced_files": [],
  "purpose": "This file is a CSS stylesheet designed to provide styling for a feedback confirmation page and associated UI modal components. It defines layout rules for containers, success/error messaging, and specific visual treatments for overlays (modals), tables, and action buttons. Notably, it contains specific styles for a '#pending-requests-overlay', implying that this CSS supports an interface where users can view and interact with pending requests via a pop-up modal within the application."
}

-------------------------------------------------
File #40
Path: /axialy-production-ui/var/www/html/axialy-ui/assets/css/feedback-form-request.css

Referenced files:
  (none)

Purpose:
This CSS file provides the visual styling for a feedback submission form. It defines the layout for a container, specific input fields (such as a textarea for user messages), submission buttons, and success/feedback message notifications. It ensures the form is consistently formatted, responsive, and aesthetically aligned with the application's UI design.

Raw AI response:
```json
{
  "referenced_files": [],
  "purpose": "This CSS file provides the visual styling for a feedback submission form. It defines the layout for a container, specific input fields (such as a textarea for user messages), submission buttons, and success/feedback message notifications. It ensures the form is consistently formatted, responsive, and aesthetically aligned with the application's UI design."
}
```

-------------------------------------------------
File #41
Path: /axialy-production-ui/var/www/html/axialy-ui/assets/css/focus-areas.css

Referenced files:
  (none)

Purpose:
This file provides the Cascading Style Sheet (CSS) definitions for the 'Focus Areas' interface component within the Axialy production UI. It defines the visual layout, interactive states (hover, active, disabled), and animations for various UI elements, including collapsible ribbons, search inputs, data summary cards, metric displays, and template selection hierarchies. By using utility classes (like .hidden) and specific IDs (like #focus-area-container), it supports the dynamic manipulation of the DOM for this feature.

Raw AI response:
```json
{
  "referenced_files": [],
  "purpose": "This file provides the Cascading Style Sheet (CSS) definitions for the 'Focus Areas' interface component within the Axialy production UI. It defines the visual layout, interactive states (hover, active, disabled), and animations for various UI elements, including collapsible ribbons, search inputs, data summary cards, metric displays, and template selection hierarchies. By using utility classes (like .hidden) and specific IDs (like #focus-area-container), it supports the dynamic manipulation of the DOM for this feature."
}
```

-------------------------------------------------
File #42
Path: /axialy-production-ui/var/www/html/axialy-ui/assets/css/generate-tab.css

Referenced files:
  (none)

Purpose:
This CSS file provides the visual styling, layout, and component design for the 'Generate' tab interface within the AxiaBA platform. It defines the appearance of interactive UI elements including collapsible ribbons, input/feedback containers, editable fields, loading spinners, character counters, and action buttons. It also contains extensive styling for modal overlays used to manage data saving (e.g., 'New Package' vs 'Existing Package' flows) and handles responsive design adjustments to ensure usability across different screen sizes. No external file dependencies (like @import rules) are present in this file.

Raw AI response:
{
  "referenced_files": [],
  "purpose": "This CSS file provides the visual styling, layout, and component design for the 'Generate' tab interface within the AxiaBA platform. It defines the appearance of interactive UI elements including collapsible ribbons, input/feedback containers, editable fields, loading spinners, character counters, and action buttons. It also contains extensive styling for modal overlays used to manage data saving (e.g., 'New Package' vs 'Existing Package' flows) and handles responsive design adjustments to ensure usability across different screen sizes. No external file dependencies (like @import rules) are present in this file."
}

-------------------------------------------------
File #43
Path: /axialy-production-ui/var/www/html/axialy-ui/assets/css/home-tab.css

Referenced files:
  (none)

Purpose:
This file contains the CSS styles for the home tab interface of the Axialy application. Its primary purpose is to define the visual presentation and layout of the main user interaction area, including a welcome section, user input field (textarea), step indicators, CTA (call-to-action) buttons with animation effects, and a secondary form display area for stakeholder management. It includes responsive design rules to ensure the interface functions correctly across mobile and desktop device resolutions.

Raw AI response:
```json
{
  "referenced_files": [],
  "purpose": "This file contains the CSS styles for the home tab interface of the Axialy application. Its primary purpose is to define the visual presentation and layout of the main user interaction area, including a welcome section, user input field (textarea), step indicators, CTA (call-to-action) buttons with animation effects, and a secondary form display area for stakeholder management. It includes responsive design rules to ensure the interface functions correctly across mobile and desktop device resolutions."
}
```

-------------------------------------------------
File #44
Path: /axialy-production-ui/var/www/html/axialy-ui/assets/css/new-focus-area-overlay.css

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/assets/css/overlay.css

Purpose:
This CSS file defines the visual styling for the 'manual focus area creation' overlay within the Axialy production UI. It implements a modern, branded look using the AxiaBA color palette (specifically purple, success green, and slate grey) and layout patterns. It relies on base styles from a parent 'overlay.css' (referenced in the file comments) while overriding them to provide specific interface components such as responsive form containers, record fieldsets, and custom scrollbars for data-heavy sections.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/assets/css/overlay.css"
  ],
  "purpose": "This CSS file defines the visual styling for the 'manual focus area creation' overlay within the Axialy production UI. It implements a modern, branded look using the AxiaBA color palette (specifically purple, success green, and slate grey) and layout patterns. It relies on base styles from a parent 'overlay.css' (referenced in the file comments) while overriding them to provide specific interface components such as responsive form containers, record fieldsets, and custom scrollbars for data-heavy sections."
}
```

-------------------------------------------------
File #45
Path: /axialy-production-ui/var/www/html/axialy-ui/assets/css/overlay.css

Referenced files:
  (none)

Purpose:
This file serves as the global CSS stylesheet for modal/popup overlays within the AxiaBA UI. It defines the structural and visual styling for overlay containers, form fields, buttons, and loading spinners. Furthermore, it contains specialized styles for specific features like 'Revisions Summary' and 'Collate Feedback' interfaces, and includes comprehensive responsive design logic to ensure these overlays function correctly across mobile and desktop devices.

Raw AI response:
{
  "referenced_files": [],
  "purpose": "This file serves as the global CSS stylesheet for modal/popup overlays within the AxiaBA UI. It defines the structural and visual styling for overlay containers, form fields, buttons, and loading spinners. Furthermore, it contains specialized styles for specific features like 'Revisions Summary' and 'Collate Feedback' interfaces, and includes comprehensive responsive design logic to ensure these overlays function correctly across mobile and desktop devices."
}

-------------------------------------------------
File #46
Path: /axialy-production-ui/var/www/html/axialy-ui/assets/css/promo-modal.css

Referenced files:
  (none)

Purpose:
This file provides the CSS styling for a dynamic promotional modal component. It defines the layout, responsiveness, typography, and visual effects (such as gradients, shadows, and animations) required to display promotional content fetched from a database. It ensures that the modal remains centered, accessible, and free of horizontal scrollbars across various device sizes, while also managing global body overflow states when the modal is active.

Raw AI response:
```json
{
  "referenced_files": [],
  "purpose": "This file provides the CSS styling for a dynamic promotional modal component. It defines the layout, responsiveness, typography, and visual effects (such as gradients, shadows, and animations) required to display promotional content fetched from a database. It ensures that the modal remains centered, accessible, and free of horizontal scrollbars across various device sizes, while also managing global body overflow states when the modal is active."
}
```

-------------------------------------------------
File #47
Path: /axialy-production-ui/var/www/html/axialy-ui/assets/css/publish-tab.css

Referenced files:
  (none)

Purpose:
This file is a comprehensive stylesheet for the 'Publish' tab within the Axialy UI production environment. Its functional purpose is to provide styling for a complex multi-step workflow that includes: 

1. Organizational and package selection interfaces.
2. Artifact generation and configuration (including HTML input forms with enhanced preview and CSS isolation features).
3. Stakeholder invitation management (handling email tags, lists, and ad-hoc additions).
4. Display of published artifacts, including grid-based layouts, expiry management badges, and status indicators.
5. Loading overlays, toast containers, and modal component styling.

The file is designed to support a responsive web interface, utilizing custom grid layouts, animations, and specific media queries to maintain usability across mobile and desktop devices.

Raw AI response:
```json
{
  "referenced_files": [],
  "purpose": "This file is a comprehensive stylesheet for the 'Publish' tab within the Axialy UI production environment. Its functional purpose is to provide styling for a complex multi-step workflow that includes: \n\n1. Organizational and package selection interfaces.\n2. Artifact generation and configuration (including HTML input forms with enhanced preview and CSS isolation features).\n3. Stakeholder invitation management (handling email tags, lists, and ad-hoc additions).\n4. Display of published artifacts, including grid-based layouts, expiry management badges, and status indicators.\n5. Loading overlays, toast containers, and modal component styling.\n\nThe file is designed to support a responsive web interface, utilizing custom grid layouts, animations, and specific media queries to maintain usability across mobile and desktop devices."
}
```

-------------------------------------------------
File #48
Path: /axialy-production-ui/var/www/html/axialy-ui/assets/css/README.md

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/assets/css/account-actions.css
  - /axialy-production-ui/var/www/html/axialy-ui/assets/css/content-review.css
  - /axialy-production-ui/var/www/html/axialy-ui/assets/css/content-revision.css
  - /axialy-production-ui/var/www/html/axialy-ui/assets/css/dashboard-tab.css
  - /axialy-production-ui/var/www/html/axialy-ui/assets/css/desktop.css
  - /axialy-production-ui/var/www/html/axialy-ui/assets/css/feedback-confirmation.css
  - /axialy-production-ui/var/www/html/axialy-ui/assets/css/feedback-form-request.css
  - /axialy-production-ui/var/www/html/axialy-ui/assets/css/focus-areas.css
  - /axialy-production-ui/var/www/html/axialy-ui/assets/css/generate-tab.css
  - /axialy-production-ui/var/www/html/axialy-ui/assets/css/home-tab.css
  - /axialy-production-ui/var/www/html/axialy-ui/assets/css/new-focus-area-overlay.css
  - /axialy-production-ui/var/www/html/axialy-ui/assets/css/overlay.css
  - /axialy-production-ui/var/www/html/axialy-ui/assets/css/publish-tab.css
  - /axialy-production-ui/var/www/html/axialy-ui/assets/css/refine-tab-overlays.css
  - /axialy-production-ui/var/www/html/axialy-ui/assets/css/refine-tab.css
  - /axialy-production-ui/var/www/html/axialy-ui/assets/css/settings-tab.css
  - /axialy-production-ui/var/www/html/axialy-ui/assets/css/stakeholder-content-review.css
  - /axialy-production-ui/var/www/html/axialy-ui/assets/css/support-tickets.css

Purpose:
This file serves as a documentation registry for the project's CSS architecture. It provides an index of the stylesheets located in the '/assets/css/' directory, explaining the functional scope of each file (e.g., individual application tabs, global layout, and specific modal overlays).

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/assets/css/account-actions.css",
    "/axialy-production-ui/var/www/html/axialy-ui/assets/css/content-review.css",
    "/axialy-production-ui/var/www/html/axialy-ui/assets/css/content-revision.css",
    "/axialy-production-ui/var/www/html/axialy-ui/assets/css/dashboard-tab.css",
    "/axialy-production-ui/var/www/html/axialy-ui/assets/css/desktop.css",
    "/axialy-production-ui/var/www/html/axialy-ui/assets/css/feedback-confirmation.css",
    "/axialy-production-ui/var/www/html/axialy-ui/assets/css/feedback-form-request.css",
    "/axialy-production-ui/var/www/html/axialy-ui/assets/css/focus-areas.css",
    "/axialy-production-ui/var/www/html/axialy-ui/assets/css/generate-tab.css",
    "/axialy-production-ui/var/www/html/axialy-ui/assets/css/home-tab.css",
    "/axialy-production-ui/var/www/html/axialy-ui/assets/css/new-focus-area-overlay.css",
    "/axialy-production-ui/var/www/html/axialy-ui/assets/css/overlay.css",
    "/axialy-production-ui/var/www/html/axialy-ui/assets/css/publish-tab.css",
    "/axialy-production-ui/var/www/html/axialy-ui/assets/css/refine-tab-overlays.css",
    "/axialy-production-ui/var/www/html/axialy-ui/assets/css/refine-tab.css",
    "/axialy-production-ui/var/www/html/axialy-ui/assets/css/settings-tab.css",
    "/axialy-production-ui/var/www/html/axialy-ui/assets/css/stakeholder-content-review.css",
    "/axialy-production-ui/var/www/html/axialy-ui/assets/css/support-tickets.css"
  ],
  "purpose": "This file serves as a documentation registry for the project's CSS architecture. It provides an index of the stylesheets located in the '/assets/css/' directory, explaining the functional scope of each file (e.g., individual application tabs, global layout, and specific modal overlays)."
}
```

-------------------------------------------------
File #49
Path: /axialy-production-ui/var/www/html/axialy-ui/assets/css/refine-tab-overlays.css

Referenced files:
  (none)

Purpose:
This file is a CSS stylesheet designed to handle the visual styling and layout of various modal overlays within the 'Refine' tab of the Axialy UI. It provides comprehensive styles for record editing, assessment modals, package advisors, and input text entry overlays. The stylesheet incorporates responsive design, accessibility features (such as keyboard navigation focus states and high-contrast support), custom scrollbar styling, and z-index management to ensure modal content remains usable and properly layered within the application interface.

Raw AI response:
{
  "referenced_files": [],
  "purpose": "This file is a CSS stylesheet designed to handle the visual styling and layout of various modal overlays within the 'Refine' tab of the Axialy UI. It provides comprehensive styles for record editing, assessment modals, package advisors, and input text entry overlays. The stylesheet incorporates responsive design, accessibility features (such as keyboard navigation focus states and high-contrast support), custom scrollbar styling, and z-index management to ensure modal content remains usable and properly layered within the application interface."
}

-------------------------------------------------
File #50
Path: /axialy-production-ui/var/www/html/axialy-ui/assets/css/refine-tab.css

Referenced files:
  (none)

Purpose:
This CSS file defines the visual styling for the 'Refine' tab interface within the Axialy production UI. It provides layout, component, and animation styles for the main content area, including the 'Axialy Advisor' call-to-action button, package summary lists with logo thumbnails, AI enhancement sections, action dropdowns, and various modal overlays for feedback and record management. It also explicitly manages z-index stacking contexts to ensure dropdowns and overlays render correctly over other page elements.

Raw AI response:
{
  "referenced_files": [],
  "purpose": "This CSS file defines the visual styling for the 'Refine' tab interface within the Axialy production UI. It provides layout, component, and animation styles for the main content area, including the 'Axialy Advisor' call-to-action button, package summary lists with logo thumbnails, AI enhancement sections, action dropdowns, and various modal overlays for feedback and record management. It also explicitly manages z-index stacking contexts to ensure dropdowns and overlays render correctly over other page elements."
}

-------------------------------------------------
File #51
Path: /axialy-production-ui/var/www/html/axialy-ui/assets/css/settings-tab.css

Referenced files:
  (none)

Purpose:
This CSS file defines the presentation layer for the 'Settings' interface within the AxiaBA/Axialy UI. It provides comprehensive styling for organization management components, including form controls (inputs, textareas, select boxes), interaction states (loading spinners, hover effects, validation indicators), and grid-based display cards for existing organizations. The styling emphasizes a brand-aligned aesthetic using gradients, specific border-radius configurations, and consistent color palettes, while also addressing accessibility through focus-visible states and responsive design breakpoints.

Raw AI response:
{
  "referenced_files": [],
  "purpose": "This CSS file defines the presentation layer for the 'Settings' interface within the AxiaBA/Axialy UI. It provides comprehensive styling for organization management components, including form controls (inputs, textareas, select boxes), interaction states (loading spinners, hover effects, validation indicators), and grid-based display cards for existing organizations. The styling emphasizes a brand-aligned aesthetic using gradients, specific border-radius configurations, and consistent color palettes, while also addressing accessibility through focus-visible states and responsive design breakpoints."
}

-------------------------------------------------
File #52
Path: /axialy-production-ui/var/www/html/axialy-ui/assets/css/stakeholder-content-review.css

Referenced files:
  (none)

Purpose:
This CSS file serves as the primary stylesheet for the stakeholder content review interface. It contains two distinct sets of styles: first, it defines the layout, typography, and interactive elements (buttons, overlays, feedback text areas) for a data review screen; second, it provides a specialized, brand-aligned visual theme (using a purple gradient and a centered card layout) for a separate 'PIN entry' authentication page. The file includes structural styles, responsive media queries, and animation definitions to support these two distinct functional views within the AxiaBA application.

Raw AI response:
{
  "referenced_files": [],
  "purpose": "This CSS file serves as the primary stylesheet for the stakeholder content review interface. It contains two distinct sets of styles: first, it defines the layout, typography, and interactive elements (buttons, overlays, feedback text areas) for a data review screen; second, it provides a specialized, brand-aligned visual theme (using a purple gradient and a centered card layout) for a separate 'PIN entry' authentication page. The file includes structural styles, responsive media queries, and animation definitions to support these two distinct functional views within the AxiaBA application."
}

-------------------------------------------------
File #53
Path: /axialy-production-ui/var/www/html/axialy-ui/assets/css/support-tickets.css

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/assets/css/overlay.css

Purpose:
This CSS file defines the visual styling for the 'Support Tickets' overlay feature within the AxiaBA platform. It ensures that the ticket interface maintains design consistency with the rest of the application by providing specific styles for the modal container, header, controls (checkboxes and buttons), data tables, and form elements. The file explicitly references 'overlay.css' in its comments, indicating it is intended to be used as a supplementary stylesheet that overrides or extends the base overlay functionality to suit the support module's layout requirements.

Raw AI response:
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/assets/css/overlay.css"
  ],
  "purpose": "This CSS file defines the visual styling for the 'Support Tickets' overlay feature within the AxiaBA platform. It ensures that the ticket interface maintains design consistency with the rest of the application by providing specific styles for the modal container, header, controls (checkboxes and buttons), data tables, and form elements. The file explicitly references 'overlay.css' in its comments, indicating it is intended to be used as a supplementary stylesheet that overrides or extends the base overlay functionality to suit the support module's layout requirements."
}

-------------------------------------------------
File #54
Path: /axialy-production-ui/var/www/html/axialy-ui/assets/css/survey-modals.css

Referenced files:
  (none)

Purpose:
This CSS file provides the styling and layout definitions for survey-related UI components, specifically focusing on action buttons within tables (e.g., 'View', 'Send Reminder', 'Cancel') and responsive modal/overlay infrastructure. It includes specific overrides and adjustments to ensure modals and collate-feedback overlays handle vertical scrolling correctly on both desktop and mobile devices.

Raw AI response:
```json
{
  "referenced_files": [],
  "purpose": "This CSS file provides the styling and layout definitions for survey-related UI components, specifically focusing on action buttons within tables (e.g., 'View', 'Send Reminder', 'Cancel') and responsive modal/overlay infrastructure. It includes specific overrides and adjustments to ensure modals and collate-feedback overlays handle vertical scrolling correctly on both desktop and mobile devices."
}
```

-------------------------------------------------
File #55
Path: /axialy-production-ui/var/www/html/axialy-ui/assets/css/survey-tab.css

Referenced files:
  (none)

Purpose:
This file is a CSS stylesheet responsible for the visual styling and layout of a survey management or feedback interface within the 'axialy-ui' system. It defines design patterns for data display, including: 

1. A primary container and content wrapper for survey-related modules.
2. Styling for filter forms (#survey-filters-form) to allow users to refine data searches.
3. Formatting for a responsive feedback request data table (#survey-feedback-requests-table), featuring hover effects, zebra-striping, and conditional hiding of columns on mobile devices.
4. UI components for interaction, such as pagination controls, custom status badges, 'compile feedback' buttons, and tooltip styles for responses.
5. Status-specific indicators (e.g., unresolved feedback highlights and feedback type color-coding) and notification toast designs.

It contains no external references to other files, serving as an encapsulated stylistic layer for the survey functionality.

Raw AI response:
```json
{
  "referenced_files": [],
  "purpose": "This file is a CSS stylesheet responsible for the visual styling and layout of a survey management or feedback interface within the 'axialy-ui' system. It defines design patterns for data display, including: \n\n1. A primary container and content wrapper for survey-related modules.\n2. Styling for filter forms (#survey-filters-form) to allow users to refine data searches.\n3. Formatting for a responsive feedback request data table (#survey-feedback-requests-table), featuring hover effects, zebra-striping, and conditional hiding of columns on mobile devices.\n4. UI components for interaction, such as pagination controls, custom status badges, 'compile feedback' buttons, and tooltip styles for responses.\n5. Status-specific indicators (e.g., unresolved feedback highlights and feedback type color-coding) and notification toast designs.\n\nIt contains no external references to other files, serving as an encapsulated stylistic layer for the survey functionality."
}
```

-------------------------------------------------
File #56
Path: /axialy-production-ui/var/www/html/axialy-ui/assets/img/temp/axialy_cta.png

Referenced files:
  (none)

Purpose:
This file is a PNG image asset used within the 'axialy-ui' system. Based on its file path ('/assets/img/temp/axialy_cta.png'), it serves as a temporary or placeholder call-to-action (CTA) button or graphic within the application's user interface.

Raw AI response:
```json
{
  "referenced_files": [],
  "purpose": "This file is a PNG image asset used within the 'axialy-ui' system. Based on its file path ('/assets/img/temp/axialy_cta.png'), it serves as a temporary or placeholder call-to-action (CTA) button or graphic within the application's user interface."
}
```

-------------------------------------------------
File #57
Path: /axialy-production-ui/var/www/html/axialy-ui/assets/img/temp/Axiamax_Phoenix_fav_1024square.png

Referenced files:
  (none)

Purpose:
This file is an image asset (PNG format) used as a favicon or brand icon for the 'Axiamax Phoenix' branding within the Axialy system. It serves as a visual identifier for the application interface.

Raw AI response:
```json
{
  "referenced_files": [],
  "purpose": "This file is an image asset (PNG format) used as a favicon or brand icon for the 'Axiamax Phoenix' branding within the Axialy system. It serves as a visual identifier for the application interface."
}
```

-------------------------------------------------
File #58
Path: /axialy-production-ui/var/www/html/axialy-ui/assets/img/axialy_cta.png

Referenced files:
  (none)

Purpose:
This file is a Portable Network Graphics (PNG) image file containing the 'axialy_cta' graphic, which serves as a Call-to-Action (CTA) element within the Axialy user interface.

Raw AI response:
{
  "referenced_files": [],
  "purpose": "This file is a Portable Network Graphics (PNG) image file containing the 'axialy_cta' graphic, which serves as a Call-to-Action (CTA) element within the Axialy user interface."
}

-------------------------------------------------
File #59
Path: /axialy-production-ui/var/www/html/axialy-ui/assets/img/axialy_cta_1.png

Referenced files:
  (none)

Purpose:
This file is a PNG image asset named 'axialy_cta_1.png', serving as a visual element (likely a Call-to-Action button or graphic) within the Axialy production UI project.

Raw AI response:
```json
{
  "referenced_files": [],
  "purpose": "This file is a PNG image asset named 'axialy_cta_1.png', serving as a visual element (likely a Call-to-Action button or graphic) within the Axialy production UI project."
}
```

-------------------------------------------------
File #60
Path: /axialy-production-ui/var/www/html/axialy-ui/assets/img/company_logo1.png

Referenced files:
  (none)

Purpose:
This file is a PNG image file containing the company logo used for branding within the Axialy production UI. It serves as a visual asset for the web interface.

Raw AI response:
```json
{
  "referenced_files": [],
  "purpose": "This file is a PNG image file containing the company logo used for branding within the Axialy production UI. It serves as a visual asset for the web interface."
}
```

-------------------------------------------------
File #61
Path: /axialy-production-ui/var/www/html/axialy-ui/assets/img/company_logo2.png

Referenced files:
  (none)

Purpose:
This file is a PNG image file containing the company logo used for the branding and visual identity of the 'axialy-ui' application, located within the project's assets directory.

Raw AI response:
```json
{
  "referenced_files": [],
  "purpose": "This file is a PNG image file containing the company logo used for the branding and visual identity of the 'axialy-ui' application, located within the project's assets directory."
}
```

-------------------------------------------------
File #62
Path: /axialy-production-ui/var/www/html/axialy-ui/assets/img/favicon.ico

Referenced files:
  (none)

Purpose:
This file is a favicon.ico, which serves as the site icon (browser tab icon) for the Axialy production user interface. Being a binary image file, it contains no code references.

Raw AI response:
{
  "referenced_files": [],
  "purpose": "This file is a favicon.ico, which serves as the site icon (browser tab icon) for the Axialy production user interface. Being a binary image file, it contains no code references."
}

-------------------------------------------------
File #63
Path: /axialy-production-ui/var/www/html/axialy-ui/assets/img/product_logo.png

Referenced files:
  (none)

Purpose:
This file is a product logo image (PNG format). Within the system, it serves as a visual asset, likely used for branding purposes in the user interface, such as headers, footers, or product identity sections within the `/axialy-production-ui/` web application.

Raw AI response:
```json
{
  "referenced_files": [],
  "purpose": "This file is a product logo image (PNG format). Within the system, it serves as a visual asset, likely used for branding purposes in the user interface, such as headers, footers, or product identity sections within the `/axialy-production-ui/` web application."
}
```

-------------------------------------------------
File #64
Path: /axialy-production-ui/var/www/html/axialy-ui/assets/img/product_logo1.png

Referenced files:
  (none)

Purpose:
This file is a PNG image file containing the logo for a product (labeled 'product_logo1'). In the context of the /axialy-production-ui/ project, it serves as a static asset used by the front-end user interface to represent a specific product visually.

Raw AI response:
{
  "referenced_files": [],
  "purpose": "This file is a PNG image file containing the logo for a product (labeled 'product_logo1'). In the context of the /axialy-production-ui/ project, it serves as a static asset used by the front-end user interface to represent a specific product visually."
}

-------------------------------------------------
File #65
Path: /axialy-production-ui/var/www/html/axialy-ui/assets/img/product_logo2.png

Referenced files:
  (none)

Purpose:
This file is a PNG image file (product_logo2.png) intended for use as a visual asset (logo) within the Axialy production UI system.

Raw AI response:
{
  "referenced_files": [],
  "purpose": "This file is a PNG image file (product_logo2.png) intended for use as a visual asset (logo) within the Axialy production UI system."
}

-------------------------------------------------
File #66
Path: /axialy-production-ui/var/www/html/axialy-ui/assets/img/product_logo3.png

Referenced files:
  (none)

Purpose:
This file is a PNG image asset (`product_logo3.png`) used for branding or identification within the Axialy UI system. As an image file, it serves no executable function but is intended for display in the product's user interface.

Raw AI response:
{
  "referenced_files": [],
  "purpose": "This file is a PNG image asset (`product_logo3.png`) used for branding or identification within the Axialy UI system. As an image file, it serves no executable function but is intended for display in the product's user interface."
}

-------------------------------------------------
File #67
Path: /axialy-production-ui/var/www/html/axialy-ui/assets/img/product_logo_orig.png

Referenced files:
  (none)

Purpose:
This file is an image asset, specifically a product logo (product_logo_orig.png), intended for use within the UI of the Axialy system. It serves as a visual element, likely displayed in the product-related views or headers of the application as defined by the directory structure (/axialy-ui/assets/img/).

Raw AI response:
{
  "referenced_files": [],
  "purpose": "This file is an image asset, specifically a product logo (product_logo_orig.png), intended for use within the UI of the Axialy system. It serves as a visual element, likely displayed in the product-related views or headers of the application as defined by the directory structure (/axialy-ui/assets/img/)."
}

-------------------------------------------------
File #68
Path: /axialy-production-ui/var/www/html/axialy-ui/assets/img/rainbow-logo.png

Referenced files:
  (none)

Purpose:
This file is a PNG image file containing the 'rainbow-logo' asset for the Axialy production UI. It serves as a visual element, likely used as the primary branding or application logo within the web interface.

Raw AI response:
```json
{
  "referenced_files": [],
  "purpose": "This file is a PNG image file containing the 'rainbow-logo' asset for the Axialy production UI. It serves as a visual element, likely used as the primary branding or application logo within the web interface."
}
```

-------------------------------------------------
File #69
Path: /axialy-production-ui/var/www/html/axialy-ui/assets/img/README.md

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/assets/img/favicon.ico

Purpose:
This file serves as documentation for the directory containing static image assets for the UI. It explicitly identifies 'favicon.ico' as a managed asset within this folder, providing context for developers on the location and role of specific branding imagery used in the application.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/assets/img/favicon.ico"
  ],
  "purpose": "This file serves as documentation for the directory containing static image assets for the UI. It explicitly identifies 'favicon.ico' as a managed asset within this folder, providing context for developers on the location and role of specific branding imagery used in the application."
}
```

-------------------------------------------------
File #70
Path: /axialy-production-ui/var/www/html/axialy-ui/assets/README.md

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/assets/css/
  - /axialy-production-ui/var/www/html/axialy-ui/assets/img/

Purpose:
This file serves as documentation for the directory structure of the static assets folder in the axialy-ui project. It defines the organization of stylesheet files within the 'css/' directory and image-based assets within the 'img/' directory, ensuring developers understand how to locate and categorize static resources.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/assets/css/",
    "/axialy-production-ui/var/www/html/axialy-ui/assets/img/"
  ],
  "purpose": "This file serves as documentation for the directory structure of the static assets folder in the axialy-ui project. It defines the organization of stylesheet files within the 'css/' directory and image-based assets within the 'img/' directory, ensuring developers understand how to locate and categorize static resources."
}
```

-------------------------------------------------
File #71
Path: /axialy-production-ui/var/www/html/axialy-ui/config/account-actions.json

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/upgrade-account.php
  - /axialy-production-ui/var/www/html/axialy-ui/logout.php
  - /axialy-production-ui/var/www/html/axialy-ui/end_demo.php

Purpose:
This configuration file serves as a registry for account-related UI actions in the application. It defines the labels, triggering mechanisms (either 'link' to a PHP script or 'js' function calls), and the activation state for menu items such as account management, session termination, and feedback submission. Note that while the JSON file lists PHP files as targets for 'link' actions, the actual existence of these files at the root directory level is assumed based on the paths provided in the 'action' field.

Raw AI response:
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/upgrade-account.php",
    "/axialy-production-ui/var/www/html/axialy-ui/logout.php",
    "/axialy-production-ui/var/www/html/axialy-ui/end_demo.php"
  ],
  "purpose": "This configuration file serves as a registry for account-related UI actions in the application. It defines the labels, triggering mechanisms (either 'link' to a PHP script or 'js' function calls), and the activation state for menu items such as account management, session termination, and feedback submission. Note that while the JSON file lists PHP files as targets for 'link' actions, the actual existence of these files at the root directory level is assumed based on the paths provided in the 'action' field."
}

-------------------------------------------------
File #72
Path: /axialy-production-ui/var/www/html/axialy-ui/config/control-panel-menu.json

Referenced files:
  - assets/img/axialy_dev_background.png
  - assets/img/AxiaBA-Umbrella.png

Purpose:
This file acts as a configuration manifest for the Axialy production UI control panel. It defines the structure, navigation targets, and UI-specific visual properties (such as background images and opacity levels) for the primary application menu and the associated views dropdown. By centralizing these UI settings in a JSON format, the application can dynamically render the navigation interface based on environment-specific (DEV vs. production) image paths.

Raw AI response:
```json
{
  "referenced_files": [
    "assets/img/axialy_dev_background.png",
    "assets/img/AxiaBA-Umbrella.png"
  ],
  "purpose": "This file acts as a configuration manifest for the Axialy production UI control panel. It defines the structure, navigation targets, and UI-specific visual properties (such as background images and opacity levels) for the primary application menu and the associated views dropdown. By centralizing these UI settings in a JSON format, the application can dynamically render the navigation interface based on environment-specific (DEV vs. production) image paths."
}
```

-------------------------------------------------
File #73
Path: /axialy-production-ui/var/www/html/axialy-ui/config/feedback-response-types.json

Referenced files:
  (none)

Purpose:
This configuration file acts as a centralized schema for defining the available input patterns and interaction models for user feedback on form items within the system. It maps semantic labels (like 'Yes/No' or 'Revise or Approve') to specific primary and secondary response actions, allowing the UI to dynamically generate feedback controls based on these predefined types.

Raw AI response:
```json
{
  "referenced_files": [],
  "purpose": "This configuration file acts as a centralized schema for defining the available input patterns and interaction models for user feedback on form items within the system. It maps semantic labels (like 'Yes/No' or 'Revise or Approve') to specific primary and secondary response actions, allowing the UI to dynamically generate feedback controls based on these predefined types."
}
```

-------------------------------------------------
File #74
Path: /axialy-production-ui/var/www/html/axialy-ui/config/package-actions.json

Referenced files:
  (none)

Purpose:
This file acts as a configuration manifest that defines the interactive menu actions available for analysis packages within the Axialy UI. It dictates the labels, trigger types (e.g., overlay, link, confirmation), and functional descriptions for operations such as creating focus areas, refreshing data, editing headers, or removing packages. It serves as a centralized source of truth for the frontend to render the 'Actions' menu for package management.

Raw AI response:
{
  "referenced_files": [],
  "purpose": "This file acts as a configuration manifest that defines the interactive menu actions available for analysis packages within the Axialy UI. It dictates the labels, trigger types (e.g., overlay, link, confirmation), and functional descriptions for operations such as creating focus areas, refreshing data, editing headers, or removing packages. It serves as a centralized source of truth for the frontend to render the 'Actions' menu for package management."
}

-------------------------------------------------
File #75
Path: /axialy-production-ui/var/www/html/axialy-ui/config/README.md

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/config/account-actions.json
  - /axialy-production-ui/var/www/html/axialy-ui/config/control-panel-menu.json
  - /axialy-production-ui/var/www/html/axialy-ui/config/feedback-response-types.json
  - /axialy-production-ui/var/www/html/axialy-ui/config/package-actions.json
  - /axialy-production-ui/var/www/html/axialy-ui/config/refine-activities.json
  - /axialy-production-ui/var/www/html/axialy-ui/config/support-actions.json

Purpose:
This file serves as technical documentation for the configuration directory of the Axialy UI. It provides an overview of the JSON-based schemas used to drive UI components—specifically navigation menus, user account actions, support workflows, and activity panels—ensuring that developers understand how to define and structure the system's dynamic interface elements.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/config/account-actions.json",
    "/axialy-production-ui/var/www/html/axialy-ui/config/control-panel-menu.json",
    "/axialy-production-ui/var/www/html/axialy-ui/config/feedback-response-types.json",
    "/axialy-production-ui/var/www/html/axialy-ui/config/package-actions.json",
    "/axialy-production-ui/var/www/html/axialy-ui/config/refine-activities.json",
    "/axialy-production-ui/var/www/html/axialy-ui/config/support-actions.json"
  ],
  "purpose": "This file serves as technical documentation for the configuration directory of the Axialy UI. It provides an overview of the JSON-based schemas used to drive UI components—specifically navigation menus, user account actions, support workflows, and activity panels—ensuring that developers understand how to define and structure the system's dynamic interface elements."
}
```

-------------------------------------------------
File #76
Path: /axialy-production-ui/var/www/html/axialy-ui/config/refine-activities.json

Referenced files:
  (none)

Purpose:
This file serves as a configuration manifest for the 'Refine Activities' menu or action panel within the Axialy UI. It defines a structured list of available user actions (such as AI-driven content enhancement, feedback collection, data management, and version recovery) that can be triggered within a 'focus area' context. Each entry specifies the UI interaction pattern (overlay vs. confirmation), the associated functional action trigger, a user-facing label, and an 'active' flag that determines whether the option is currently enabled for the interface.

Raw AI response:
```json
{
  "referenced_files": [],
  "purpose": "This file serves as a configuration manifest for the 'Refine Activities' menu or action panel within the Axialy UI. It defines a structured list of available user actions (such as AI-driven content enhancement, feedback collection, data management, and version recovery) that can be triggered within a 'focus area' context. Each entry specifies the UI interaction pattern (overlay vs. confirmation), the associated functional action trigger, a user-facing label, and an 'active' flag that determines whether the option is currently enabled for the interface."
}
```

-------------------------------------------------
File #77
Path: /axialy-production-ui/var/www/html/axialy-ui/config/support-actions.json

Referenced files:
  - /user-documentation.php

Purpose:
This file serves as a configuration manifest for the UI's support menu. It defines a list of support-related actions (links or JavaScript function calls) available to the user, allowing the frontend to dynamically render the support dropdown or menu based on the provided JSON structure. Note that the 'Contact Support' entry is currently a placeholder, indicating that this feature is incomplete or pending development.

Raw AI response:
```json
{
  "referenced_files": [
    "/user-documentation.php"
  ],
  "purpose": "This file serves as a configuration manifest for the UI's support menu. It defines a list of support-related actions (links or JavaScript function calls) available to the user, allowing the frontend to dynamically render the support dropdown or menu based on the provided JSON structure. Note that the 'Contact Support' entry is currently a placeholder, indicating that this feature is incomplete or pending development."
}
```

-------------------------------------------------
File #78
Path: /axialy-production-ui/var/www/html/axialy-ui/content/generate-tab.html

Referenced files:
  (none)

Purpose:
This file provides the HTML structure for the 'Generate' tab interface in the Axialy application. It serves as a user input and control dashboard, featuring a multi-line text area for analysis scenarios, a dynamic section for selecting AI focus areas, and controls for processing AI-generated data. The interface is designed to be populated dynamically, as indicated by empty containers like 'ribbons-container' and 'chooseFocusForm', and displays metadata such as character counts, input summaries, and versioning information.

Raw AI response:
{
  "referenced_files": [],
  "purpose": "This file provides the HTML structure for the 'Generate' tab interface in the Axialy application. It serves as a user input and control dashboard, featuring a multi-line text area for analysis scenarios, a dynamic section for selecting AI focus areas, and controls for processing AI-generated data. The interface is designed to be populated dynamically, as indicated by empty containers like 'ribbons-container' and 'chooseFocusForm', and displays metadata such as character counts, input summaries, and versioning information."
}

-------------------------------------------------
File #79
Path: /axialy-production-ui/var/www/html/axialy-ui/content/home-tab.html

Referenced files:
  - https://ui.axialy.ai/assets/img/axialy_cta.png

Purpose:
The file serves as the HTML template for the 'Home' tab of the Axialy application's user interface. Its primary function is to provide the user with a structured input interface for submitting thoughts, goals, or concerns for AI-driven analysis. It includes a step indicator, a character-limited text area, a submission trigger (CTA button), a loading state indicator, and placeholders for the subsequent display of analysis results and package creation workflows. The file is designed to be lightweight and performant by avoiding complex animations, relying on external CSS and JavaScript (implied but not explicitly referenced in this file) to handle the interaction logic and dynamic DOM manipulation.

Raw AI response:
```json
{
  "referenced_files": [
    "https://ui.axialy.ai/assets/img/axialy_cta.png"
  ],
  "purpose": "The file serves as the HTML template for the 'Home' tab of the Axialy application's user interface. Its primary function is to provide the user with a structured input interface for submitting thoughts, goals, or concerns for AI-driven analysis. It includes a step indicator, a character-limited text area, a submission trigger (CTA button), a loading state indicator, and placeholders for the subsequent display of analysis results and package creation workflows. The file is designed to be lightweight and performant by avoiding complex animations, relying on external CSS and JavaScript (implied but not explicitly referenced in this file) to handle the interaction logic and dynamic DOM manipulation."
}
```

-------------------------------------------------
File #80
Path: /axialy-production-ui/var/www/html/axialy-ui/content/publish-tab.html

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/content/assets/css/publish-tab.css

Purpose:
This file serves as the UI template for the 'Publish' tab within the Axialy system. It provides the structural markup for managing publication workflows, including modals for setting publication metadata (title/description), configuring publication expiration dates, managing stakeholder access via PINs and URLs, and initiating artifact refinements. The file acts as a container for dynamic content and interactive modal components that facilitate the deployment and maintenance of shared publication artifacts.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/content/assets/css/publish-tab.css"
  ],
  "purpose": "This file serves as the UI template for the 'Publish' tab within the Axialy system. It provides the structural markup for managing publication workflows, including modals for setting publication metadata (title/description), configuring publication expiration dates, managing stakeholder access via PINs and URLs, and initiating artifact refinements. The file acts as a container for dynamic content and interactive modal components that facilitate the deployment and maintenance of shared publication artifacts."
}
```

-------------------------------------------------
File #81
Path: /axialy-production-ui/var/www/html/axialy-ui/content/README.md

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/content/dashboard-tab.html
  - /axialy-production-ui/var/www/html/axialy-ui/content/generate-tab.html
  - /axialy-production-ui/var/www/html/axialy-ui/content/home-tab.html
  - /axialy-production-ui/var/www/html/axialy-ui/content/publish-tab.html
  - /axialy-production-ui/var/www/html/axialy-ui/content/refine-tab.html
  - /axialy-production-ui/var/www/html/axialy-ui/content/settings-tab.html
  - /axialy-production-ui/var/www/html/axialy-ui/content/submit-issue-overlay.html
  - /axialy-production-ui/var/www/html/axialy-ui/content/user-documentation.html

Purpose:
This README.md file serves as the documentation and manifest for the UI content directory. Its primary purpose is to inventory the HTML fragments and full-page templates that constitute the core user interface components (tabs and overlays) for the Axialy production application, providing a brief functional summary of each file's role within the system.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/content/dashboard-tab.html",
    "/axialy-production-ui/var/www/html/axialy-ui/content/generate-tab.html",
    "/axialy-production-ui/var/www/html/axialy-ui/content/home-tab.html",
    "/axialy-production-ui/var/www/html/axialy-ui/content/publish-tab.html",
    "/axialy-production-ui/var/www/html/axialy-ui/content/refine-tab.html",
    "/axialy-production-ui/var/www/html/axialy-ui/content/settings-tab.html",
    "/axialy-production-ui/var/www/html/axialy-ui/content/submit-issue-overlay.html",
    "/axialy-production-ui/var/www/html/axialy-ui/content/user-documentation.html"
  ],
  "purpose": "This README.md file serves as the documentation and manifest for the UI content directory. Its primary purpose is to inventory the HTML fragments and full-page templates that constitute the core user interface components (tabs and overlays) for the Axialy production application, providing a brief functional summary of each file's role within the system."
}
```

-------------------------------------------------
File #82
Path: /axialy-production-ui/var/www/html/axialy-ui/content/refine-tab.html

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/content/assets/css/refine-tab.css
  - /axialy-production-ui/var/www/html/axialy-ui/content/assets/img/axialy_cta.png

Purpose:
This file acts as a structural HTML template for the 'Refine' tab within the Axialy UI. It provides the layout for managing analysis packages, including UI elements for package selection, searching, and managing focus areas. It also defines multiple modal and overlay components (both legacy and new) used for user interactions, such as creating new focus areas, viewing package details, and accessing AI-driven 'Axialy Advisor' assessments. The file relies on external CSS for styling and includes image assets for the advisor call-to-action button.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/content/assets/css/refine-tab.css",
    "/axialy-production-ui/var/www/html/axialy-ui/content/assets/img/axialy_cta.png"
  ],
  "purpose": "This file acts as a structural HTML template for the 'Refine' tab within the Axialy UI. It provides the layout for managing analysis packages, including UI elements for package selection, searching, and managing focus areas. It also defines multiple modal and overlay components (both legacy and new) used for user interactions, such as creating new focus areas, viewing package details, and accessing AI-driven 'Axialy Advisor' assessments. The file relies on external CSS for styling and includes image assets for the advisor call-to-action button."
}
```

-------------------------------------------------
File #83
Path: /axialy-production-ui/var/www/html/axialy-ui/content/settings-tab.html

Referenced files:
  (none)

Purpose:
This file serves as a UI template for the 'Organization Settings' tab within the Axialy platform. Its primary functions are to provide a user interface for: 1) selecting an active organization context that filters data across the platform, 2) rendering a form for creating new custom organizations (including fields for contact info, website, notes, and logo uploads), and 3) displaying a summary list of existing custom organizations. It acts as a structural view that relies on external JavaScript (not referenced in this file) to handle form submission, data validation, and dynamic population of the organization list and dropdown elements.

Raw AI response:
```json
{
  "referenced_files": [],
  "purpose": "This file serves as a UI template for the 'Organization Settings' tab within the Axialy platform. Its primary functions are to provide a user interface for: 1) selecting an active organization context that filters data across the platform, 2) rendering a form for creating new custom organizations (including fields for contact info, website, notes, and logo uploads), and 3) displaying a summary list of existing custom organizations. It acts as a structural view that relies on external JavaScript (not referenced in this file) to handle form submission, data validation, and dynamic population of the organization list and dropdown elements."
}
```

-------------------------------------------------
File #84
Path: /axialy-production-ui/var/www/html/axialy-ui/content/submit-issue-overlay.html

Referenced files:
  (none)

Purpose:
This file is a UI component defining an HTML overlay (modal) for the 'Submit an Issue' feature. It provides the structure for a feedback or bug reporting form, including input fields for a title and description, and action buttons for submitting or canceling the request. As this file contains only HTML, the functional logic (the 'closeIssueOverlay' and 'submitIssue' JavaScript functions triggered by the onclick events) is expected to be defined in a separate script file not present in the provided context.

Raw AI response:
```json
{
  "referenced_files": [],
  "purpose": "This file is a UI component defining an HTML overlay (modal) for the 'Submit an Issue' feature. It provides the structure for a feedback or bug reporting form, including input fields for a title and description, and action buttons for submitting or canceling the request. As this file contains only HTML, the functional logic (the 'closeIssueOverlay' and 'submitIssue' JavaScript functions triggered by the onclick events) is expected to be defined in a separate script file not present in the provided context."
}
```

-------------------------------------------------
File #85
Path: /axialy-production-ui/var/www/html/axialy-ui/content/survey-tab.html

Referenced files:
  (none)

Purpose:
This file serves as a UI template (HTML fragment) for the 'Survey' tab within the Axialy dashboard. Its primary purpose is to provide an interface for users to view, filter, and paginate stakeholder feedback requests. It includes a collapsible filter form, a tabular display for feedback records (with dynamic placeholders for data injection), and pagination controls. As a front-end component, it relies on external JavaScript (not provided in this file) to handle the logic for filtering, table population, and modal interactions indicated by the comments.

Raw AI response:
```json
{
  "referenced_files": [],
  "purpose": "This file serves as a UI template (HTML fragment) for the 'Survey' tab within the Axialy dashboard. Its primary purpose is to provide an interface for users to view, filter, and paginate stakeholder feedback requests. It includes a collapsible filter form, a tabular display for feedback records (with dynamic placeholders for data injection), and pagination controls. As a front-end component, it relies on external JavaScript (not provided in this file) to handle the logic for filtering, table population, and modal interactions indicated by the comments."
}
```

-------------------------------------------------
File #86
Path: /axialy-production-ui/var/www/html/axialy-ui/content/user-documentation.html

Referenced files:
  - /assets/css/marketing.css
  - /axialy.ai/assets/css/styles.css

Purpose:
This file serves as the landing page or home view for the AxiaBA user documentation portal. It provides an introductory interface for users to navigate through various business analysis guides and offers helpful tips on how to interact with the documentation, such as downloading offline versions and contacting support. Note that the references to external CSS files are commented out, indicating they are not currently active in the rendered output.

Raw AI response:
{
  "referenced_files": [
    "/assets/css/marketing.css",
    "/axialy.ai/assets/css/styles.css"
  ],
  "purpose": "This file serves as the landing page or home view for the AxiaBA user documentation portal. It provides an introductory interface for users to navigate through various business analysis guides and offers helpful tips on how to interact with the documentation, such as downloading offline versions and contacting support. Note that the references to external CSS files are commented out, indicating they are not currently active in the rendered output."
}

-------------------------------------------------
File #87
Path: /axialy-production-ui/var/www/html/axialy-ui/docs/README.md

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/docs/view_document.php

Purpose:
This README.md file serves as documentation for the '/docs/' directory within the Axialy UI system. Its primary purpose is to describe the functionality of 'view_document.php', which is responsible for fetching documentation records from the database, rendering various formats (Markdown, HTML, JSON, text) for browser display, and handling document/version-specific file downloads.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/docs/view_document.php"
  ],
  "purpose": "This README.md file serves as documentation for the '/docs/' directory within the Axialy UI system. Its primary purpose is to describe the functionality of 'view_document.php', which is responsible for fetching documentation records from the database, rendering various formats (Markdown, HTML, JSON, text) for browser display, and handling document/version-specific file downloads."
}
```

-------------------------------------------------
File #88
Path: /axialy-production-ui/var/www/html/axialy-ui/docs/view_document.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php

Purpose:
The primary purpose of this file is to retrieve and display document content stored in the system database. It acts as a controller that fetches both document-level and active-version-level records based on a 'key' query parameter. It handles file delivery (PDF/DOCX) for both record levels and renders content dynamically in the browser, providing a custom Markdown-to-HTML conversion utility for documents stored in 'md' format while supporting alternative formats like HTML, JSON, or plain text.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php"
  ],
  "purpose": "The primary purpose of this file is to retrieve and display document content stored in the system database. It acts as a controller that fetches both document-level and active-version-level records based on a 'key' query parameter. It handles file delivery (PDF/DOCX) for both record levels and renders content dynamically in the browser, providing a custom Markdown-to-HTML conversion utility for documents stored in 'md' format while supporting alternative formats like HTML, JSON, or plain text."
}
```

-------------------------------------------------
File #89
Path: /axialy-production-ui/var/www/html/axialy-ui/includes/account_creation.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/Config.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/Mailer.php

Purpose:
The `AccountCreation` class serves as a service layer responsible for managing the user registration workflow. It handles email verification token generation, validates email uniqueness, facilitates the dispatch of transactional emails (verification and welcome emails) via the `Mailer` utility, and manages the transactional database operations required to provision a new user account and their default organization.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/Config.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/Mailer.php"
  ],
  "purpose": "The `AccountCreation` class serves as a service layer responsible for managing the user registration workflow. It handles email verification token generation, validates email uniqueness, facilitates the dispatch of transactional emails (verification and welcome emails) via the `Mailer` utility, and manages the transactional database operations required to provision a new user account and their default organization."
}
```

-------------------------------------------------
File #90
Path: /axialy-production-ui/var/www/html/axialy-ui/includes/api_auth.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/auth.php

Purpose:
The purpose of this file is to provide a central security middleware function, `validateApiAccess()`, specifically for API endpoints. It ensures that the requesting user has an active session and a valid, non-expired subscription status (including support for 'day' passes, trial periods, and standard active subscriptions). It relies on a globally defined `$pdo` object (likely initialized in the required `auth.php` file) to query user subscription data and enforces access control by terminating execution with appropriate JSON error responses and redirect instructions if validation fails.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/auth.php"
  ],
  "purpose": "The purpose of this file is to provide a central security middleware function, `validateApiAccess()`, specifically for API endpoints. It ensures that the requesting user has an active session and a valid, non-expired subscription status (including support for 'day' passes, trial periods, and standard active subscriptions). It relies on a globally defined `$pdo` object (likely initialized in the required `auth.php` file) to query user subscription data and enforces access control by terminating execution with appropriate JSON error responses and redirect instructions if validation fails."
}
```

-------------------------------------------------
File #91
Path: /axialy-production-ui/var/www/html/axialy-ui/includes/auth.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/debug_utils.php

Purpose:
The file `/includes/auth.php` serves as the central authentication and access control layer for the application. It initializes secure session management, enforces user authentication for protected pages, validates subscription status (including support for day passes, promo codes, and Stripe-managed monthly subscriptions), and ensures users have accepted the latest Terms of Service (TOS). It also provides maintenance utility functions to periodically prune expired database sessions and verification/reset tokens.

Raw AI response:
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/debug_utils.php"
  ],
  "purpose": "The file `/includes/auth.php` serves as the central authentication and access control layer for the application. It initializes secure session management, enforces user authentication for protected pages, validates subscription status (including support for day passes, promo codes, and Stripe-managed monthly subscriptions), and ensures users have accepted the latest Terms of Service (TOS). It also provides maintenance utility functions to periodically prune expired database sessions and verification/reset tokens."
}

-------------------------------------------------
File #92
Path: /axialy-production-ui/var/www/html/axialy-ui/includes/Config.php

Referenced files:
  - /axialy-production-ui/var/www/html/.env

Purpose:
This file serves as a singleton configuration manager for the Axialy-UI system. Its primary purpose is to aggregate application settings from environment variables or local '.env' files, providing a unified and consistent interface for other parts of the application to access critical configuration (such as database credentials, API keys for Stripe/Postmark, and service URLs). It implements the `ArrayAccess` interface to maintain backward compatibility with legacy code that expects an array-like syntax for configuration access.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/.env"
  ],
  "purpose": "This file serves as a singleton configuration manager for the Axialy-UI system. Its primary purpose is to aggregate application settings from environment variables or local '.env' files, providing a unified and consistent interface for other parts of the application to access critical configuration (such as database credentials, API keys for Stripe/Postmark, and service URLs). It implements the `ArrayAccess` interface to maintain backward compatibility with legacy code that expects an array-like syntax for configuration access."
}
```

-------------------------------------------------
File #93
Path: /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/.env

Purpose:
The primary purpose of this file is to establish and return a PDO database connection instance for the Axialy UI application. It dynamically manages database configuration by first checking system environment variables and falling back to a '.env' file located in the parent directory (which is populated during the deployment process). It includes validation to ensure all required database credentials are present and implements error handling to log connection failures internally while returning a generic 500 error to the client.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/.env"
  ],
  "purpose": "The primary purpose of this file is to establish and return a PDO database connection instance for the Axialy UI application. It dynamically manages database configuration by first checking system environment variables and falling back to a '.env' file located in the parent directory (which is populated during the deployment process). It includes validation to ensure all required database credentials are present and implements error handling to log connection failures internally while returning a generic 500 error to the client."
}
```

-------------------------------------------------
File #94
Path: /axialy-production-ui/var/www/html/axialy-ui/includes/debug_utils.php

Referenced files:
  (none)

Purpose:
This file serves as a global helper utility for the application, providing a standardized `debugLog` function. Its primary purpose is to format and record diagnostic information to the system's error log, including timestamps and optional variable data serialized via `print_r`. By wrapping this in a `function_exists` check, it ensures the utility can be safely included in multiple contexts without causing naming conflicts.

Raw AI response:
```json
{
  "referenced_files": [],
  "purpose": "This file serves as a global helper utility for the application, providing a standardized `debugLog` function. Its primary purpose is to format and record diagnostic information to the system's error log, including timestamps and optional variable data serialized via `print_r`. By wrapping this in a `function_exists` check, it ensures the utility can be safely included in multiple contexts without causing naming conflicts."
}
```

-------------------------------------------------
File #95
Path: /axialy-production-ui/var/www/html/axialy-ui/includes/focus_org_session.php

Referenced files:
  (none)

Purpose:
This file acts as a utility library for managing the 'focus organization' state for users within the application. It provides two primary functions: 'getFocusOrganization' to retrieve the currently active organization context for a specific user from the database, and 'setFocusOrganization' to update or clear the user's active organization context by interacting with the 'user_focus_organizations' table. It uses a transaction-based approach to ensure data integrity when updating user preferences.

Raw AI response:
```json
{
  "referenced_files": [],
  "purpose": "This file acts as a utility library for managing the 'focus organization' state for users within the application. It provides two primary functions: 'getFocusOrganization' to retrieve the currently active organization context for a specific user from the database, and 'setFocusOrganization' to update or clear the user's active organization context by interacting with the 'user_focus_organizations' table. It uses a transaction-based approach to ensure data integrity when updating user preferences."
}
```

-------------------------------------------------
File #96
Path: /axialy-production-ui/var/www/html/axialy-ui/includes/html_sanitizer.php

Referenced files:
  (none)

Purpose:
The file serves as a utility library for securing and optimizing HTML content destined for rendering in browser environments, specifically designed for iframe isolation. It provides two distinct security profiles: a standard 'publication' mode that strips all executable scripts and dangerous event handlers, and an 'interactive publication' mode that permits safe JavaScript and interactive event handlers (e.g., onclick) while blocking sensitive patterns like document.cookie access, window redirection, or dynamic script evaluation. It includes helper functions for CSS sanitization, structural validation, and the extraction/re-injection of embedded stylesheets to ensure clean, compliant HTML outputs.

Raw AI response:
{
  "referenced_files": [],
  "purpose": "The file serves as a utility library for securing and optimizing HTML content destined for rendering in browser environments, specifically designed for iframe isolation. It provides two distinct security profiles: a standard 'publication' mode that strips all executable scripts and dangerous event handlers, and an 'interactive publication' mode that permits safe JavaScript and interactive event handlers (e.g., onclick) while blocking sensitive patterns like document.cookie access, window redirection, or dynamic script evaluation. It includes helper functions for CSS sanitization, structural validation, and the extraction/re-injection of embedded stylesheets to ensure clean, compliant HTML outputs."
}

-------------------------------------------------
File #97
Path: /axialy-production-ui/var/www/html/axialy-ui/includes/Mailer.php

Referenced files:
  - /axialy-production-ui/var/www/html/.env

Purpose:
The `Mailer.php` class acts as a dedicated service layer for dispatching system-generated emails via the Postmark API. It replaces legacy mail delivery systems (SendGrid/PHPMailer) and provides specific methods for sending verification, welcome, feedback, and publication invitation emails. The class is responsible for loading configuration from an external `.env` file, preparing structured email payloads (HTML and plain text), and handling API communication using PHP's cURL extension.

Raw AI response:
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/.env"
  ],
  "purpose": "The `Mailer.php` class acts as a dedicated service layer for dispatching system-generated emails via the Postmark API. It replaces legacy mail delivery systems (SendGrid/PHPMailer) and provides specific methods for sending verification, welcome, feedback, and publication invitation emails. The class is responsible for loading configuration from an external `.env` file, preparing structured email payloads (HTML and plain text), and handling API communication using PHP's cURL extension."
}

-------------------------------------------------
File #98
Path: /axialy-production-ui/var/www/html/axialy-ui/includes/README.md

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/account_creation.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/api_auth.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/auth.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/debug_utils.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/focus_org_session.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/html_sanitizer.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/validate_subscription.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/validation.php

Purpose:
This file serves as the documentation/manifest for the `/includes/` directory. It outlines the specific responsibilities of each core PHP module used across the Axialy production UI, covering authentication, database connectivity, security sanitization, and business logic related to user accounts and subscription management.

Raw AI response:
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/account_creation.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/api_auth.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/auth.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/debug_utils.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/focus_org_session.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/html_sanitizer.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/validate_subscription.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/validation.php"
  ],
  "purpose": "This file serves as the documentation/manifest for the `/includes/` directory. It outlines the specific responsibilities of each core PHP module used across the Axialy production UI, covering authentication, database connectivity, security sanitization, and business logic related to user accounts and subscription management."
}

-------------------------------------------------
File #99
Path: /axialy-production-ui/var/www/html/axialy-ui/includes/validate_subscription.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/auth.php

Purpose:
This file serves as a JSON API endpoint responsible for validating the subscription status of an authenticated user. It retrieves the user's subscription metadata (subscription status, plan type, and trial expiration) from the 'ui_users' database table. It then calculates the validity of the user's access based on the current date, distinguishing between 'day' passes (which rely on trial expiration dates) and standard subscriptions. The file provides a standardized JSON response indicating whether the user has active access, suitable for client-side AJAX requests to gate features or pages.

Raw AI response:
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/auth.php"
  ],
  "purpose": "This file serves as a JSON API endpoint responsible for validating the subscription status of an authenticated user. It retrieves the user's subscription metadata (subscription status, plan type, and trial expiration) from the 'ui_users' database table. It then calculates the validity of the user's access based on the current date, distinguishing between 'day' passes (which rely on trial expiration dates) and standard subscriptions. The file provides a standardized JSON response indicating whether the user has active access, suitable for client-side AJAX requests to gate features or pages."
}

-------------------------------------------------
File #100
Path: /axialy-production-ui/var/www/html/axialy-ui/includes/validation.php

Referenced files:
  (none)

Purpose:
The file `/axialy-production-ui/var/www/html/axialy-ui/includes/validation.php` acts as a utility library providing helper functions for data validation across the application. It contains specialized validation logic for various form submissions and API data structures, including basic input checking, summary generation requests, analysis package header configurations, and content review request forms. It ensures that required fields are present and correctly formatted before data is processed by other parts of the system.

Raw AI response:
{
  "referenced_files": [],
  "purpose": "The file `/axialy-production-ui/var/www/html/axialy-ui/includes/validation.php` acts as a utility library providing helper functions for data validation across the application. It contains specialized validation logic for various form submissions and API data structures, including basic input checking, summary generation requests, analysis package header configurations, and content review request forms. It ensures that required fields are present and correctly formatted before data is processed by other parts of the system."
}

-------------------------------------------------
File #101
Path: /axialy-production-ui/var/www/html/axialy-ui/js/generate/augment-existing-package.js

Referenced files:
  (none)

Purpose:
The file '/axialy-production-ui/var/www/html/axialy-ui/js/generate/augment-existing-package.js' appears to be a client-side JavaScript module designed to handle the logic for modifying or adding components to an already defined software package. Given the path and naming convention, it likely interacts with an API or a form interface to inject new configurations or dependencies into an existing project structure within the Axialy UI system. Note: As the content was empty/not provided in the context, this purpose is inferred from the file path and naming structure.

Raw AI response:
{
  "referenced_files": [],
  "purpose": "The file '/axialy-production-ui/var/www/html/axialy-ui/js/generate/augment-existing-package.js' appears to be a client-side JavaScript module designed to handle the logic for modifying or adding components to an already defined software package. Given the path and naming convention, it likely interacts with an API or a form interface to inject new configurations or dependencies into an existing project structure within the Axialy UI system. Note: As the content was empty/not provided in the context, this purpose is inferred from the file path and naming structure."
}

-------------------------------------------------
File #102
Path: /axialy-production-ui/var/www/html/axialy-ui/js/generate/index.js

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/content/generate-tab.html

Purpose:
This module acts as the orchestrator for the 'Generate' tab functionality. Its primary purpose is to asynchronously load the 'generate-tab.html' template into the application's overview panel and subsequently initialize various feature-specific modules (such as InputTextModule, FocusAreasModule, ProcessFeedbackModule, DynamicRibbonsModule, and FocusAreaVersionModule). It is designed to be invoked by 'layout.js' when the user navigates to the Generate section, handles subscription-based access control (via 401 response checks), and ensures the UI components within the generated content are properly bound and focused.

Raw AI response:
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/content/generate-tab.html"
  ],
  "purpose": "This module acts as the orchestrator for the 'Generate' tab functionality. Its primary purpose is to asynchronously load the 'generate-tab.html' template into the application's overview panel and subsequently initialize various feature-specific modules (such as InputTextModule, FocusAreasModule, ProcessFeedbackModule, DynamicRibbonsModule, and FocusAreaVersionModule). It is designed to be invoked by 'layout.js' when the user navigates to the Generate section, handles subscription-based access control (via 401 response checks), and ensures the UI components within the generated content are properly bound and focused."
}

-------------------------------------------------
File #103
Path: /axialy-production-ui/var/www/html/axialy-ui/js/generate/README.md

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/js/generate/content/generate-tab.html
  - /axialy-production-ui/var/www/html/axialy-ui/js/generate/fetch_active_packages_for_save.php
  - /axialy-production-ui/var/www/html/axialy-ui/js/generate/save_data_existing_package.php

Purpose:
This README file serves as documentation for the '/js/generate/' directory, which contains the core JavaScript modules responsible for the 'Generate' tab functionality in the Axialy UI. It outlines the architecture of the tab, including initialization processes, UI interaction handling (collapsible ribbons), and the logic for saving data (either as a new package or appended to an existing one).

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/js/generate/content/generate-tab.html",
    "/axialy-production-ui/var/www/html/axialy-ui/js/generate/fetch_active_packages_for_save.php",
    "/axialy-production-ui/var/www/html/axialy-ui/js/generate/save_data_existing_package.php"
  ],
  "purpose": "This README file serves as documentation for the '/js/generate/' directory, which contains the core JavaScript modules responsible for the 'Generate' tab functionality in the Axialy UI. It outlines the architecture of the tab, including initialization processes, UI interaction handling (collapsible ribbons), and the logic for saving data (either as a new package or appended to an existing one)."
}
```

-------------------------------------------------
File #104
Path: /axialy-production-ui/var/www/html/axialy-ui/js/generate/save-data-destination-overlay.js

Referenced files:
  (none)

Purpose:
The file '/axialy-production-ui/var/www/html/axialy-ui/js/generate/save-data-destination-overlay.js' appears to be an empty file. Without content, it is impossible to determine its specific functional purpose or identify any internal dependencies, imports, or external scripts it might reference. If this is part of the 'axialy' UI framework, it is likely intended to house the JavaScript logic for an overlay component used when a user chooses a destination to save generated data, but currently, it serves no functional role.

Raw AI response:
{
  "referenced_files": [],
  "purpose": "The file '/axialy-production-ui/var/www/html/axialy-ui/js/generate/save-data-destination-overlay.js' appears to be an empty file. Without content, it is impossible to determine its specific functional purpose or identify any internal dependencies, imports, or external scripts it might reference. If this is part of the 'axialy' UI framework, it is likely intended to house the JavaScript logic for an overlay component used when a user chooses a destination to save generated data, but currently, it serves no functional role."
}

-------------------------------------------------
File #105
Path: /axialy-production-ui/var/www/html/axialy-ui/js/generate/save-data-enhancement.js

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/js/generate/fetch_active_packages_for_save.php
  - /axialy-production-ui/var/www/html/axialy-ui/js/generate/save_data_existing_package.php

Purpose:
This JavaScript file provides a UI enhancement for the data-saving process in the Axialy application. It intercepts the click event on the '#save-data-btn' and introduces a custom overlay that allows users to choose between saving generated data as a new package or adding it to an existing one. It manages the lifecycle of these overlays (creation, rendering, interaction, and cleanup) and makes asynchronous calls to backend PHP endpoints to fetch available packages and persist the selected data. Note that the script relies on external global objects like 'ProcessFeedbackModule' and 'DynamicRibbonsModule', which are expected to exist in the broader application environment.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/js/generate/fetch_active_packages_for_save.php",
    "/axialy-production-ui/var/www/html/axialy-ui/js/generate/save_data_existing_package.php"
  ],
  "purpose": "This JavaScript file provides a UI enhancement for the data-saving process in the Axialy application. It intercepts the click event on the '#save-data-btn' and introduces a custom overlay that allows users to choose between saving generated data as a new package or adding it to an existing one. It manages the lifecycle of these overlays (creation, rendering, interaction, and cleanup) and makes asynchronous calls to backend PHP endpoints to fetch available packages and persist the selected data. Note that the script relies on external global objects like 'ProcessFeedbackModule' and 'DynamicRibbonsModule', which are expected to exist in the broader application environment."
}
```

-------------------------------------------------
File #106
Path: /axialy-production-ui/var/www/html/axialy-ui/js/generate/ui.js

Referenced files:
  (none)

Purpose:
The `GenerateUIModule` is a client-side JavaScript module designed to manage UI interactivity within the generation interface. Its primary function is to initialize 'ribbon' toggles, which allow users to expand or collapse specific sections of the UI (specifically those marked with classes `.input-ribbon` or `.feedback-ribbon`). It also manages a default state for specific elements, such as the 'Choose AI Focus Areas' section, ensuring it appears expanded upon initialization. The module includes a loose coupling to `ProcessFeedbackModule`, triggering a UI update for save buttons whenever a ribbon is toggled, provided that module is loaded in the global scope.

Raw AI response:
```json
{
  "referenced_files": [],
  "purpose": "The `GenerateUIModule` is a client-side JavaScript module designed to manage UI interactivity within the generation interface. Its primary function is to initialize 'ribbon' toggles, which allow users to expand or collapse specific sections of the UI (specifically those marked with classes `.input-ribbon` or `.feedback-ribbon`). It also manages a default state for specific elements, such as the 'Choose AI Focus Areas' section, ensuring it appears expanded upon initialization. The module includes a loose coupling to `ProcessFeedbackModule`, triggering a UI update for save buttons whenever a ribbon is toggled, provided that module is loaded in the global scope."
}
```

-------------------------------------------------
File #107
Path: /axialy-production-ui/var/www/html/axialy-ui/js/home/home-tab.js

Referenced files:
  - content/home-tab.html
  - /axialy_helper.php
  - /store_summary.php
  - /ai_helper.php
  - /get_focus_organization.php
  - /save_analysis_package.php

Purpose:
The primary purpose of this file is to manage the 'Home' tab functionality of the Axialy UI. It handles user input collection, triggers AI-driven analysis via external API calls, dynamically renders the analysis results into the DOM, and facilitates the creation of persistent 'Analysis Packages' from those results. It also maintains UI state—such as progress steps, form validation, and smooth scrolling—and integrates with a global 'OverlayModule' to manage user interactions for saving and reviewing package data.

Raw AI response:
{
  "referenced_files": [
    "content/home-tab.html",
    "/axialy_helper.php",
    "/store_summary.php",
    "/ai_helper.php",
    "/get_focus_organization.php",
    "/save_analysis_package.php"
  ],
  "purpose": "The primary purpose of this file is to manage the 'Home' tab functionality of the Axialy UI. It handles user input collection, triggers AI-driven analysis via external API calls, dynamically renders the analysis results into the DOM, and facilitates the creation of persistent 'Analysis Packages' from those results. It also maintains UI state—such as progress steps, form validation, and smooth scrolling—and integrates with a global 'OverlayModule' to manage user interactions for saving and reviewing package data."
}

-------------------------------------------------
File #108
Path: /axialy-production-ui/var/www/html/axialy-ui/js/home/README.md

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/js/home/home-tab.js
  - /axialy-production-ui/var/www/html/axialy-ui/js/home/content/home-tab.html
  - /axialy-production-ui/var/www/html/axialy-ui/axialy_helper.php
  - /axialy-production-ui/var/www/html/axialy-ui/store_summary.php
  - /axialy-production-ui/var/www/html/axialy-ui/save_analysis_package.php

Purpose:
This README acts as the architectural documentation for the 'Home' tab functionality. It describes the lifecycle of a user's interaction: from submitting a prompt to the AI, receiving and rendering structured advice, and finally bootstrapping a new analysis package. The file serves as a manifest for the logic contained in home-tab.js, detailing the integration points with the backend PHP scripts and the template-based UI injection.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/js/home/home-tab.js",
    "/axialy-production-ui/var/www/html/axialy-ui/js/home/content/home-tab.html",
    "/axialy-production-ui/var/www/html/axialy-ui/axialy_helper.php",
    "/axialy-production-ui/var/www/html/axialy-ui/store_summary.php",
    "/axialy-production-ui/var/www/html/axialy-ui/save_analysis_package.php"
  ],
  "purpose": "This README acts as the architectural documentation for the 'Home' tab functionality. It describes the lifecycle of a user's interaction: from submitting a prompt to the AI, receiving and rendering structured advice, and finally bootstrapping a new analysis package. The file serves as a manifest for the logic contained in home-tab.js, detailing the integration points with the backend PHP scripts and the template-based UI injection."
}
```

-------------------------------------------------
File #109
Path: /axialy-production-ui/var/www/html/axialy-ui/js/modules/README.md

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/js/modules/subscription-validation-module.js
  - /axialy-production-ui/var/www/html/axialy-ui/js/modules/tab-navigation-module.js
  - /axialy-production-ui/var/www/html/axialy-ui/js/modules/ui-utils-module.js
  - /includes/validate_subscription.php
  - /subscription.php

Purpose:
This README.md file serves as documentation for the shared JavaScript modules located in the /js/modules/ directory. Its primary purpose is to outline the architectural role and key functionalities of three core modules: subscription validation, tab navigation, and UI utilities, which collectively manage state, cross-tab consistency, and visual presentation across the application.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/js/modules/subscription-validation-module.js",
    "/axialy-production-ui/var/www/html/axialy-ui/js/modules/tab-navigation-module.js",
    "/axialy-production-ui/var/www/html/axialy-ui/js/modules/ui-utils-module.js",
    "/includes/validate_subscription.php",
    "/subscription.php"
  ],
  "purpose": "This README.md file serves as documentation for the shared JavaScript modules located in the /js/modules/ directory. Its primary purpose is to outline the architectural role and key functionalities of three core modules: subscription validation, tab navigation, and UI utilities, which collectively manage state, cross-tab consistency, and visual presentation across the application."
}
```

-------------------------------------------------
File #110
Path: /axialy-production-ui/var/www/html/axialy-ui/js/modules/subscription-validation-module.js

Referenced files:
  - /includes/validate_subscription.php
  - /subscription.php

Purpose:
The purpose of this file is to act as a client-side utility module that enforces subscription requirements for the application. It performs an asynchronous check against the server via '/includes/validate_subscription.php' to determine if the current session's subscription is valid. If the validation fails or the server returns an unauthorized status (401), the module forces a browser redirect to '/subscription.php' to handle the subscription status.

Raw AI response:
```json
{
  "referenced_files": [
    "/includes/validate_subscription.php",
    "/subscription.php"
  ],
  "purpose": "The purpose of this file is to act as a client-side utility module that enforces subscription requirements for the application. It performs an asynchronous check against the server via '/includes/validate_subscription.php' to determine if the current session's subscription is valid. If the validation fails or the server returns an unauthorized status (401), the module forces a browser redirect to '/subscription.php' to handle the subscription status."
}
```

-------------------------------------------------
File #111
Path: /axialy-production-ui/var/www/html/axialy-ui/js/modules/ui-utils-module.js

Referenced files:
  (none)

Purpose:
The `ui-utils-module.js` file serves as a helper module within the Axialy UI framework. Its primary purpose is to provide reusable utility functions for DOM manipulation and state synchronization, specifically: 1) Updating the browser document title and synchronizing a 'views-menu' dropdown element when the application tab changes; 2) Dynamically applying background image and opacity settings to the '.page-container' via CSS custom properties based on data attributes; and 3) Dynamically adjusting the height of the '.overview-panel' based on the window's viewport height and the dimensions of the header and footer. It does not explicitly reference or import other files, relying instead on direct DOM selection and manipulation.

Raw AI response:
{
  "referenced_files": [],
  "purpose": "The `ui-utils-module.js` file serves as a helper module within the Axialy UI framework. Its primary purpose is to provide reusable utility functions for DOM manipulation and state synchronization, specifically: 1) Updating the browser document title and synchronizing a 'views-menu' dropdown element when the application tab changes; 2) Dynamically applying background image and opacity settings to the '.page-container' via CSS custom properties based on data attributes; and 3) Dynamically adjusting the height of the '.overview-panel' based on the window's viewport height and the dimensions of the header and footer. It does not explicitly reference or import other files, relying instead on direct DOM selection and manipulation."
}

-------------------------------------------------
File #112
Path: /axialy-production-ui/var/www/html/axialy-ui/js/publish/events/expiry-management-events.js

Referenced files:
  - /update_publication_expiry.php

Purpose:
This file is a JavaScript module responsible for managing the publication expiry dates within the UI. It provides functionality to: 1) capture user interactions on specific 'expiry-related' buttons, 2) dynamically generate a modal overlay that allows users to either set a custom expiry date or select from predefined time intervals (1 day, 1 week, 30 days, 90 days), 3) provide an option to remove expiration entirely, and 4) communicate these updates to the backend via the `/update_publication_expiry.php` endpoint. It relies on external modules like `PublishStateModule` for managing artifact data and `PublishUIModule` for UI notifications, loading states, and DOM re-rendering.

Raw AI response:
{
  "referenced_files": [
    "/update_publication_expiry.php"
  ],
  "purpose": "This file is a JavaScript module responsible for managing the publication expiry dates within the UI. It provides functionality to: 1) capture user interactions on specific 'expiry-related' buttons, 2) dynamically generate a modal overlay that allows users to either set a custom expiry date or select from predefined time intervals (1 day, 1 week, 30 days, 90 days), 3) provide an option to remove expiration entirely, and 4) communicate these updates to the backend via the `/update_publication_expiry.php` endpoint. It relies on external modules like `PublishStateModule` for managing artifact data and `PublishUIModule` for UI notifications, loading states, and DOM re-rendering."
}

-------------------------------------------------
File #113
Path: /axialy-production-ui/var/www/html/axialy-ui/js/publish/events/publication-settings-events.js

Referenced files:
  - /publish_artifact.php

Purpose:
This file manages the UI event handling and modal interaction for configuring publication settings before an artifact is officially published. It provides the user with an overlay to define a publication title, description, and custom expiration settings (or no expiration). Upon confirmation, it communicates with the server via the '/publish_artifact.php' endpoint and, on success, transitions the UI to a subsequent step for inviting stakeholders. The module relies on external global modules ('PublishStateModule', 'PublishUIModule', and 'PublishUtilsModule') to manage state, UI feedback, and input sanitization.

Raw AI response:
```json
{
  "referenced_files": [
    "/publish_artifact.php"
  ],
  "purpose": "This file manages the UI event handling and modal interaction for configuring publication settings before an artifact is officially published. It provides the user with an overlay to define a publication title, description, and custom expiration settings (or no expiration). Upon confirmation, it communicates with the server via the '/publish_artifact.php' endpoint and, on success, transitions the UI to a subsequent step for inviting stakeholders. The module relies on external global modules ('PublishStateModule', 'PublishUIModule', and 'PublishUtilsModule') to manage state, UI feedback, and input sanitization."
}
```

-------------------------------------------------
File #114
Path: /axialy-production-ui/var/www/html/axialy-ui/js/publish/events/stakeholder-invitation-events.js

Referenced files:
  (none)

Purpose:
This module, `PublishStakeholderInvitationEvents`, manages the interactive UI lifecycle for stakeholder invitations within the publication process. It handles DOM event listeners for buttons that add stakeholders (from packages or contributors), validate/add ad-hoc email addresses, clear lists, and trigger the actual invitation dispatching process via `PublishAPIModule`. It also contains the logic to dynamically generate and manage a modal overlay for inviting stakeholders to existing publications, ensuring that user interactions are properly tracked and cleaned up. Note: This file relies on several global modules (`PublishStateModule`, `PublishUIModule`, `PublishAPIModule`, `PublishUtilsModule`, and `PublishEventsModule`) which are expected to be loaded in the environment but are not explicitly imported in the file content.

Raw AI response:
{
  "referenced_files": [],
  "purpose": "This module, `PublishStakeholderInvitationEvents`, manages the interactive UI lifecycle for stakeholder invitations within the publication process. It handles DOM event listeners for buttons that add stakeholders (from packages or contributors), validate/add ad-hoc email addresses, clear lists, and trigger the actual invitation dispatching process via `PublishAPIModule`. It also contains the logic to dynamically generate and manage a modal overlay for inviting stakeholders to existing publications, ensuring that user interactions are properly tracked and cleaned up. Note: This file relies on several global modules (`PublishStateModule`, `PublishUIModule`, `PublishAPIModule`, `PublishUtilsModule`, and `PublishEventsModule`) which are expected to be loaded in the environment but are not explicitly imported in the file content."
}

-------------------------------------------------
File #115
Path: /axialy-production-ui/var/www/html/axialy-ui/js/publish/api.js

Referenced files:
  - /get_analysis_packages_for_publish.php
  - /get_published_artifacts.php
  - /clone_published_artifact.php
  - /get_package_focus_areas_for_publish.php
  - /update_focus_organization.php
  - /get_custom_organizations.php
  - /generate_publication_suggestions.php
  - /generate_publication_artifact.php
  - /publish_artifact.php
  - /get_package_stakeholders.php
  - /get_package_contributors.php
  - /send_publication_invitations.php
  - https://api.axiaba.com/axialy_helper.php

Purpose:
The `PublishAPIModule` is a client-side JavaScript service that acts as the primary interface for the 'Publish' workflow within the Axialy UI. It orchestrates communication between the frontend and various PHP backend endpoints to manage analysis packages, publication artifacts, and stakeholder communications. Its core functionality includes fetching project metadata, generating and revising publication content via an external AI API (Axiaba), handling custom HTML inputs without AI interference, and finalizing the publication of artifacts to stakeholders.

Raw AI response:
{
  "referenced_files": [
    "/get_analysis_packages_for_publish.php",
    "/get_published_artifacts.php",
    "/clone_published_artifact.php",
    "/get_package_focus_areas_for_publish.php",
    "/update_focus_organization.php",
    "/get_custom_organizations.php",
    "/generate_publication_suggestions.php",
    "/generate_publication_artifact.php",
    "/publish_artifact.php",
    "/get_package_stakeholders.php",
    "/get_package_contributors.php",
    "/send_publication_invitations.php",
    "https://api.axiaba.com/axialy_helper.php"
  ],
  "purpose": "The `PublishAPIModule` is a client-side JavaScript service that acts as the primary interface for the 'Publish' workflow within the Axialy UI. It orchestrates communication between the frontend and various PHP backend endpoints to manage analysis packages, publication artifacts, and stakeholder communications. Its core functionality includes fetching project metadata, generating and revising publication content via an external AI API (Axiaba), handling custom HTML inputs without AI interference, and finalizing the publication of artifacts to stakeholders."
}

-------------------------------------------------
File #116
Path: /axialy-production-ui/var/www/html/axialy-ui/js/publish/events.js

Referenced files:
  - /view_publication.php
  - /get_package_focus_areas_for_publish.php

Purpose:
The `PublishEventsModule` serves as the centralized event-handling and orchestration layer for the 'Publish' feature in the UI. It manages user interactions across the entire publishing workflow, including organization selection, package browsing, AI-assisted artifact generation, manual HTML content input, and stakeholder invitation management. 

Key functions include:
- Binding and tracking global event listeners to the document to manage UI lifecycle.
- Facilitating state transitions and view updates by coordinating between other modules (e.g., `PublishAPIModule` for data, `PublishStateModule` for application state, and `PublishUIModule` for rendering).
- Handling specific UI logic for workflows like 'Clone,' 'Preview HTML,' 'Generate Artifact,' and 'Invite Stakeholders.'

Note: The file relies heavily on external global modules (`PublishUIModule`, `PublishAPIModule`, `PublishStateModule`, `PublishUtilsModule`, etc.) that are expected to be loaded in the same environment. It also references legacy external modules (`PublishStakeholderInvitationEvents`, `PublishExpiryManagementEvents`, `PublishPublicationSettingsEvents`) for specific modal functionality.

Raw AI response:
```json
{
  "referenced_files": [
    "/view_publication.php",
    "/get_package_focus_areas_for_publish.php"
  ],
  "purpose": "The `PublishEventsModule` serves as the centralized event-handling and orchestration layer for the 'Publish' feature in the UI. It manages user interactions across the entire publishing workflow, including organization selection, package browsing, AI-assisted artifact generation, manual HTML content input, and stakeholder invitation management. \n\nKey functions include:\n- Binding and tracking global event listeners to the document to manage UI lifecycle.\n- Facilitating state transitions and view updates by coordinating between other modules (e.g., `PublishAPIModule` for data, `PublishStateModule` for application state, and `PublishUIModule` for rendering).\n- Handling specific UI logic for workflows like 'Clone,' 'Preview HTML,' 'Generate Artifact,' and 'Invite Stakeholders.'\n\nNote: The file relies heavily on external global modules (`PublishUIModule`, `PublishAPIModule`, `PublishStateModule`, `PublishUtilsModule`, etc.) that are expected to be loaded in the same environment. It also references legacy external modules (`PublishStakeholderInvitationEvents`, `PublishExpiryManagementEvents`, `PublishPublicationSettingsEvents`) for specific modal functionality."
}
```

-------------------------------------------------
File #117
Path: /axialy-production-ui/var/www/html/axialy-ui/js/publish/html-input.js

Referenced files:
  - PublishStateModule
  - PublishUIModule
  - PublishUtilsModule
  - PublishEventsModule
  - PublishAPIModule

Purpose:
The `PublishHtmlInputModule` serves as a dedicated component for collecting, validating, and previewing raw HTML content within the publishing workflow. It provides an interface for users to input custom HTML, ensuring it is preserved exactly as provided (with no sanitization or modification) for publication. The module handles real-time input validation, UI state management via the `PublishStateModule`, and renders the HTML input/review steps within the application's publishing UI. Note: The file references several global objects (e.g., `PublishStateModule`, `PublishUIModule`) which are expected to be defined elsewhere in the system.

Raw AI response:
```json
{
  "referenced_files": [
    "PublishStateModule",
    "PublishUIModule",
    "PublishUtilsModule",
    "PublishEventsModule",
    "PublishAPIModule"
  ],
  "purpose": "The `PublishHtmlInputModule` serves as a dedicated component for collecting, validating, and previewing raw HTML content within the publishing workflow. It provides an interface for users to input custom HTML, ensuring it is preserved exactly as provided (with no sanitization or modification) for publication. The module handles real-time input validation, UI state management via the `PublishStateModule`, and renders the HTML input/review steps within the application's publishing UI. Note: The file references several global objects (e.g., `PublishStateModule`, `PublishUIModule`) which are expected to be defined elsewhere in the system."
}
```

-------------------------------------------------
File #118
Path: /axialy-production-ui/var/www/html/axialy-ui/js/publish/index.js

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/js/publish/PublishEventsModule.js
  - /axialy-production-ui/var/www/html/axialy-ui/js/publish/PublishStateModule.js
  - /axialy-production-ui/var/www/html/axialy-ui/js/publish/PublishUIModule.js

Purpose:
The `PublishIndexModule` acts as the primary entry point and controller for the 'Publish' tab within the Axialy UI. Its functional purpose is to manage the lifecycle of the Publish interface, including initialization, cleanup, state reset, and the orchestration of event listeners and main view loading. It relies on global module variables (PublishEventsModule, PublishStateModule, and PublishUIModule) to handle specific business logic, state management, and UI feedback, respectively.

Raw AI response:
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/js/publish/PublishEventsModule.js",
    "/axialy-production-ui/var/www/html/axialy-ui/js/publish/PublishStateModule.js",
    "/axialy-production-ui/var/www/html/axialy-ui/js/publish/PublishUIModule.js"
  ],
  "purpose": "The `PublishIndexModule` acts as the primary entry point and controller for the 'Publish' tab within the Axialy UI. Its functional purpose is to manage the lifecycle of the Publish interface, including initialization, cleanup, state reset, and the orchestration of event listeners and main view loading. It relies on global module variables (PublishEventsModule, PublishStateModule, and PublishUIModule) to handle specific business logic, state management, and UI feedback, respectively."
}

-------------------------------------------------
File #119
Path: /axialy-production-ui/var/www/html/axialy-ui/js/publish/README.md

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/js/publish/index.js
  - /issue_ajax_actions.php

Purpose:
This file serves as documentation for the 'Publish' module within the Axialy UI. It outlines the functionality of the `PublishIndexModule`, which manages the user interface for submitting feature requests or ideas, including DOM interaction, input validation, and asynchronous communication with the server via the `/issue_ajax_actions.php` endpoint.

Raw AI response:
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/js/publish/index.js",
    "/issue_ajax_actions.php"
  ],
  "purpose": "This file serves as documentation for the 'Publish' module within the Axialy UI. It outlines the functionality of the `PublishIndexModule`, which manages the user interface for submitting feature requests or ideas, including DOM interaction, input validation, and asynchronous communication with the server via the `/issue_ajax_actions.php` endpoint."
}

-------------------------------------------------
File #120
Path: /axialy-production-ui/var/www/html/axialy-ui/js/publish/state.js

Referenced files:
  (none)

Purpose:
The `PublishStateModule` serves as a centralized state container for the front-end publication workflow within the Axialy application. It uses the revealing module pattern to manage the application's reactive state across multiple steps of the artifact creation and publishing process. Specifically, it tracks UI view state, organizational context, analysis package selections, focus areas, content generation (including new HTML input support), and stakeholder communication details. By providing getter and setter methods for each piece of state, it ensures a consistent data interface for other controller modules or UI components to interact with the publication lifecycle.

Raw AI response:
{
  "referenced_files": [],
  "purpose": "The `PublishStateModule` serves as a centralized state container for the front-end publication workflow within the Axialy application. It uses the revealing module pattern to manage the application's reactive state across multiple steps of the artifact creation and publishing process. Specifically, it tracks UI view state, organizational context, analysis package selections, focus areas, content generation (including new HTML input support), and stakeholder communication details. By providing getter and setter methods for each piece of state, it ensures a consistent data interface for other controller modules or UI components to interact with the publication lifecycle."
}

-------------------------------------------------
File #121
Path: /axialy-production-ui/var/www/html/axialy-ui/js/publish/ui.js

Referenced files:
  - /js/publish/ui.js

Purpose:
The `PublishUIModule` serves as the primary front-end rendering layer for the publication workflow within the Axialy UI. It provides functions to dynamically inject HTML content into the DOM for key stages of the publishing process, including organization selection, displaying published artifacts, browsing analysis packages, handling custom HTML inputs with CSS isolation, and managing AI-driven generation and revision of artifacts. It relies on other modules—`PublishUtilsModule`, `PublishStateModule`, and `PublishAPIModule`—to handle data sanitation, application state, and API communication, respectively.

Raw AI response:
{
  "referenced_files": [
    "/js/publish/ui.js"
  ],
  "purpose": "The `PublishUIModule` serves as the primary front-end rendering layer for the publication workflow within the Axialy UI. It provides functions to dynamically inject HTML content into the DOM for key stages of the publishing process, including organization selection, displaying published artifacts, browsing analysis packages, handling custom HTML inputs with CSS isolation, and managing AI-driven generation and revision of artifacts. It relies on other modules—`PublishUtilsModule`, `PublishStateModule`, and `PublishAPIModule`—to handle data sanitation, application state, and API communication, respectively."
}

-------------------------------------------------
File #122
Path: /axialy-production-ui/var/www/html/axialy-ui/js/publish/utils.js

Referenced files:
  (none)

Purpose:
The file serves as a utility module for the publishing section of the frontend application. It provides three helper functions: 'sanitizeHTML' to safely escape strings for injection into the DOM, 'createToast' to programmatically generate Bootstrap-styled toast notification elements, and 'debounce' to limit the frequency of function execution. The module uses an Immediately Invoked Function Expression (IIFE) to encapsulate these utilities and expose them via the 'PublishUtilsModule' namespace. No external files are referenced within the provided code.

Raw AI response:
{
  "referenced_files": [],
  "purpose": "The file serves as a utility module for the publishing section of the frontend application. It provides three helper functions: 'sanitizeHTML' to safely escape strings for injection into the DOM, 'createToast' to programmatically generate Bootstrap-styled toast notification elements, and 'debounce' to limit the frequency of function execution. The module uses an Immediately Invoked Function Expression (IIFE) to encapsulate these utilities and expose them via the 'PublishUtilsModule' namespace. No external files are referenced within the provided code."
}

-------------------------------------------------
File #123
Path: /axialy-production-ui/var/www/html/axialy-ui/js/refine/actions.js

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/js/refine/RefineStateModule
  - /axialy-production-ui/var/www/html/axialy-ui/js/refine/RefineUtilsModule
  - /axialy-production-ui/var/www/html/axialy-ui/js/refine/RefineApiModule
  - /axialy-production-ui/var/www/html/axialy-ui/js/refine/EnhanceContentModule
  - /axialy-production-ui/var/www/html/axialy-ui/js/refine/ContentReviewModule
  - /axialy-production-ui/var/www/html/axialy-ui/js/refine/CollateFeedbackModule
  - /axialy-production-ui/var/www/html/axialy-ui/js/refine/RecoverFocusAreaModule
  - /axialy-production-ui/var/www/html/axialy-ui/js/refine/ContentRevisionModule
  - /axialy-production-ui/var/www/html/axialy-ui/js/refine/RefineEventsModule

Purpose:
The `RefineActionsModule` acts as a central dispatcher for administrative and editorial activities related to 'Focus Areas' within the UI. It maps high-level user actions (like 'Enhance Content', 'Request Feedback', or 'Delete Focus Area Data') to their specific implementation modules. It is designed to be invoked by `RefineEventsModule.toggleRefineDropdown()`, retrieves necessary state information via `RefineStateModule`, and delegates functional execution to dedicated modules or the `RefineApiModule`. Note: The file assumes the existence of several global `window` objects (e.g., `EnhanceContentModule`, `ContentReviewModule`) which are not explicitly defined here but are required for the module to function.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/js/refine/RefineStateModule",
    "/axialy-production-ui/var/www/html/axialy-ui/js/refine/RefineUtilsModule",
    "/axialy-production-ui/var/www/html/axialy-ui/js/refine/RefineApiModule",
    "/axialy-production-ui/var/www/html/axialy-ui/js/refine/EnhanceContentModule",
    "/axialy-production-ui/var/www/html/axialy-ui/js/refine/ContentReviewModule",
    "/axialy-production-ui/var/www/html/axialy-ui/js/refine/CollateFeedbackModule",
    "/axialy-production-ui/var/www/html/axialy-ui/js/refine/RecoverFocusAreaModule",
    "/axialy-production-ui/var/www/html/axialy-ui/js/refine/ContentRevisionModule",
    "/axialy-production-ui/var/www/html/axialy-ui/js/refine/RefineEventsModule"
  ],
  "purpose": "The `RefineActionsModule` acts as a central dispatcher for administrative and editorial activities related to 'Focus Areas' within the UI. It maps high-level user actions (like 'Enhance Content', 'Request Feedback', or 'Delete Focus Area Data') to their specific implementation modules. It is designed to be invoked by `RefineEventsModule.toggleRefineDropdown()`, retrieves necessary state information via `RefineStateModule`, and delegates functional execution to dedicated modules or the `RefineApiModule`. Note: The file assumes the existence of several global `window` objects (e.g., `EnhanceContentModule`, `ContentReviewModule`) which are not explicitly defined here but are required for the module to function."
}
```

-------------------------------------------------
File #124
Path: /axialy-production-ui/var/www/html/axialy-ui/js/refine/api.js

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/api/get_analysis_packages_with_metrics.php
  - /axialy-production-ui/var/www/html/axialy-ui/js/refine/fetch_analysis_package_focus_area_records.php
  - /axialy-production-ui/var/www/html/axialy-ui/js/refine/config/refine-activities.json
  - /axialy-production-ui/var/www/html/axialy-ui/js/refine/fetch_stakeholder_feedback.php
  - /axialy-production-ui/var/www/html/axialy-ui/js/refine/process_delete_focus_area_data.php

Purpose:
The `api.js` file serves as a centralized JavaScript module (using the revealing module pattern) that encapsulates all network communication for the 'refine' feature set. It acts as an abstraction layer between the frontend UI and various backend PHP endpoints and configuration files, handling data fetching for analysis packages, focus-area records, stakeholder feedback, and activity configuration, as well as managing the deletion of focus-area data. Note: The paths for the referenced files are inferred relative to the directory of the current file (`/axialy-production-ui/var/www/html/axialy-ui/js/refine/`).

Raw AI response:
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/api/get_analysis_packages_with_metrics.php",
    "/axialy-production-ui/var/www/html/axialy-ui/js/refine/fetch_analysis_package_focus_area_records.php",
    "/axialy-production-ui/var/www/html/axialy-ui/js/refine/config/refine-activities.json",
    "/axialy-production-ui/var/www/html/axialy-ui/js/refine/fetch_stakeholder_feedback.php",
    "/axialy-production-ui/var/www/html/axialy-ui/js/refine/process_delete_focus_area_data.php"
  ],
  "purpose": "The `api.js` file serves as a centralized JavaScript module (using the revealing module pattern) that encapsulates all network communication for the 'refine' feature set. It acts as an abstraction layer between the frontend UI and various backend PHP endpoints and configuration files, handling data fetching for analysis packages, focus-area records, stakeholder feedback, and activity configuration, as well as managing the deletion of focus-area data. Note: The paths for the referenced files are inferred relative to the directory of the current file (`/axialy-production-ui/var/www/html/axialy-ui/js/refine/`)."
}

-------------------------------------------------
File #125
Path: /axialy-production-ui/var/www/html/axialy-ui/js/refine/augment-focus-area.js

Referenced files:
  - fetch_analysis_package_focus_area_records.php
  - save_revised_records.php

Purpose:
The `FocusAreaAugmentationModule` facilitates an AI-driven workflow for adding new records to a specific 'Focus Area' within an analysis package. 

Key functional steps include:
1. Collecting user instructions via a UI overlay.
2. Fetching existing records from `fetch_analysis_package_focus_area_records.php` to provide context for the AI.
3. Sending the existing data and user prompt to an external AI helper endpoint (configured via `window.AxiaBAConfig.api_base_url` + `/ai_helper.php`).
4. Rendering an interactive overlay that allows users to review and manually edit the AI-generated content.
5. Merging the new records with existing data and committing the changes to the system via `save_revised_records.php`.

The module relies on an external `RefineUtilsModule` for UI feedback (spinners) and assumes global configuration variables (`AxiaBAConfig`) are available in the browser environment.

Raw AI response:
```json
{
  "referenced_files": [
    "fetch_analysis_package_focus_area_records.php",
    "save_revised_records.php"
  ],
  "purpose": "The `FocusAreaAugmentationModule` facilitates an AI-driven workflow for adding new records to a specific 'Focus Area' within an analysis package. \n\nKey functional steps include:\n1. Collecting user instructions via a UI overlay.\n2. Fetching existing records from `fetch_analysis_package_focus_area_records.php` to provide context for the AI.\n3. Sending the existing data and user prompt to an external AI helper endpoint (configured via `window.AxiaBAConfig.api_base_url` + `/ai_helper.php`).\n4. Rendering an interactive overlay that allows users to review and manually edit the AI-generated content.\n5. Merging the new records with existing data and committing the changes to the system via `save_revised_records.php`.\n\nThe module relies on an external `RefineUtilsModule` for UI feedback (spinners) and assumes global configuration variables (`AxiaBAConfig`) are available in the browser environment."
}
```

-------------------------------------------------
File #126
Path: /axialy-production-ui/var/www/html/axialy-ui/js/refine/axialyAssessmentModule.js

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/api/get_analysis_packages_with_metrics.php
  - https://api.axiaba.com/axialy_analysis_package_assessor.php

Purpose:
The purpose of `axialyAssessmentModule.js` is to manage an interactive 'Axialy Assessment' overlay interface. It facilitates the retrieval of analysis package metrics from the backend, sends them to an external AI-based assessment API (axiaba.com), and renders the resulting analysis in a user-friendly UI. The module implements 'enhanced' interaction patterns, such as tile-based package selection, visual feedback, and modal navigation, ensuring parity with the existing `AxialyPackageAdvisorModule`. It relies on global objects like `RefineStateModule`, `RefineUtilsModule`, and `window.AxiaBAConfig` to function within the broader application lifecycle.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/api/get_analysis_packages_with_metrics.php",
    "https://api.axiaba.com/axialy_analysis_package_assessor.php"
  ],
  "purpose": "The purpose of `axialyAssessmentModule.js` is to manage an interactive 'Axialy Assessment' overlay interface. It facilitates the retrieval of analysis package metrics from the backend, sends them to an external AI-based assessment API (axiaba.com), and renders the resulting analysis in a user-friendly UI. The module implements 'enhanced' interaction patterns, such as tile-based package selection, visual feedback, and modal navigation, ensuring parity with the existing `AxialyPackageAdvisorModule`. It relies on global objects like `RefineStateModule`, `RefineUtilsModule`, and `window.AxiaBAConfig` to function within the broader application lifecycle."
}
```

-------------------------------------------------
File #127
Path: /axialy-production-ui/var/www/html/axialy-ui/js/refine/axialyPackageAdvisorModule.js

Referenced files:
  - fetch_analysis_package_focus_areas_with_metrics.php
  - https://api.axiaba.com/axialy_analysis_package_advisor.php

Purpose:
The `axialyPackageAdvisorModule.js` file implements the frontend logic for the "Axialy Advisor," an AI-driven analysis tool for individual software packages. It serves as an orchestrator that: 1) Fetches comprehensive package data (including metrics and focus areas) via an internal PHP script; 2) Transmits that data, along with optional user context, to an external API endpoint for analysis; and 3) Dynamically renders the resulting actionable advisements in an overlay UI. It also provides interactive features for users to act on these suggestions, such as navigating to specific focus areas, triggering automated feedback requests, or initiating content creation/enhancement workflows by integrating with other modules like `RefineActionsModule` and `NewFocusAreaCreationModule`.

Raw AI response:
```json
{
  "referenced_files": [
    "fetch_analysis_package_focus_areas_with_metrics.php",
    "https://api.axiaba.com/axialy_analysis_package_advisor.php"
  ],
  "purpose": "The `axialyPackageAdvisorModule.js` file implements the frontend logic for the \"Axialy Advisor,\" an AI-driven analysis tool for individual software packages. It serves as an orchestrator that: 1) Fetches comprehensive package data (including metrics and focus areas) via an internal PHP script; 2) Transmits that data, along with optional user context, to an external API endpoint for analysis; and 3) Dynamically renders the resulting actionable advisements in an overlay UI. It also provides interactive features for users to act on these suggestions, such as navigating to specific focus areas, triggering automated feedback requests, or initiating content creation/enhancement workflows by integrating with other modules like `RefineActionsModule` and `NewFocusAreaCreationModule`."
}
```

-------------------------------------------------
File #128
Path: /axialy-production-ui/var/www/html/axialy-ui/js/refine/edit-record-overlay.js

Referenced files:
  - /aii_helper.php

Purpose:
The primary purpose of this file is to provide a client-side UI overlay for editing 'focus-area' records within the Axialy system. It manages the distinction between system-level 'ephemeral' fields (such as deletion status and IDs) and user-editable properties stored within an 'axia_properties' object. The module handles UI rendering, state synchronization, input validation (via DOM manipulation), and integrates with an external AI service endpoint (via 'aii_helper.php') to allow users to enhance record data based on natural language instructions. It also tracks changed fields and provides functionality for resetting, deleting, or saving records.

Raw AI response:
```json
{
  "referenced_files": [
    "/aii_helper.php"
  ],
  "purpose": "The primary purpose of this file is to provide a client-side UI overlay for editing 'focus-area' records within the Axialy system. It manages the distinction between system-level 'ephemeral' fields (such as deletion status and IDs) and user-editable properties stored within an 'axia_properties' object. The module handles UI rendering, state synchronization, input validation (via DOM manipulation), and integrates with an external AI service endpoint (via 'aii_helper.php') to allow users to enhance record data based on natural language instructions. It also tracks changed fields and provides functionality for resetting, deleting, or saving records."
}
```

-------------------------------------------------
File #129
Path: /axialy-production-ui/var/www/html/axialy-ui/js/refine/events.js

Referenced files:
  - /config/package-actions.json
  - remove_analysis_package.php
  - recover_analysis_package.php
  - update_analysis_package.php

Purpose:
The `RefineEventsModule` serves as the primary controller for user interaction within the analysis refinement UI. Its main responsibilities include: 

1. Initializing event listeners for searching, package selection, and triggering actions via dropdown menus.
2. Managing the state of 'deleted' packages and the visibility of package action menus.
3. Handling lifecycle actions for analysis packages, including selection, deselection, removal, recovery, and header metadata updates.
4. Acting as a bridge between the user interface and backend services (via `fetch` requests) and other modular components such as `RefineApiModule`, `RefineStateModule`, `RefineUIModule`, and `RefineUtilsModule`. 

Note: The file depends on several global modules (`RefineStateModule`, `RefineUtilsModule`, `RefineApiModule`, `RefineUIModule`, `RefineActionsModule`, `OverlayModule`, etc.) which are not provided in the current context but are expected to be available in the global scope.

Raw AI response:
```json
{
  "referenced_files": [
    "/config/package-actions.json",
    "remove_analysis_package.php",
    "recover_analysis_package.php",
    "update_analysis_package.php"
  ],
  "purpose": "The `RefineEventsModule` serves as the primary controller for user interaction within the analysis refinement UI. Its main responsibilities include: \n\n1. Initializing event listeners for searching, package selection, and triggering actions via dropdown menus.\n2. Managing the state of 'deleted' packages and the visibility of package action menus.\n3. Handling lifecycle actions for analysis packages, including selection, deselection, removal, recovery, and header metadata updates.\n4. Acting as a bridge between the user interface and backend services (via `fetch` requests) and other modular components such as `RefineApiModule`, `RefineStateModule`, `RefineUIModule`, and `RefineUtilsModule`. \n\nNote: The file depends on several global modules (`RefineStateModule`, `RefineUtilsModule`, `RefineApiModule`, `RefineUIModule`, `RefineActionsModule`, `OverlayModule`, etc.) which are not provided in the current context but are expected to be available in the global scope."
}
```

-------------------------------------------------
File #130
Path: /axialy-production-ui/var/www/html/axialy-ui/js/refine/index.js

Referenced files:
  - RefineApiModule (implicit: likely /js/refine/api.js)
  - RefineStateModule (implicit: likely /js/refine/state.js)
  - RefineEventsModule (implicit: likely /js/refine/events.js)
  - AxialyAssessmentModule (global)
  - DynamicRibbonsModule (global)
  - AxialyPackageAdvisorModule (global)
  - RefineUtilsModule (global)
  - layout.js (referenced in code comments)

Purpose:
The RefineIndexModule acts as the primary controller for the 'Refine' tab in the application. It initializes the feature set by coordinating data fetching (via API and State modules), setting up event listeners, and configuring UI components such as ribbons and package overlays. It provides a central interface for reloading the view, managing user-driven focus area expansions, and ensuring that UI elements are correctly synchronized after state changes (such as saving a package).

Raw AI response:
```json
{
  "referenced_files": [
    "RefineApiModule (implicit: likely /js/refine/api.js)",
    "RefineStateModule (implicit: likely /js/refine/state.js)",
    "RefineEventsModule (implicit: likely /js/refine/events.js)",
    "AxialyAssessmentModule (global)",
    "DynamicRibbonsModule (global)",
    "AxialyPackageAdvisorModule (global)",
    "RefineUtilsModule (global)",
    "layout.js (referenced in code comments)"
  ],
  "purpose": "The RefineIndexModule acts as the primary controller for the 'Refine' tab in the application. It initializes the feature set by coordinating data fetching (via API and State modules), setting up event listeners, and configuring UI components such as ribbons and package overlays. It provides a central interface for reloading the view, managing user-driven focus area expansions, and ensuring that UI elements are correctly synchronized after state changes (such as saving a package)."
}
```

-------------------------------------------------
File #131
Path: /axialy-production-ui/var/www/html/axialy-ui/js/refine/new-record-overlay.js

Referenced files:
  - /aii_helper.php

Purpose:
The file implements a UI module (`NewRecordOverlayModule`) responsible for rendering a browser-based overlay used to create new 'focus-area' records. It manages the state of input fields, provides functionality to reset or toggle the deletion status of a record, and facilitates AI-driven data enhancement by communicating with the `/aii_helper.php` endpoint via the Fetch API. The module uses global configuration objects (`window.AxiaBAConfig`) to authenticate and route API requests and updates the DOM dynamically to reflect both user input and AI-suggested property revisions.

Raw AI response:
```json
{
  "referenced_files": [
    "/aii_helper.php"
  ],
  "purpose": "The file implements a UI module (`NewRecordOverlayModule`) responsible for rendering a browser-based overlay used to create new 'focus-area' records. It manages the state of input fields, provides functionality to reset or toggle the deletion status of a record, and facilitates AI-driven data enhancement by communicating with the `/aii_helper.php` endpoint via the Fetch API. The module uses global configuration objects (`window.AxiaBAConfig`) to authenticate and route API requests and updates the DOM dynamically to reflect both user input and AI-suggested property revisions."
}
```

-------------------------------------------------
File #132
Path: /axialy-production-ui/var/www/html/axialy-ui/js/refine/README.md

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/js/refine/actions.js
  - /axialy-production-ui/var/www/html/axialy-ui/js/refine/api.js
  - /axialy-production-ui/var/www/html/axialy-ui/js/refine/augment-focus-area.js
  - /axialy-production-ui/var/www/html/axialy-ui/js/refine/axialyAssessmentModule.js
  - /axialy-production-ui/var/www/html/axialy-ui/js/refine/axialyPackageAdvisorModule.js
  - /axialy-production-ui/var/www/html/axialy-ui/js/refine/edit-record-overlay.js
  - /axialy-production-ui/var/www/html/axialy-ui/js/refine/events.js
  - /axialy-production-ui/var/www/html/axialy-ui/js/refine/index.js
  - /axialy-production-ui/var/www/html/axialy-ui/js/refine/new-record-overlay.js
  - /axialy-production-ui/var/www/html/axialy-ui/js/refine/recover-focus-area.js
  - /axialy-production-ui/var/www/html/axialy-ui/js/refine/state.js
  - /axialy-production-ui/var/www/html/axialy-ui/js/refine/ui.js
  - /axialy-production-ui/var/www/html/axialy-ui/js/refine/utils.js
  - /api/get_analysis_packages_with_metrics.php
  - config/refine-activities.json
  - save_revised_records.php
  - axialy_analysis_package_assessor.php
  - axialy_analysis_package_advisor.php
  - fetch_past_versions.php
  - process_recover_focus_area.php

Purpose:
This README file serves as the documentation for the 'Refine' tab module. Its primary purpose is to outline the architectural components, module responsibilities, and key API/backend interactions for the user interface responsible for reviewing, editing, and refining AI-generated focus-area records within the Axialy system. It acts as a structural reference for developers maintaining the frontend logic, state management, and the interaction flow between the UI and various backend processing scripts.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/js/refine/actions.js",
    "/axialy-production-ui/var/www/html/axialy-ui/js/refine/api.js",
    "/axialy-production-ui/var/www/html/axialy-ui/js/refine/augment-focus-area.js",
    "/axialy-production-ui/var/www/html/axialy-ui/js/refine/axialyAssessmentModule.js",
    "/axialy-production-ui/var/www/html/axialy-ui/js/refine/axialyPackageAdvisorModule.js",
    "/axialy-production-ui/var/www/html/axialy-ui/js/refine/edit-record-overlay.js",
    "/axialy-production-ui/var/www/html/axialy-ui/js/refine/events.js",
    "/axialy-production-ui/var/www/html/axialy-ui/js/refine/index.js",
    "/axialy-production-ui/var/www/html/axialy-ui/js/refine/new-record-overlay.js",
    "/axialy-production-ui/var/www/html/axialy-ui/js/refine/recover-focus-area.js",
    "/axialy-production-ui/var/www/html/axialy-ui/js/refine/state.js",
    "/axialy-production-ui/var/www/html/axialy-ui/js/refine/ui.js",
    "/axialy-production-ui/var/www/html/axialy-ui/js/refine/utils.js",
    "/api/get_analysis_packages_with_metrics.php",
    "config/refine-activities.json",
    "save_revised_records.php",
    "axialy_analysis_package_assessor.php",
    "axialy_analysis_package_advisor.php",
    "fetch_past_versions.php",
    "process_recover_focus_area.php"
  ],
  "purpose": "This README file serves as the documentation for the 'Refine' tab module. Its primary purpose is to outline the architectural components, module responsibilities, and key API/backend interactions for the user interface responsible for reviewing, editing, and refining AI-generated focus-area records within the Axialy system. It acts as a structural reference for developers maintaining the frontend logic, state management, and the interaction flow between the UI and various backend processing scripts."
}
```

-------------------------------------------------
File #133
Path: /axialy-production-ui/var/www/html/axialy-ui/js/refine/recover-focus-area.js

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/js/refine/fetch_past_versions.php
  - /axialy-production-ui/var/www/html/axialy-ui/js/refine/process_recover_focus_area.php

Purpose:
This JavaScript module provides a client-side interface for managing and restoring historical versions of 'Focus Areas' within the Axialy UI. It creates a modal overlay that fetches a list of past versions via an API call, displays them to the user with metadata (such as revision summaries and timestamps), and provides a mechanism to restore a selected version by sending a POST request to a backend processing script. Upon successful restoration, it attempts to refresh the specific UI component (using the global `reloadRefineTabAndOpenPackage` function) or performs a full page reload to reflect the changes.

Raw AI response:
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/js/refine/fetch_past_versions.php",
    "/axialy-production-ui/var/www/html/axialy-ui/js/refine/process_recover_focus_area.php"
  ],
  "purpose": "This JavaScript module provides a client-side interface for managing and restoring historical versions of 'Focus Areas' within the Axialy UI. It creates a modal overlay that fetches a list of past versions via an API call, displays them to the user with metadata (such as revision summaries and timestamps), and provides a mechanism to restore a selected version by sending a POST request to a backend processing script. Upon successful restoration, it attempts to refresh the specific UI component (using the global `reloadRefineTabAndOpenPackage` function) or performs a full page reload to reflect the changes."
}

-------------------------------------------------
File #134
Path: /axialy-production-ui/var/www/html/axialy-ui/js/refine/state.js

Referenced files:
  (none)

Purpose:
The file implements a JavaScript module using the revealing module pattern to serve as a centralized state manager for the 'refine' feature of the Axialy UI. It provides getter and setter methods to track application-level data, including the currently selected package (ID and name), version, associated stakeholders, and active refinement activities. By encapsulating this state in an IIFE (Immediately Invoked Function Expression), it ensures the data remains private and provides a clean, controlled API for other UI components to read and update the application state during the refinement process.

Raw AI response:
{
  "referenced_files": [],
  "purpose": "The file implements a JavaScript module using the revealing module pattern to serve as a centralized state manager for the 'refine' feature of the Axialy UI. It provides getter and setter methods to track application-level data, including the currently selected package (ID and name), version, associated stakeholders, and active refinement activities. By encapsulating this state in an IIFE (Immediately Invoked Function Expression), it ensures the data remains private and provides a clean, controlled API for other UI components to read and update the application state during the refinement process."
}

-------------------------------------------------
File #135
Path: /axialy-production-ui/var/www/html/axialy-ui/js/refine/ui.js

Referenced files:
  - /serve_logo.php
  - save_revised_records.php
  - fetch_stakeholder_feedback.php

Purpose:
The `ui.js` file serves as the core JavaScript controller for the 'Refine' tab UI in the Axialy system. It manages the dynamic rendering of package summaries and focus-area records, facilitates client-side interaction (such as editing records, adding new records, and toggling UI sections), and handles data persistence by communicating with server-side endpoints. Key responsibilities include managing UI state (like distinguishing ephemeral vs. user-defined fields), coordinating with external modules (like `EditRecordOverlayModule`, `NewRecordOverlayModule`, and `RefineEventsModule`), and ensuring that data payloads for saving updates correctly account for record status (new, modified, or soft-deleted).

Raw AI response:
{
  "referenced_files": [
    "/serve_logo.php",
    "save_revised_records.php",
    "fetch_stakeholder_feedback.php"
  ],
  "purpose": "The `ui.js` file serves as the core JavaScript controller for the 'Refine' tab UI in the Axialy system. It manages the dynamic rendering of package summaries and focus-area records, facilitates client-side interaction (such as editing records, adding new records, and toggling UI sections), and handles data persistence by communicating with server-side endpoints. Key responsibilities include managing UI state (like distinguishing ephemeral vs. user-defined fields), coordinating with external modules (like `EditRecordOverlayModule`, `NewRecordOverlayModule`, and `RefineEventsModule`), and ensuring that data payloads for saving updates correctly account for record status (new, modified, or soft-deleted)."
}

-------------------------------------------------
File #136
Path: /axialy-production-ui/var/www/html/axialy-ui/js/refine/utils.js

Referenced files:
  (none)

Purpose:
The file serves as a utility module for the 'refine' feature set within the Axialy UI. It provides reusable helper functions, specifically a debounce implementation for performance optimization, UI manipulation methods for displaying and hiding full-page loading masks (spinners), and a cleanup function to remove existing refine-related dropdown elements from the DOM.

Raw AI response:
```json
{
  "referenced_files": [],
  "purpose": "The file serves as a utility module for the 'refine' feature set within the Axialy UI. It provides reusable helper functions, specifically a debounce implementation for performance optimization, UI manipulation methods for displaying and hiding full-page loading masks (spinners), and a cleanup function to remove existing refine-related dropdown elements from the DOM."
}
```

-------------------------------------------------
File #137
Path: /axialy-production-ui/var/www/html/axialy-ui/js/settings/api.js

Referenced files:
  - /get_custom_organizations.php
  - /get_focus_organization.php
  - /update_focus_organization.php
  - /create_custom_organization.php
  - /update_custom_organization.php

Purpose:
The `SettingsAPIModule` acts as an asynchronous client-side API layer for managing organization settings within the UI. It provides functions to fetch, create, and update custom organizations, as well as manage the user's currently active ('focus') organization by communicating with PHP backend endpoints.

Raw AI response:
```json
{
  "referenced_files": [
    "/get_custom_organizations.php",
    "/get_focus_organization.php",
    "/update_focus_organization.php",
    "/create_custom_organization.php",
    "/update_custom_organization.php"
  ],
  "purpose": "The `SettingsAPIModule` acts as an asynchronous client-side API layer for managing organization settings within the UI. It provides functions to fetch, create, and update custom organizations, as well as manage the user's currently active ('focus') organization by communicating with PHP backend endpoints."
}
```

-------------------------------------------------
File #138
Path: /axialy-production-ui/var/www/html/axialy-ui/js/settings/events.js

Referenced files:
  (none)

Purpose:
The `SettingsEventsModule` is responsible for initializing and managing all event-driven interactions within the Settings tab of the application. It acts as a bridge between the DOM (user inputs and forms) and the supporting modules (`SettingsAPIModule`, `SettingsStateModule`, and `SettingsUIModule`). Its primary functions include: 1) Handling changes to the focus organization selection; 2) Managing form validation for creating and editing organizations (including real-time validation feedback for name inputs); 3) Controlling UI interactions such as toggling edit forms and submitting updates; and 4) Coordinating the flow of data between the UI, local state, and the server API. Note: This file relies on several global modules (`SettingsAPIModule`, `SettingsStateModule`, `SettingsUIModule`) which are implied to exist in the execution environment but are not explicitly defined or imported in this file.

Raw AI response:
```json
{
  "referenced_files": [],
  "purpose": "The `SettingsEventsModule` is responsible for initializing and managing all event-driven interactions within the Settings tab of the application. It acts as a bridge between the DOM (user inputs and forms) and the supporting modules (`SettingsAPIModule`, `SettingsStateModule`, and `SettingsUIModule`). Its primary functions include: 1) Handling changes to the focus organization selection; 2) Managing form validation for creating and editing organizations (including real-time validation feedback for name inputs); 3) Controlling UI interactions such as toggling edit forms and submitting updates; and 4) Coordinating the flow of data between the UI, local state, and the server API. Note: This file relies on several global modules (`SettingsAPIModule`, `SettingsStateModule`, `SettingsUIModule`) which are implied to exist in the execution environment but are not explicitly defined or imported in this file."
}
```

-------------------------------------------------
File #139
Path: /axialy-production-ui/var/www/html/axialy-ui/js/settings/index.js

Referenced files:
  - SettingsStateModule
  - SettingsAPIModule
  - SettingsUIModule
  - SettingsEventsModule

Purpose:
The `SettingsIndexModule` serves as the primary controller for the 'Settings' tab in the Axialy UI. Its functional purpose is to orchestrate the initialization process: fetching organizational data, updating the application state, rendering UI components, setting up event listeners, and enhancing form interactions (such as character counters, image previews, and real-time field validation). The code relies on several global modules (`SettingsStateModule`, `SettingsAPIModule`, `SettingsUIModule`, `SettingsEventsModule`) which are presumed to be loaded elsewhere in the execution context, as they are not defined within this file.

Raw AI response:
{
  "referenced_files": [
    "SettingsStateModule",
    "SettingsAPIModule",
    "SettingsUIModule",
    "SettingsEventsModule"
  ],
  "purpose": "The `SettingsIndexModule` serves as the primary controller for the 'Settings' tab in the Axialy UI. Its functional purpose is to orchestrate the initialization process: fetching organizational data, updating the application state, rendering UI components, setting up event listeners, and enhancing form interactions (such as character counters, image previews, and real-time field validation). The code relies on several global modules (`SettingsStateModule`, `SettingsAPIModule`, `SettingsUIModule`, `SettingsEventsModule`) which are presumed to be loaded elsewhere in the execution context, as they are not defined within this file.",
  "caveats": "The file references several external modules that are not provided in the context. While the functionality is clear, the implementation depends on the existence of these modules in the global scope."
}

-------------------------------------------------
File #140
Path: /axialy-production-ui/var/www/html/axialy-ui/js/settings/README.md

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/js/settings/api.js
  - /axialy-production-ui/var/www/html/axialy-ui/js/settings/events.js
  - /axialy-production-ui/var/www/html/axialy-ui/js/settings/index.js
  - /axialy-production-ui/var/www/html/axialy-ui/js/settings/state.js
  - /axialy-production-ui/var/www/html/axialy-ui/js/settings/ui.js
  - /axialy-production-ui/var/www/html/axialy-ui/js/settings/utils.js
  - /get_custom_organizations.php
  - /get_focus_organization.php
  - /update_focus_organization.php
  - /create_custom_organization.php
  - /update_custom_organization.php

Purpose:
This README file serves as architectural documentation for the 'Settings' module within the Axialy UI. It outlines the structure and responsibilities of the JavaScript components used to manage custom organizations and the active focus organization. It details how the frontend modules (state, API, UI, events, and utilities) interact with each other and identifies the specific backend PHP endpoints consumed by the API module.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/js/settings/api.js",
    "/axialy-production-ui/var/www/html/axialy-ui/js/settings/events.js",
    "/axialy-production-ui/var/www/html/axialy-ui/js/settings/index.js",
    "/axialy-production-ui/var/www/html/axialy-ui/js/settings/state.js",
    "/axialy-production-ui/var/www/html/axialy-ui/js/settings/ui.js",
    "/axialy-production-ui/var/www/html/axialy-ui/js/settings/utils.js",
    "/get_custom_organizations.php",
    "/get_focus_organization.php",
    "/update_focus_organization.php",
    "/create_custom_organization.php",
    "/update_custom_organization.php"
  ],
  "purpose": "This README file serves as architectural documentation for the 'Settings' module within the Axialy UI. It outlines the structure and responsibilities of the JavaScript components used to manage custom organizations and the active focus organization. It details how the frontend modules (state, API, UI, events, and utilities) interact with each other and identifies the specific backend PHP endpoints consumed by the API module."
}
```

-------------------------------------------------
File #141
Path: /axialy-production-ui/var/www/html/axialy-ui/js/settings/state.js

Referenced files:
  (none)

Purpose:
This file implements a self-contained JavaScript module using the revealing module pattern to manage the application's global or session-specific state related to 'settings', specifically handling the current organization focus and a list of custom organizations. It acts as a singleton data store to maintain and provide access to these variables across the frontend UI, ensuring they are encapsulated and accessible via getter and setter methods.

Raw AI response:
```json
{
  "referenced_files": [],
  "purpose": "This file implements a self-contained JavaScript module using the revealing module pattern to manage the application's global or session-specific state related to 'settings', specifically handling the current organization focus and a list of custom organizations. It acts as a singleton data store to maintain and provide access to these variables across the frontend UI, ensuring they are encapsulated and accessible via getter and setter methods."
}
```

-------------------------------------------------
File #142
Path: /axialy-production-ui/var/www/html/axialy-ui/js/settings/ui.js

Referenced files:
  - /serve_logo.php

Purpose:
The `SettingsUIModule` serves as the frontend controller for managing the user interface within the organization settings area. Its primary responsibilities include DOM manipulation for dynamic elements such as the organization list cards, form validation for creating and editing organizations, managing loading states/overlays, and handling toast notifications. It acts as a bridge between the raw data (managed by `SettingsStateModule`, which is referenced but not provided) and the rendered HTML, incorporating security measures by utilizing `SettingsUtilsModule` (referenced) for input sanitization.

Raw AI response:
{
  "referenced_files": [
    "/serve_logo.php"
  ],
  "purpose": "The `SettingsUIModule` serves as the frontend controller for managing the user interface within the organization settings area. Its primary responsibilities include DOM manipulation for dynamic elements such as the organization list cards, form validation for creating and editing organizations, managing loading states/overlays, and handling toast notifications. It acts as a bridge between the raw data (managed by `SettingsStateModule`, which is referenced but not provided) and the rendered HTML, incorporating security measures by utilizing `SettingsUtilsModule` (referenced) for input sanitization."
}

-------------------------------------------------
File #143
Path: /axialy-production-ui/var/www/html/axialy-ui/js/settings/utils.js

Referenced files:
  (none)

Purpose:
The `utils.js` file serves as a utility module for the settings interface of the Axialy UI. It provides two primary helper functions: `sanitizeHTML`, which prevents XSS by encoding strings, and `createToast`, which generates Bootstrap-compatible notification DOM elements. The module uses the revealing module pattern to expose these functions to the rest of the application.

Raw AI response:
{
  "referenced_files": [],
  "purpose": "The `utils.js` file serves as a utility module for the settings interface of the Axialy UI. It provides two primary helper functions: `sanitizeHTML`, which prevents XSS by encoding strings, and `createToast`, which generates Bootstrap-compatible notification DOM elements. The module uses the revealing module pattern to expose these functions to the rest of the application."
}

-------------------------------------------------
File #144
Path: /axialy-production-ui/var/www/html/axialy-ui/js/survey/api.js

Referenced files:
  - get_dashboard_custom_organizations.php
  - get_dashboard_stakeholder_emails.php
  - get_dashboard_analysis_packages.php
  - get_dashboard_focus_areas.php
  - get_survey_stakeholder_feedback_requests.php

Purpose:
The file provides a JavaScript module ('SurveyAPIModule') that acts as an abstraction layer for making asynchronous HTTP requests to various backend PHP endpoints. Its purpose is to centralize data fetching logic for the 'Survey' tab in the UI, ensuring that data (such as stakeholder information, analysis packages, and feedback requests) is retrieved consistently and errors are handled and logged uniformly. The file uses relative paths for all fetch calls, indicating it expects these PHP scripts to be co-located or accessible via the same base route as the UI entry point.

Raw AI response:
```json
{
  "referenced_files": [
    "get_dashboard_custom_organizations.php",
    "get_dashboard_stakeholder_emails.php",
    "get_dashboard_analysis_packages.php",
    "get_dashboard_focus_areas.php",
    "get_survey_stakeholder_feedback_requests.php"
  ],
  "purpose": "The file provides a JavaScript module ('SurveyAPIModule') that acts as an abstraction layer for making asynchronous HTTP requests to various backend PHP endpoints. Its purpose is to centralize data fetching logic for the 'Survey' tab in the UI, ensuring that data (such as stakeholder information, analysis packages, and feedback requests) is retrieved consistently and errors are handled and logged uniformly. The file uses relative paths for all fetch calls, indicating it expects these PHP scripts to be co-located or accessible via the same base route as the UI entry point."
}
```

-------------------------------------------------
File #145
Path: /axialy-production-ui/var/www/html/axialy-ui/js/survey/events.js

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/js/survey/state.js
  - /axialy-production-ui/var/www/html/axialy-ui/js/survey/api.js
  - /axialy-production-ui/var/www/html/axialy-ui/js/survey/ui.js

Purpose:
The `SurveyEventsModule` acts as the primary event orchestration layer for the Survey interface. Its purpose is to register and manage DOM event listeners (such as form submissions, filter resets, pagination clicks, and action button interactions) and coordinate the data flow between the API, the application state, and the UI. It relies on `SurveyStateModule` for managing current application state, `SurveyAPIModule` for network requests, and `SurveyUIModule` for rendering updates. Note that while these dependencies are not explicitly imported, they are referenced globally throughout the code.

Raw AI response:
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/js/survey/state.js",
    "/axialy-production-ui/var/www/html/axialy-ui/js/survey/api.js",
    "/axialy-production-ui/var/www/html/axialy-ui/js/survey/ui.js"
  ],
  "purpose": "The `SurveyEventsModule` acts as the primary event orchestration layer for the Survey interface. Its purpose is to register and manage DOM event listeners (such as form submissions, filter resets, pagination clicks, and action button interactions) and coordinate the data flow between the API, the application state, and the UI. It relies on `SurveyStateModule` for managing current application state, `SurveyAPIModule` for network requests, and `SurveyUIModule` for rendering updates. Note that while these dependencies are not explicitly imported, they are referenced globally throughout the code.",
  "caveats": "The file references `SurveyStateModule`, `SurveyAPIModule`, and `SurveyUIModule`. The actual file paths for these modules are not provided in the context, so they were inferred based on typical project structure for this directory."
}

-------------------------------------------------
File #146
Path: /axialy-production-ui/var/www/html/axialy-ui/js/survey/index.js

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/js/survey/state.js
  - /axialy-production-ui/var/www/html/axialy-ui/js/survey/events.js
  - /axialy-production-ui/var/www/html/axialy-ui/js/survey/ui.js

Purpose:
The `SurveyIndexModule` serves as the primary entry point and orchestrator for the survey functionality within the Axialy UI. Its functional purpose is to manage the lifecycle of the Survey tab, specifically handling the asynchronous initialization process. It delegates task execution to three inferred companion modules: 'SurveyStateModule' (for tracking initialization status), 'SurveyEventsModule' (for loading data and registering event listeners), and 'SurveyUIModule' (for providing user feedback via toasts in case of errors). Note: The referenced modules are not defined in this file, implying they exist as global objects or are loaded via other scripts in the application's dependency chain.

Raw AI response:
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/js/survey/state.js",
    "/axialy-production-ui/var/www/html/axialy-ui/js/survey/events.js",
    "/axialy-production-ui/var/www/html/axialy-ui/js/survey/ui.js"
  ],
  "purpose": "The `SurveyIndexModule` serves as the primary entry point and orchestrator for the survey functionality within the Axialy UI. Its functional purpose is to manage the lifecycle of the Survey tab, specifically handling the asynchronous initialization process. It delegates task execution to three inferred companion modules: 'SurveyStateModule' (for tracking initialization status), 'SurveyEventsModule' (for loading data and registering event listeners), and 'SurveyUIModule' (for providing user feedback via toasts in case of errors). Note: The referenced modules are not defined in this file, implying they exist as global objects or are loaded via other scripts in the application's dependency chain."
}

-------------------------------------------------
File #147
Path: /axialy-production-ui/var/www/html/axialy-ui/js/survey/modals.js

Referenced files:
  - fetch_survey_feedback_details.php
  - send_stakeholder_reminder.php
  - cancel_stakeholder_feedback_request.php
  - download_content_review_form.php

Purpose:
This module acts as a UI controller for handling various stakeholder feedback-related modal windows. It manages the lifecycle of modals for viewing feedback details, sending reminders to stakeholders, and cancelling feedback requests. It performs data fetching via AJAX to populate these modals and includes utility functions for sanitation and PDF document generation. The module expects the global presence of 'SurveyUIModule' for notifications and 'SurveyEventsModule' for refreshing the view after successful actions.

Raw AI response:
```json
{
  "referenced_files": [
    "fetch_survey_feedback_details.php",
    "send_stakeholder_reminder.php",
    "cancel_stakeholder_feedback_request.php",
    "download_content_review_form.php"
  ],
  "purpose": "This module acts as a UI controller for handling various stakeholder feedback-related modal windows. It manages the lifecycle of modals for viewing feedback details, sending reminders to stakeholders, and cancelling feedback requests. It performs data fetching via AJAX to populate these modals and includes utility functions for sanitation and PDF document generation. The module expects the global presence of 'SurveyUIModule' for notifications and 'SurveyEventsModule' for refreshing the view after successful actions."
}
```

-------------------------------------------------
File #148
Path: /axialy-production-ui/var/www/html/axialy-ui/js/survey/state.js

Referenced files:
  (none)

Purpose:
The file implements a JavaScript module using the revealing module pattern to serve as a centralized, in-memory state manager for the survey functionality within the axialy-ui application. It maintains private variables for data collections (such as feedback requests, organizations, stakeholder emails, analysis packages, and focus areas) and pagination metadata. By exposing getter, setter, and reset functions, it allows other components of the application to access and synchronize the current state of survey-related data without directly mutating the internal state variables.

Raw AI response:
{
  "referenced_files": [],
  "purpose": "The file implements a JavaScript module using the revealing module pattern to serve as a centralized, in-memory state manager for the survey functionality within the axialy-ui application. It maintains private variables for data collections (such as feedback requests, organizations, stakeholder emails, analysis packages, and focus areas) and pagination metadata. By exposing getter, setter, and reset functions, it allows other components of the application to access and synchronize the current state of survey-related data without directly mutating the internal state variables."
}

-------------------------------------------------
File #149
Path: /axialy-production-ui/var/www/html/axialy-ui/js/survey/ui.js

Referenced files:
  - SurveyUtilsModule
  - SurveyModalsModule
  - SurveyCollateFeedbackModule

Purpose:
The `SurveyUIModule` is a JavaScript module responsible for managing the user interface layer of the survey feedback system. Its primary functions include populating filter dropdowns, dynamically rendering the 'survey-feedback-requests-table' with formatted data, handling client-side pagination, and triggering toast notifications. It also acts as an interface controller that delegates complex actions—such as viewing feedback, sending reminders, cancelling requests, and compiling feedback—to other specialized modules (SurveyModalsModule and SurveyCollateFeedbackModule) after verifying their availability in the global scope.

Raw AI response:
```json
{
  "referenced_files": [
    "SurveyUtilsModule",
    "SurveyModalsModule",
    "SurveyCollateFeedbackModule"
  ],
  "purpose": "The `SurveyUIModule` is a JavaScript module responsible for managing the user interface layer of the survey feedback system. Its primary functions include populating filter dropdowns, dynamically rendering the 'survey-feedback-requests-table' with formatted data, handling client-side pagination, and triggering toast notifications. It also acts as an interface controller that delegates complex actions—such as viewing feedback, sending reminders, cancelling requests, and compiling feedback—to other specialized modules (SurveyModalsModule and SurveyCollateFeedbackModule) after verifying their availability in the global scope.",
  "note": "The referenced dependencies (SurveyUtilsModule, SurveyModalsModule, SurveyCollateFeedbackModule) are accessed via the global `window` object or expected to be present in the execution environment; their physical file paths are not explicitly defined in the provided code snippet."
}
```

-------------------------------------------------
File #150
Path: /axialy-production-ui/var/www/html/axialy-ui/js/survey/utils.js

Referenced files:
  (none)

Purpose:
The file serves as a JavaScript utility module (SurveyUtilsModule) that provides shared helper functions for the survey and feedback management interface. It includes methods for XSS sanitization, dynamic creation of Bootstrap-compatible UI components (toasts and tooltips), and helper functions for formatting business-logic-specific data such as response counts, dates, and feedback type badges. Note that this file assumes the presence of external libraries like Bootstrap (e.g., 'bootstrap.Tooltip') in the global scope.

Raw AI response:
```json
{
  "referenced_files": [],
  "purpose": "The file serves as a JavaScript utility module (SurveyUtilsModule) that provides shared helper functions for the survey and feedback management interface. It includes methods for XSS sanitization, dynamic creation of Bootstrap-compatible UI components (toasts and tooltips), and helper functions for formatting business-logic-specific data such as response counts, dates, and feedback type badges. Note that this file assumes the presence of external libraries like Bootstrap (e.g., 'bootstrap.Tooltip') in the global scope."
}
```

-------------------------------------------------
File #151
Path: /axialy-production-ui/var/www/html/axialy-ui/js/account-actions.js

Referenced files:
  - assets/css/account-modal.css
  - /manage-subscription.php
  - /subscription.php

Purpose:
The primary purpose of `account-actions.js` is to manage the user interface for account management operations, specifically handling subscription-related actions. It dynamically fetches the account management content via an AJAX request to `/manage-subscription.php`, injects it into a modal overlay, and manages the lifecycle of that modal (opening, closing, and handling form submissions like subscription cancellations). The script also dynamically injects its own CSS dependencies and coordinates with a global `OverlayModule` for UI feedback.

Raw AI response:
{
  "referenced_files": [
    "assets/css/account-modal.css",
    "/manage-subscription.php",
    "/subscription.php"
  ],
  "purpose": "The primary purpose of `account-actions.js` is to manage the user interface for account management operations, specifically handling subscription-related actions. It dynamically fetches the account management content via an AJAX request to `/manage-subscription.php`, injects it into a modal overlay, and manages the lifecycle of that modal (opening, closing, and handling form submissions like subscription cancellations). The script also dynamically injects its own CSS dependencies and coordinates with a global `OverlayModule` for UI feedback."
}

-------------------------------------------------
File #152
Path: /axialy-production-ui/var/www/html/axialy-ui/js/analysis-package-header.js

Referenced files:
  - /get_organizations.php

Purpose:
The `analysis-package-header.js` module serves as a UI component for displaying and managing a modal overlay used to review and edit 'Analysis Package' metadata. It provides form functionality for capturing an organization selection, a package title, a short summary, and a detailed description. It handles the lifecycle of this dialog (creation, display, event handling, focus trapping for accessibility, and input validation) and interacts with the backend via a fetch request to `/get_organizations.php` to populate the organizational dropdown.

Raw AI response:
{
  "referenced_files": [
    "/get_organizations.php"
  ],
  "purpose": "The `analysis-package-header.js` module serves as a UI component for displaying and managing a modal overlay used to review and edit 'Analysis Package' metadata. It provides form functionality for capturing an organization selection, a package title, a short summary, and a detailed description. It handles the lifecycle of this dialog (creation, display, event handling, focus trapping for accessibility, and input validation) and interacts with the backend via a fetch request to `/get_organizations.php` to populate the organizational dropdown."
}

-------------------------------------------------
File #153
Path: /axialy-production-ui/var/www/html/axialy-ui/js/apply-revisions-handler.js

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/aii_helper.php
  - /axialy-production-ui/var/www/html/axialy-ui/save_revised_records.php

Purpose:
The file `/js/apply-revisions-handler.js` acts as a client-side orchestrator for the 'Revisions Summary' workflow. It manages the lifecycle of processing user-provided feedback (both itemized and general), sending that data to an AI helper script (`/aii_helper.php`) for analysis, and displaying the AI's recommendations in an interactive overlay. It also handles the final commitment of approved revisions back to the server via `/save_revised_records.php`. The handler includes context-aware navigation to ensure that after saving changes, the UI transitions back to the specific tab (Refine or Survey) from which the feedback process was initiated.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/aii_helper.php",
    "/axialy-production-ui/var/www/html/axialy-ui/save_revised_records.php"
  ],
  "purpose": "The file `/js/apply-revisions-handler.js` acts as a client-side orchestrator for the 'Revisions Summary' workflow. It manages the lifecycle of processing user-provided feedback (both itemized and general), sending that data to an AI helper script (`/aii_helper.php`) for analysis, and displaying the AI's recommendations in an interactive overlay. It also handles the final commitment of approved revisions back to the server via `/save_revised_records.php`. The handler includes context-aware navigation to ensure that after saving changes, the UI transitions back to the specific tab (Refine or Survey) from which the feedback process was initiated."
}
```

-------------------------------------------------
File #154
Path: /axialy-production-ui/var/www/html/axialy-ui/js/collate-feedback.js

Referenced files:
  - fetch_stakeholder_feedback.php
  - fetch_feedback_details.php

Purpose:
The `collate-feedback.js` file implements a client-side module responsible for aggregating and managing stakeholder feedback for specific project focus areas. It provides a UI overlay that allows users to review general and itemized feedback, assign actions (Apply, Add Instruction, or Ignore) to individual feedback responses, and persist these actions. Upon final submission, it interacts with an external `ApplyRevisionsHandler` (referenced globally) to process the collected revisions for the selected package and focus area.

Raw AI response:
{
  "referenced_files": [
    "fetch_stakeholder_feedback.php",
    "fetch_feedback_details.php"
  ],
  "purpose": "The `collate-feedback.js` file implements a client-side module responsible for aggregating and managing stakeholder feedback for specific project focus areas. It provides a UI overlay that allows users to review general and itemized feedback, assign actions (Apply, Add Instruction, or Ignore) to individual feedback responses, and persist these actions. Upon final submission, it interacts with an external `ApplyRevisionsHandler` (referenced globally) to process the collected revisions for the selected package and focus area."
}

-------------------------------------------------
File #155
Path: /axialy-production-ui/var/www/html/axialy-ui/js/content-review-overlay.js

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/config/refine-activities.json
  - /axialy-production-ui/var/www/html/axialy-ui/js/send_content_review_emails.php

Purpose:
The primary purpose of this file is to manage the 'Content Review' user interface flow within the application. It dynamically populates a set of action buttons (Activities) based on a configuration file, handles user interaction for these actions—specifically the 'Request Stakeholder Feedback' flow—and renders an overlay modal. This modal allows users to select stakeholders from a predefined list or add them manually, provide feedback, and trigger the email dispatch process via an AJAX call to the backend.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/config/refine-activities.json",
    "/axialy-production-ui/var/www/html/axialy-ui/js/send_content_review_emails.php"
  ],
  "purpose": "The primary purpose of this file is to manage the 'Content Review' user interface flow within the application. It dynamically populates a set of action buttons (Activities) based on a configuration file, handles user interaction for these actions—specifically the 'Request Stakeholder Feedback' flow—and renders an overlay modal. This modal allows users to select stakeholders from a predefined list or add them manually, provide feedback, and trigger the email dispatch process via an AJAX call to the backend."
}
```

-------------------------------------------------
File #156
Path: /axialy-production-ui/var/www/html/axialy-ui/js/content-review.js

Referenced files:
  - config/feedback-response-types.json
  - fetch_analysis_package_focus_area_records.php
  - /process_content_review_request.php

Purpose:
The `content-review.js` file implements a two-step client-side user interface (overlay system) for managing and submitting content review requests for specific focus areas within an analysis package. 

1. It first gathers request details such as stakeholder emails, a personal message, and feedback form configuration (general vs. itemized).
2. It then provides a preview interface where users can select or deselect individual records associated with the focus area version.
3. Finally, it transmits the final request data, including the selected record indices, to the server via `/process_content_review_request.php` for processing. 

It relies on external configuration data from `config/feedback-response-types.json` and fetches analytical record data from `fetch_analysis_package_focus_area_records.php` to populate the selection interface.

Raw AI response:
```json
{
  "referenced_files": [
    "config/feedback-response-types.json",
    "fetch_analysis_package_focus_area_records.php",
    "/process_content_review_request.php"
  ],
  "purpose": "The `content-review.js` file implements a two-step client-side user interface (overlay system) for managing and submitting content review requests for specific focus areas within an analysis package. \n\n1. It first gathers request details such as stakeholder emails, a personal message, and feedback form configuration (general vs. itemized).\n2. It then provides a preview interface where users can select or deselect individual records associated with the focus area version.\n3. Finally, it transmits the final request data, including the selected record indices, to the server via `/process_content_review_request.php` for processing. \n\nIt relies on external configuration data from `config/feedback-response-types.json` and fetches analytical record data from `fetch_analysis_package_focus_area_records.php` to populate the selection interface."
}
```

-------------------------------------------------
File #157
Path: /axialy-production-ui/var/www/html/axialy-ui/js/content-revision.js

Referenced files:
  - fetch_analysis_package_focus_area_records.php
  - process_content_revision.php

Purpose:
This file is a JavaScript module responsible for managing a "Content Revision" UI overlay. Its primary purpose is to allow users to view, edit, add, or soft-delete records associated with a specific focus area within an analysis package. It fetches existing data via AJAX, renders an interactive form dynamically, and submits changes back to the server to trigger the creation of a new version of the focus-area records. The module also handles UI lifecycle events, such as creating loading spinners and refreshing the application state upon a successful commit.

Raw AI response:
```json
{
  "referenced_files": [
    "fetch_analysis_package_focus_area_records.php",
    "process_content_revision.php"
  ],
  "purpose": "This file is a JavaScript module responsible for managing a \"Content Revision\" UI overlay. Its primary purpose is to allow users to view, edit, add, or soft-delete records associated with a specific focus area within an analysis package. It fetches existing data via AJAX, renders an interactive form dynamically, and submits changes back to the server to trigger the creation of a new version of the focus-area records. The module also handles UI lifecycle events, such as creating loading spinners and refreshing the application state upon a successful commit."
}
```

-------------------------------------------------
File #158
Path: /axialy-production-ui/var/www/html/axialy-ui/js/dynamic-ribbons.js

Referenced files:
  (none)

Purpose:
The `dynamic-ribbons.js` file implements a JavaScript module (`DynamicRibbonsModule`) designed to manage the display and manipulation of interactive data grid 'ribbons' within the user interface. It provides functionality to dynamically generate tables from input data (associated with `input_text_summaries`), allow users to toggle the visibility of these ribbons, add or delete rows, and edit cell contents in-place. Crucially, it tracks all rendered ribbons in an in-memory `ribbonsDataCollection` and provides a `collectRibbonsData` method to aggregate the current state of these grids for form submission or saving. The module relies on a global `ProcessFeedbackModule` (referenced via `ProcessFeedbackModule.updateSaveButtonState()`) to update the state of the UI save buttons when user edits occur.

Raw AI response:
```json
{
  "referenced_files": [],
  "purpose": "The `dynamic-ribbons.js` file implements a JavaScript module (`DynamicRibbonsModule`) designed to manage the display and manipulation of interactive data grid 'ribbons' within the user interface. It provides functionality to dynamically generate tables from input data (associated with `input_text_summaries`), allow users to toggle the visibility of these ribbons, add or delete rows, and edit cell contents in-place. Crucially, it tracks all rendered ribbons in an in-memory `ribbonsDataCollection` and provides a `collectRibbonsData` method to aggregate the current state of these grids for form submission or saving. The module relies on a global `ProcessFeedbackModule` (referenced via `ProcessFeedbackModule.updateSaveButtonState()`) to update the state of the UI save buttons when user edits occur."
}
```

-------------------------------------------------
File #159
Path: /axialy-production-ui/var/www/html/axialy-ui/js/enhance-content.js

Referenced files:
  - /aii_helper.php
  - /save_enhanced_records.php
  - /fetch_analysis_package_focus_area_records.php

Purpose:
The `enhance-content.js` file implements a client-side module responsible for the "Enhance Focus Area" workflow in the Axia system. Its primary purpose is to allow users to provide instructions to an AI to transform existing records within a specific focus area. The module handles the entire process: fetching current record data via `fetch_analysis_package_focus_area_records.php`, sending the data and user instructions to the AI through `aii_helper.php`, displaying the AI-generated revisions in an interactive review overlay, and finally committing the accepted changes to the system via `save_enhanced_records.php`. It also manages UI elements like loading spinners and conditional styling for created, updated, or deleted records.

Raw AI response:
{
  "referenced_files": [
    "/aii_helper.php",
    "/save_enhanced_records.php",
    "/fetch_analysis_package_focus_area_records.php"
  ],
  "purpose": "The `enhance-content.js` file implements a client-side module responsible for the \"Enhance Focus Area\" workflow in the Axia system. Its primary purpose is to allow users to provide instructions to an AI to transform existing records within a specific focus area. The module handles the entire process: fetching current record data via `fetch_analysis_package_focus_area_records.php`, sending the data and user instructions to the AI through `aii_helper.php`, displaying the AI-generated revisions in an interactive review overlay, and finally committing the accepted changes to the system via `save_enhanced_records.php`. It also manages UI elements like loading spinners and conditional styling for created, updated, or deleted records."
}

-------------------------------------------------
File #160
Path: /axialy-production-ui/var/www/html/axialy-ui/js/export-csv.js

Referenced files:
  (none)

Purpose:
The file defines a client-side JavaScript module named 'ExportCSVModule' designed to handle the export of data into CSV format. It specifically targets DOM elements with the class '.export-csv-btn' within a '.focus-area-record-item' container. When triggered, the module extracts JSON data stored in the element's 'data-exportData' attribute, flattens nested 'properties' objects into individual CSV columns (while excluding specific fields like 'input_text_summary'), generates a downloadable CSV file using a Blob, and names the file based on the corresponding header text found in the UI.

Raw AI response:
```json
{
  "referenced_files": [],
  "purpose": "The file defines a client-side JavaScript module named 'ExportCSVModule' designed to handle the export of data into CSV format. It specifically targets DOM elements with the class '.export-csv-btn' within a '.focus-area-record-item' container. When triggered, the module extracts JSON data stored in the element's 'data-exportData' attribute, flattens nested 'properties' objects into individual CSV columns (while excluding specific fields like 'input_text_summary'), generates a downloadable CSV file using a Blob, and names the file based on the corresponding header text found in the UI."
}
```

-------------------------------------------------
File #161
Path: /axialy-production-ui/var/www/html/axialy-ui/js/feedback-confirmation.js

Referenced files:
  (none)

Purpose:
The file `/axialy-production-ui/var/www/html/axialy-ui/js/feedback-confirmation.js` is a client-side JavaScript file responsible for managing the UI state of two specific modal overlays: 'experience-feedback' and 'pending-requests'. It attaches event listeners to trigger buttons and close buttons to toggle the visibility (display: flex/none) of these overlays. It also implements a global keyboard event listener to allow the user to close both overlays by pressing the 'Escape' key. The script is designed to be resilient by checking for the existence of DOM elements before attempting to add listeners.

Raw AI response:
{
  "referenced_files": [],
  "purpose": "The file `/axialy-production-ui/var/www/html/axialy-ui/js/feedback-confirmation.js` is a client-side JavaScript file responsible for managing the UI state of two specific modal overlays: 'experience-feedback' and 'pending-requests'. It attaches event listeners to trigger buttons and close buttons to toggle the visibility (display: flex/none) of these overlays. It also implements a global keyboard event listener to allow the user to close both overlays by pressing the 'Escape' key. The script is designed to be resilient by checking for the existence of DOM elements before attempting to add listeners."
}

-------------------------------------------------
File #162
Path: /axialy-production-ui/var/www/html/axialy-ui/js/focus-area-version.js

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/js/store_analysis_package_focus_area_version.php

Purpose:
The `focus-area-version.js` file serves as a client-side JavaScript module responsible for managing versioning for analysis package focus areas. It provides functionality to increment a version number, persist that update to the server via a POST request to `store_analysis_package_focus_area_version.php`, and dynamically update the document object model (DOM) to reflect the new version number in the UI. Note: The reference to `store_analysis_package_focus_area_version.php` is assumed to reside in the same directory context as the JS file, though its existence was not explicitly provided in the file list.

Raw AI response:
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/js/store_analysis_package_focus_area_version.php"
  ],
  "purpose": "The `focus-area-version.js` file serves as a client-side JavaScript module responsible for managing versioning for analysis package focus areas. It provides functionality to increment a version number, persist that update to the server via a POST request to `store_analysis_package_focus_area_version.php`, and dynamically update the document object model (DOM) to reflect the new version number in the UI. Note: The reference to `store_analysis_package_focus_area_version.php` is assumed to reside in the same directory context as the JS file, though its existence was not explicitly provided in the file list."
}

-------------------------------------------------
File #163
Path: /axialy-production-ui/var/www/html/axialy-ui/js/focus-areas-initialization.js

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/js/focus-areas.js
  - /axialy-production-ui/var/www/html/axialy-ui/js/dynamic-ribbons.js

Purpose:
This file serves as an initialization wrapper for the 'Focus Areas' feature within the Axialy UI. It encapsulates the startup logic using an IIFE (Immediately Invoked Function Expression) and triggers initialization processes for both the Focus Areas and Dynamic Ribbons modules once the DOM is fully loaded. Note: The referenced modules (FocusAreasModule and DynamicRibbonsModule) are expected to be defined in separate files (likely located in the same directory) as this script checks for their existence in the global scope before invoking their respective methods.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/js/focus-areas.js",
    "/axialy-production-ui/var/www/html/axialy-ui/js/dynamic-ribbons.js"
  ],
  "purpose": "This file serves as an initialization wrapper for the 'Focus Areas' feature within the Axialy UI. It encapsulates the startup logic using an IIFE (Immediately Invoked Function Expression) and triggers initialization processes for both the Focus Areas and Dynamic Ribbons modules once the DOM is fully loaded. Note: The referenced modules (FocusAreasModule and DynamicRibbonsModule) are expected to be defined in separate files (likely located in the same directory) as this script checks for their existence in the global scope before invoking their respective methods."
}
```

-------------------------------------------------
File #164
Path: /axialy-production-ui/var/www/html/axialy-ui/js/focus-areas-module.js

Referenced files:
  (none)

Purpose:
The file defines a JavaScript module named 'FocusAreasModule' using the Revealing Module Pattern. Its primary purpose is to provide a structured namespace for managing 'Focus Areas' functionality within the UI, currently exposing an 'initializeAdditionalFeatures' method for potential event handling or feature initialization logic. As the content currently lacks internal implementations, it serves as a boilerplate for future feature expansion related to the Focus Areas component.

Raw AI response:
```json
{
  "referenced_files": [],
  "purpose": "The file defines a JavaScript module named 'FocusAreasModule' using the Revealing Module Pattern. Its primary purpose is to provide a structured namespace for managing 'Focus Areas' functionality within the UI, currently exposing an 'initializeAdditionalFeatures' method for potential event handling or feature initialization logic. As the content currently lacks internal implementations, it serves as a boilerplate for future feature expansion related to the Focus Areas component."
}
```

-------------------------------------------------
File #165
Path: /axialy-production-ui/var/www/html/axialy-ui/js/focus-areas.js

Referenced files:
  - /get_templates.php

Purpose:
The FocusAreasModule is a client-side JavaScript utility responsible for dynamically populating and managing a 'Choose Focus Areas' form in the UI. It fetches a hierarchical list of templates (which can be nested directories or individual JSON files) from the backend via 'get_templates.php' using an API key. Key functionalities include: rendering checkboxes for the templates, providing recursive directory navigation (expand/collapse), implementing 'Select All'/'Unselect All' logic for categorized groups, and interacting with an optional 'ProcessFeedbackModule' to toggle the state of submission and save buttons based on the user's selections. It also handles prepending user-specific stakeholder context text when specific templates are processed.

Raw AI response:
```json
{
  "referenced_files": [
    "/get_templates.php"
  ],
  "purpose": "The FocusAreasModule is a client-side JavaScript utility responsible for dynamically populating and managing a 'Choose Focus Areas' form in the UI. It fetches a hierarchical list of templates (which can be nested directories or individual JSON files) from the backend via 'get_templates.php' using an API key. Key functionalities include: rendering checkboxes for the templates, providing recursive directory navigation (expand/collapse), implementing 'Select All'/'Unselect All' logic for categorized groups, and interacting with an optional 'ProcessFeedbackModule' to toggle the state of submission and save buttons based on the user's selections. It also handles prepending user-specific stakeholder context text when specific templates are processed."
}
```

-------------------------------------------------
File #166
Path: /axialy-production-ui/var/www/html/axialy-ui/js/input-text.js

Referenced files:
  (none)

Purpose:
The file defines a JavaScript module named `InputTextModule` responsible for managing the state and display of a multi-line text input field. Its primary functions are to track character counts against a defined maximum of 50,000, provide visual feedback (CSS class toggling) when the character threshold is approached or exceeded, and update specific UI elements with summary data received via a custom `summarySaved` event. Notably, it acts as a client-side controller that triggers state updates in a separate, implicitly referenced global module, `ProcessFeedbackModule`, to synchronize button states ('Send' and 'Save') based on the input text content.

Raw AI response:
{
  "referenced_files": [],
  "purpose": "The file defines a JavaScript module named `InputTextModule` responsible for managing the state and display of a multi-line text input field. Its primary functions are to track character counts against a defined maximum of 50,000, provide visual feedback (CSS class toggling) when the character threshold is approached or exceeded, and update specific UI elements with summary data received via a custom `summarySaved` event. Notably, it acts as a client-side controller that triggers state updates in a separate, implicitly referenced global module, `ProcessFeedbackModule`, to synchronize button states ('Send' and 'Save') based on the input text content."
}

-------------------------------------------------
File #167
Path: /axialy-production-ui/var/www/html/axialy-ui/js/layout.js

Referenced files:
  - log_errors.php
  - content/home-tab.html
  - assets/css/home-tab.css
  - js/home/home-tab.js
  - content/generate-tab.html
  - assets/css/generate-tab.css
  - js/generate/ui.js
  - js/generate/index.js
  - content/refine-tab.html
  - assets/css/refine-tab.css
  - assets/css/refine-tab-overlays.css
  - js/refine/utils.js
  - js/refine/state.js
  - js/refine/api.js
  - js/refine/ui.js
  - js/refine/events.js
  - js/refine/actions.js
  - js/enhance-content.js
  - js/refine/axialyAssessmentModule.js
  - js/refine/axialyPackageAdvisorModule.js
  - js/refine/index.js
  - js/refine/new-record-overlay.js
  - js/refine/edit-record-overlay.js
  - js/refine/augment-focus-area.js
  - js/refine/recover-focus-area.js
  - content/survey-tab.html
  - assets/css/survey-tab.css
  - js/survey/utils.js
  - js/survey/state.js
  - js/survey/api.js
  - js/survey/ui.js
  - js/survey/events.js
  - js/survey-collate-feedback.js
  - js/survey/index.js
  - content/settings-tab.html
  - assets/css/settings-tab.css
  - js/settings/utils.js
  - js/settings/state.js
  - js/settings/api.js
  - js/settings/ui.js
  - js/settings/events.js
  - js/settings/index.js
  - content/publish-tab.html
  - assets/css/publish-tab.css
  - js/publish/utils.js
  - js/publish/state.js
  - js/publish/api.js
  - js/publish/ui.js
  - js/publish/events.js
  - js/publish/events/expiry-management-events.js
  - js/publish/events/publication-settings-events.js
  - js/publish/events/stakeholder-invitation-events.js
  - js/publish/index.js

Purpose:
This file acts as the central layout controller for the Axialy UI. It manages SPA-like navigation by dynamically loading tab-specific HTML, CSS, and JavaScript modules into the '#overview-panel' based on user interactions. It handles synchronization between the side control panel and a dropdown navigation menu, manages global UI state (like pin/collapsed states, dropdown toggles, and page titles), and facilitates error logging to the server. Additionally, it provides specific utility functions for cross-module integration, such as programmatically switching to and configuring the Refine tab.

Raw AI response:
```json
{
  "referenced_files": [
    "log_errors.php",
    "content/home-tab.html",
    "assets/css/home-tab.css",
    "js/home/home-tab.js",
    "content/generate-tab.html",
    "assets/css/generate-tab.css",
    "js/generate/ui.js",
    "js/generate/index.js",
    "content/refine-tab.html",
    "assets/css/refine-tab.css",
    "assets/css/refine-tab-overlays.css",
    "js/refine/utils.js",
    "js/refine/state.js",
    "js/refine/api.js",
    "js/refine/ui.js",
    "js/refine/events.js",
    "js/refine/actions.js",
    "js/enhance-content.js",
    "js/refine/axialyAssessmentModule.js",
    "js/refine/axialyPackageAdvisorModule.js",
    "js/refine/index.js",
    "js/refine/new-record-overlay.js",
    "js/refine/edit-record-overlay.js",
    "js/refine/augment-focus-area.js",
    "js/refine/recover-focus-area.js",
    "content/survey-tab.html",
    "assets/css/survey-tab.css",
    "js/survey/utils.js",
    "js/survey/state.js",
    "js/survey/api.js",
    "js/survey/ui.js",
    "js/survey/events.js",
    "js/survey-collate-feedback.js",
    "js/survey/index.js",
    "content/settings-tab.html",
    "assets/css/settings-tab.css",
    "js/settings/utils.js",
    "js/settings/state.js",
    "js/settings/api.js",
    "js/settings/ui.js",
    "js/settings/events.js",
    "js/settings/index.js",
    "content/publish-tab.html",
    "assets/css/publish-tab.css",
    "js/publish/utils.js",
    "js/publish/state.js",
    "js/publish/api.js",
    "js/publish/ui.js",
    "js/publish/events.js",
    "js/publish/events/expiry-management-events.js",
    "js/publish/events/publication-settings-events.js",
    "js/publish/events/stakeholder-invitation-events.js",
    "js/publish/index.js"
  ],
  "purpose": "This file acts as the central layout controller for the Axialy UI. It manages SPA-like navigation by dynamically loading tab-specific HTML, CSS, and JavaScript modules into the '#overview-panel' based on user interactions. It handles synchronization between the side control panel and a dropdown navigation menu, manages global UI state (like pin/collapsed states, dropdown toggles, and page titles), and facilitates error logging to the server. Additionally, it provides specific utility functions for cross-module integration, such as programmatically switching to and configuring the Refine tab."
}
```

-------------------------------------------------
File #168
Path: /axialy-production-ui/var/www/html/axialy-ui/js/new-focus-area-creation.js

Referenced files:
  - /process_new_focus_area.php
  - /axialy_helper.php

Purpose:
The file implements the 'NewFocusAreaCreationModule', a JavaScript controller responsible for managing the AI-driven workflow for creating new focus areas within the Axialy system. It triggers upon an 'FA_CREATE' advisor action, providing an interactive overlay where users can review and edit pre-populated data. It facilitates API communication to generate a full focus area specification (using an AI backend) and handles the subsequent submission of that specification back to the server. Additionally, it offers a fallback 'Manual Approach' and manages UI states (loading spinners, form validation, and dynamic content addition for stakeholders/records) to ensure a consistent user experience.

Raw AI response:
```json
{
  "referenced_files": [
    "/process_new_focus_area.php",
    "/axialy_helper.php"
  ],
  "purpose": "The file implements the 'NewFocusAreaCreationModule', a JavaScript controller responsible for managing the AI-driven workflow for creating new focus areas within the Axialy system. It triggers upon an 'FA_CREATE' advisor action, providing an interactive overlay where users can review and edit pre-populated data. It facilitates API communication to generate a full focus area specification (using an AI backend) and handles the subsequent submission of that specification back to the server. Additionally, it offers a fallback 'Manual Approach' and manages UI states (loading spinners, form validation, and dynamic content addition for stakeholders/records) to ensure a consistent user experience."
}
```

-------------------------------------------------
File #169
Path: /axialy-production-ui/var/www/html/axialy-ui/js/new-focus-area-overlay.js

Referenced files:
  - process_new_focus_area.php

Purpose:
This JavaScript file defines a module for the Axialy UI that provides an overlay interface for creating new focus areas within a package. It manages the collection of user-defined property names and associated data records, handling the transition between input states (details vs. records), applying modern brand-compliant styling, and ultimately committing the collected data to the server via a POST request to 'process_new_focus_area.php'.

Raw AI response:
```json
{
  "referenced_files": [
    "process_new_focus_area.php"
  ],
  "purpose": "This JavaScript file defines a module for the Axialy UI that provides an overlay interface for creating new focus areas within a package. It manages the collection of user-defined property names and associated data records, handling the transition between input states (details vs. records), applying modern brand-compliant styling, and ultimately committing the collected data to the server via a POST request to 'process_new_focus_area.php'."
}
```

-------------------------------------------------
File #170
Path: /axialy-production-ui/var/www/html/axialy-ui/js/overlay.js

Referenced files:
  - /get_focus_organization.php
  - /get_custom_organizations.php

Purpose:
This file acts as a UI utility module (`OverlayModule`) responsible for managing modal-style overlays within the browser. It provides methods to display loading states, simple information messages, and a complex 'Header Review' form that allows users to edit analysis package metadata and select an associated organization. The module handles DOM creation/cleanup, mobile-specific viewport locking, and asynchronous data fetching from the backend to populate organization selection dropdowns.

Raw AI response:
```json
{
  "referenced_files": [
    "/get_focus_organization.php",
    "/get_custom_organizations.php"
  ],
  "purpose": "This file acts as a UI utility module (`OverlayModule`) responsible for managing modal-style overlays within the browser. It provides methods to display loading states, simple information messages, and a complex 'Header Review' form that allows users to edit analysis package metadata and select an associated organization. The module handles DOM creation/cleanup, mobile-specific viewport locking, and asynchronous data fetching from the backend to populate organization selection dropdowns."
}
```

-------------------------------------------------
File #171
Path: /axialy-production-ui/var/www/html/axialy-ui/js/process-feedback.js

Referenced files:
  - /ai_helper.php
  - /store_summary.php
  - /get_focus_organization.php
  - /save_analysis_package.php

Purpose:
The `ProcessFeedbackModule` is a JavaScript controller responsible for managing the feedback loop between the user's input, external AI analysis, and persistent storage. Its primary functions include: 

1. Orchestrating the 'Send Selected' workflow: It collects user input, invokes AI to generate summaries, retrieves focus-area records based on selected templates via `ai_helper.php`, and stores summary metadata via `store_summary.php`.
2. Managing UI state: It dynamically controls the 'Send' and 'Save' buttons, handles progress spinners, and updates status messages based on ongoing asynchronous operations.
3. Handling 'Save' functionality: It manages the serialization and consolidation of AI-generated 'ribbons' into a structured format, communicates with the backend to generate package headers, and performs the final persistence of analysis packages via `save_analysis_package.php`.

Note: This module expects several global dependencies (such as `FocusAreasModule`, `DynamicRibbonsModule`, `OverlayModule`, and `AxiaBAConfig`) to be present in the execution environment to function correctly.

Raw AI response:
{
  "referenced_files": [
    "/ai_helper.php",
    "/store_summary.php",
    "/get_focus_organization.php",
    "/save_analysis_package.php"
  ],
  "purpose": "The `ProcessFeedbackModule` is a JavaScript controller responsible for managing the feedback loop between the user's input, external AI analysis, and persistent storage. Its primary functions include: \n\n1. Orchestrating the 'Send Selected' workflow: It collects user input, invokes AI to generate summaries, retrieves focus-area records based on selected templates via `ai_helper.php`, and stores summary metadata via `store_summary.php`.\n2. Managing UI state: It dynamically controls the 'Send' and 'Save' buttons, handles progress spinners, and updates status messages based on ongoing asynchronous operations.\n3. Handling 'Save' functionality: It manages the serialization and consolidation of AI-generated 'ribbons' into a structured format, communicates with the backend to generate package headers, and performs the final persistence of analysis packages via `save_analysis_package.php`.\n\nNote: This module expects several global dependencies (such as `FocusAreasModule`, `DynamicRibbonsModule`, `OverlayModule`, and `AxiaBAConfig`) to be present in the execution environment to function correctly."
}

-------------------------------------------------
File #172
Path: /axialy-production-ui/var/www/html/axialy-ui/js/promo-modal.js

Referenced files:
  - /api/check-default-promo.php
  - /offer/index.php

Purpose:
This file is a client-side JavaScript module responsible for managing a dynamic promotional modal. It automatically triggers an API request to '/api/check-default-promo.php' upon page load to verify if a specific promotional offer (defaulting to 'axialyst') is active. If active, it dynamically injects the offer details into the DOM, handles user interactions (closing via ESC key, clicking outside, or a dedicated button), and redirects users to '/offer/index.php' when they choose to activate the offer.

Raw AI response:
{
  "referenced_files": [
    "/api/check-default-promo.php",
    "/offer/index.php"
  ],
  "purpose": "This file is a client-side JavaScript module responsible for managing a dynamic promotional modal. It automatically triggers an API request to '/api/check-default-promo.php' upon page load to verify if a specific promotional offer (defaulting to 'axialyst') is active. If active, it dynamically injects the offer details into the DOM, handles user interactions (closing via ESC key, clicking outside, or a dedicated button), and redirects users to '/offer/index.php' when they choose to activate the offer."
}

-------------------------------------------------
File #173
Path: /axialy-production-ui/var/www/html/axialy-ui/js/README.md

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/js/account-actions.js
  - /axialy-production-ui/var/www/html/axialy-ui/js/apply-revisions-handler.js
  - /axialy-production-ui/var/www/html/axialy-ui/js/collate-feedback.js
  - /axialy-production-ui/var/www/html/axialy-ui/js/content-review-overlay.js
  - /axialy-production-ui/var/www/html/axialy-ui/js/content-review.js
  - /axialy-production-ui/var/www/html/axialy-ui/js/content-revision.js
  - /axialy-production-ui/var/www/html/axialy-ui/js/dynamic-ribbons.js
  - /axialy-production-ui/var/www/html/axialy-ui/js/enhance-content.js
  - /axialy-production-ui/var/www/html/axialy-ui/js/export-csv.js
  - /axialy-production-ui/var/www/html/axialy-ui/js/feedback-confirmation.js
  - /axialy-production-ui/var/www/html/axialy-ui/js/focus-area-version.js
  - /axialy-production-ui/var/www/html/axialy-ui/js/focus-areas-initialization.js
  - /axialy-production-ui/var/www/html/axialy-ui/js/focus-areas-module.js
  - /axialy-production-ui/var/www/html/axialy-ui/js/focus-areas.js
  - /axialy-production-ui/var/www/html/axialy-ui/js/input-text.js
  - /axialy-production-ui/var/www/html/axialy-ui/js/layout.js
  - /axialy-production-ui/var/www/html/axialy-ui/js/new-focus-area-overlay.js
  - /axialy-production-ui/var/www/html/axialy-ui/js/overlay.js
  - /axialy-production-ui/var/www/html/axialy-ui/js/process-feedback.js
  - /axialy-production-ui/var/www/html/axialy-ui/js/ribbon-handler.js
  - /axialy-production-ui/var/www/html/axialy-ui/js/ribbon-toggles.js
  - /axialy-production-ui/var/www/html/axialy-ui/js/revised-records-overlay.js
  - /axialy-production-ui/var/www/html/axialy-ui/js/save-analysis-package.js
  - /axialy-production-ui/var/www/html/axialy-ui/js/stakeholder-content-review.js
  - /axialy-production-ui/var/www/html/axialy-ui/js/support-tickets.js
  - /axialy-production-ui/var/www/html/axialy-ui/js/update-overview-panel.js
  - /axialy-production-ui/var/www/html/axialy-ui/js/dashboard/
  - /axialy-production-ui/var/www/html/axialy-ui/js/publish/
  - /axialy-production-ui/var/www/html/axialy-ui/js/settings/

Purpose:
This file serves as the documentation and manifest for the core JavaScript modules located in the /js/ directory. It provides a structured overview of the UI components, which include functionality for focus-area management, AI feedback processing, content review flows, and global layout orchestration.

Raw AI response:
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/js/account-actions.js",
    "/axialy-production-ui/var/www/html/axialy-ui/js/apply-revisions-handler.js",
    "/axialy-production-ui/var/www/html/axialy-ui/js/collate-feedback.js",
    "/axialy-production-ui/var/www/html/axialy-ui/js/content-review-overlay.js",
    "/axialy-production-ui/var/www/html/axialy-ui/js/content-review.js",
    "/axialy-production-ui/var/www/html/axialy-ui/js/content-revision.js",
    "/axialy-production-ui/var/www/html/axialy-ui/js/dynamic-ribbons.js",
    "/axialy-production-ui/var/www/html/axialy-ui/js/enhance-content.js",
    "/axialy-production-ui/var/www/html/axialy-ui/js/export-csv.js",
    "/axialy-production-ui/var/www/html/axialy-ui/js/feedback-confirmation.js",
    "/axialy-production-ui/var/www/html/axialy-ui/js/focus-area-version.js",
    "/axialy-production-ui/var/www/html/axialy-ui/js/focus-areas-initialization.js",
    "/axialy-production-ui/var/www/html/axialy-ui/js/focus-areas-module.js",
    "/axialy-production-ui/var/www/html/axialy-ui/js/focus-areas.js",
    "/axialy-production-ui/var/www/html/axialy-ui/js/input-text.js",
    "/axialy-production-ui/var/www/html/axialy-ui/js/layout.js",
    "/axialy-production-ui/var/www/html/axialy-ui/js/new-focus-area-overlay.js",
    "/axialy-production-ui/var/www/html/axialy-ui/js/overlay.js",
    "/axialy-production-ui/var/www/html/axialy-ui/js/process-feedback.js",
    "/axialy-production-ui/var/www/html/axialy-ui/js/ribbon-handler.js",
    "/axialy-production-ui/var/www/html/axialy-ui/js/ribbon-toggles.js",
    "/axialy-production-ui/var/www/html/axialy-ui/js/revised-records-overlay.js",
    "/axialy-production-ui/var/www/html/axialy-ui/js/save-analysis-package.js",
    "/axialy-production-ui/var/www/html/axialy-ui/js/stakeholder-content-review.js",
    "/axialy-production-ui/var/www/html/axialy-ui/js/support-tickets.js",
    "/axialy-production-ui/var/www/html/axialy-ui/js/update-overview-panel.js",
    "/axialy-production-ui/var/www/html/axialy-ui/js/dashboard/",
    "/axialy-production-ui/var/www/html/axialy-ui/js/publish/",
    "/axialy-production-ui/var/www/html/axialy-ui/js/settings/"
  ],
  "purpose": "This file serves as the documentation and manifest for the core JavaScript modules located in the /js/ directory. It provides a structured overview of the UI components, which include functionality for focus-area management, AI feedback processing, content review flows, and global layout orchestration."
}

-------------------------------------------------
File #174
Path: /axialy-production-ui/var/www/html/axialy-ui/js/refine-tab-initialization.js

Referenced files:
  (none)

Purpose:
The file defines a JavaScript module 'RefineTabInitializationModule' responsible for configuring UI components specifically for the 'Refine' tab within the Axialy production interface. Its primary function is to initialize necessary UI elements (such as dynamic ribbon toggles via 'DynamicRibbonsModule') while explicitly excluding features relevant only to the 'Generate' tab (like input focus and feedback processing modules). While it checks for the existence of 'DynamicRibbonsModule' to ensure compatibility, it does not explicitly import or define a path to that dependency within the provided snippet.

Raw AI response:
```json
{
  "referenced_files": [],
  "purpose": "The file defines a JavaScript module 'RefineTabInitializationModule' responsible for configuring UI components specifically for the 'Refine' tab within the Axialy production interface. Its primary function is to initialize necessary UI elements (such as dynamic ribbon toggles via 'DynamicRibbonsModule') while explicitly excluding features relevant only to the 'Generate' tab (like input focus and feedback processing modules). While it checks for the existence of 'DynamicRibbonsModule' to ensure compatibility, it does not explicitly import or define a path to that dependency within the provided snippet."
}
```

-------------------------------------------------
File #175
Path: /axialy-production-ui/var/www/html/axialy-ui/js/revised-records-overlay.js

Referenced files:
  - /save_revised_records.php

Purpose:
The file implements a JavaScript module (`RevisedRecordsOverlay`) designed to manage the final review and submission of updated focus area records. It generates a UI overlay that sorts records by 'focusAreaRecordNumber', presents them in an editable table format (with specific internal fields excluded), and allows the user to commit these changes via a POST request to '/save_revised_records.php'. It also includes helper functionality to manage the loading state and triggers a client-side callback (`reloadRefineTabAndOpenPackage`) upon successful server-side processing.

Raw AI response:
```json
{
  "referenced_files": [
    "/save_revised_records.php"
  ],
  "purpose": "The file implements a JavaScript module (`RevisedRecordsOverlay`) designed to manage the final review and submission of updated focus area records. It generates a UI overlay that sorts records by 'focusAreaRecordNumber', presents them in an editable table format (with specific internal fields excluded), and allows the user to commit these changes via a POST request to '/save_revised_records.php'. It also includes helper functionality to manage the loading state and triggers a client-side callback (`reloadRefineTabAndOpenPackage`) upon successful server-side processing."
}
```

-------------------------------------------------
File #176
Path: /axialy-production-ui/var/www/html/axialy-ui/js/ribbon-handler.js

Referenced files:
  (none)

Purpose:
The file `/axialy-production-ui/var/www/html/axialy-ui/js/ribbon-handler.js` is a client-side JavaScript module responsible for managing the UI behavior of 'static ribbons' within the application. Its primary purpose is to provide toggle functionality (expand/collapse) for UI elements that contain content headers. It handles existing DOM elements with the class '.notifications-ribbon' and also provides a programmatic function, 'displayNotifications()', to dynamically inject a notifications ribbon into a container identified as 'ribbons-container'. The script is designed to exclude dynamic template processing to maintain a separation of concerns.

Raw AI response:
{
  "referenced_files": [],
  "purpose": "The file `/axialy-production-ui/var/www/html/axialy-ui/js/ribbon-handler.js` is a client-side JavaScript module responsible for managing the UI behavior of 'static ribbons' within the application. Its primary purpose is to provide toggle functionality (expand/collapse) for UI elements that contain content headers. It handles existing DOM elements with the class '.notifications-ribbon' and also provides a programmatic function, 'displayNotifications()', to dynamically inject a notifications ribbon into a container identified as 'ribbons-container'. The script is designed to exclude dynamic template processing to maintain a separation of concerns."
}

-------------------------------------------------
File #177
Path: /axialy-production-ui/var/www/html/axialy-ui/js/ribbon-toggles.js

Referenced files:
  (none)

Purpose:
This file provides utility functions for managing the UI state of 'ribbons' on the webpage. It defines two main functions: 'setupRibbonToggles', which manages the expansion and collapse behavior for input and feedback sections (optionally triggering a callback to 'ProcessFeedbackModule'), and 'setupPackagesRibbonToggle', which handles the specific collapse/expand logic for an 'Analysis Packages' section using CSS class toggling. The code implicitly relies on a globally defined 'ProcessFeedbackModule' object when the toggle logic is invoked with the update flag set to true.

Raw AI response:
```json
{
  "referenced_files": [],
  "purpose": "This file provides utility functions for managing the UI state of 'ribbons' on the webpage. It defines two main functions: 'setupRibbonToggles', which manages the expansion and collapse behavior for input and feedback sections (optionally triggering a callback to 'ProcessFeedbackModule'), and 'setupPackagesRibbonToggle', which handles the specific collapse/expand logic for an 'Analysis Packages' section using CSS class toggling. The code implicitly relies on a globally defined 'ProcessFeedbackModule' object when the toggle logic is invoked with the update flag set to true."
}
```

-------------------------------------------------
File #178
Path: /axialy-production-ui/var/www/html/axialy-ui/js/save-analysis-package.js

Referenced files:
  - /ai_helper.php
  - /save_analysis_package.php

Purpose:
The purpose of this module is to orchestrate the saving of an 'Analysis Package' from the UI. It functions by gathering data from 'DynamicRibbonsModule', interacting with an AI service via 'ai_helper.php' to generate a package header, allowing the user to review/edit this header through an 'OverlayModule', and finally persisting the consolidated package data to the database via 'save_analysis_package.php'. Upon a successful save, it handles UI cleanup, including resetting input fields, clearing UI state, and resetting character counts and summary IDs.

Raw AI response:
```json
{
  "referenced_files": [
    "/ai_helper.php",
    "/save_analysis_package.php"
  ],
  "purpose": "The purpose of this module is to orchestrate the saving of an 'Analysis Package' from the UI. It functions by gathering data from 'DynamicRibbonsModule', interacting with an AI service via 'ai_helper.php' to generate a package header, allowing the user to review/edit this header through an 'OverlayModule', and finally persisting the consolidated package data to the database via 'save_analysis_package.php'. Upon a successful save, it handles UI cleanup, including resetting input fields, clearing UI state, and resetting character counts and summary IDs."
}
```

-------------------------------------------------
File #179
Path: /axialy-production-ui/var/www/html/axialy-ui/js/stakeholder-content-review.js

Referenced files:
  (none)

Purpose:
This JavaScript file handles the client-side interaction logic for a stakeholder content review system. It manages two modes of feedback: 'General' (a standard textarea input) and 'Itemized' (a grid-based interface allowing users to select 'Primary' or 'Secondary' actions for specific data records). It includes logic for opening/closing feedback overlays, updating form inputs based on user selection, applying visual feedback (highlighting/borders) to the UI, and performing form submission validation and UI masking (loading states) before the form is sent to the server.

Raw AI response:
{
  "referenced_files": [],
  "purpose": "This JavaScript file handles the client-side interaction logic for a stakeholder content review system. It manages two modes of feedback: 'General' (a standard textarea input) and 'Itemized' (a grid-based interface allowing users to select 'Primary' or 'Secondary' actions for specific data records). It includes logic for opening/closing feedback overlays, updating form inputs based on user selection, applying visual feedback (highlighting/borders) to the UI, and performing form submission validation and UI masking (loading states) before the form is sent to the server."
}

-------------------------------------------------
File #180
Path: /axialy-production-ui/var/www/html/axialy-ui/js/support-tickets.js

Referenced files:
  - /issue_ajax_actions.php
  - /assets/css/support-tickets.css

Purpose:
This file implements the client-side UI logic for a 'Support Tickets' management system. It dynamically creates and manages an overlay container to allow users to view their existing support tickets, inspect ticket details, and submit new support requests. The file handles API communication with the server via /issue_ajax_actions.php for CRUD operations and dynamically manages DOM elements to switch between the list view, details view, and submission form. Note: The code contains an optional (currently commented-out) call to load a stylesheet from /assets/css/support-tickets.css.

Raw AI response:
```json
{
  "referenced_files": [
    "/issue_ajax_actions.php",
    "/assets/css/support-tickets.css"
  ],
  "purpose": "This file implements the client-side UI logic for a 'Support Tickets' management system. It dynamically creates and manages an overlay container to allow users to view their existing support tickets, inspect ticket details, and submit new support requests. The file handles API communication with the server via /issue_ajax_actions.php for CRUD operations and dynamically manages DOM elements to switch between the list view, details view, and submission form. Note: The code contains an optional (currently commented-out) call to load a stylesheet from /assets/css/support-tickets.css."
}
```

-------------------------------------------------
File #181
Path: /axialy-production-ui/var/www/html/axialy-ui/js/survey-collate-feedback.js

Referenced files:
  - fetch_survey_feedback_details.php

Purpose:
The file `/js/survey-collate-feedback.js` serves as a dedicated module for rendering and managing an interactive UI overlay used to compile and review stakeholder feedback specifically for survey-based requests. It bridges the gap between raw survey feedback data and the system's general feedback aggregation logic by transforming raw data into an 'aggregator format.' Key functionalities include fetching survey feedback via a backend PHP endpoint, rendering a collapsible UI to view/process general and itemized feedback, managing UI states for user actions (Apply, Add Instruction, Ignore), and providing an interface to trigger the `ApplyRevisionsHandler` once feedback is processed.

Raw AI response:
```json
{
  "referenced_files": [
    "fetch_survey_feedback_details.php"
  ],
  "purpose": "The file `/js/survey-collate-feedback.js` serves as a dedicated module for rendering and managing an interactive UI overlay used to compile and review stakeholder feedback specifically for survey-based requests. It bridges the gap between raw survey feedback data and the system's general feedback aggregation logic by transforming raw data into an 'aggregator format.' Key functionalities include fetching survey feedback via a backend PHP endpoint, rendering a collapsible UI to view/process general and itemized feedback, managing UI states for user actions (Apply, Add Instruction, Ignore), and providing an interface to trigger the `ApplyRevisionsHandler` once feedback is processed."
}
```

-------------------------------------------------
File #182
Path: /axialy-production-ui/var/www/html/axialy-ui/js/update-overview-panel.js

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/content/dashboard-tab.html
  - /axialy-production-ui/var/www/html/axialy-ui/assets/css/dashboard-tab.css
  - /axialy-production-ui/var/www/html/axialy-ui/js/dashboard/dashboard.js
  - /axialy-production-ui/var/www/html/axialy-ui/content/survey-tab.html
  - /axialy-production-ui/var/www/html/axialy-ui/assets/css/survey-tab.css
  - /axialy-production-ui/var/www/html/axialy-ui/content/settings-tab.html
  - /axialy-production-ui/var/www/html/axialy-ui/assets/css/settings-tab.css
  - /axialy-production-ui/var/www/html/axialy-ui/js/settings-tab.js

Purpose:
This file serves as a dynamic loader for the application's main navigation tabs (Dashboard, Survey, and Settings). It provides functions to fetch HTML partials and inject them into the 'overview-panel' element, while concurrently managing the asynchronous loading or updating of required CSS and JavaScript resources to ensure modularity. Note that the script logic assumes global modules like 'SurveyIndexModule' and 'SettingsModule' are pre-loaded in the browser environment.

Raw AI response:
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/content/dashboard-tab.html",
    "/axialy-production-ui/var/www/html/axialy-ui/assets/css/dashboard-tab.css",
    "/axialy-production-ui/var/www/html/axialy-ui/js/dashboard/dashboard.js",
    "/axialy-production-ui/var/www/html/axialy-ui/content/survey-tab.html",
    "/axialy-production-ui/var/www/html/axialy-ui/assets/css/survey-tab.css",
    "/axialy-production-ui/var/www/html/axialy-ui/content/settings-tab.html",
    "/axialy-production-ui/var/www/html/axialy-ui/assets/css/settings-tab.css",
    "/axialy-production-ui/var/www/html/axialy-ui/js/settings-tab.js"
  ],
  "purpose": "This file serves as a dynamic loader for the application's main navigation tabs (Dashboard, Survey, and Settings). It provides functions to fetch HTML partials and inject them into the 'overview-panel' element, while concurrently managing the asynchronous loading or updating of required CSS and JavaScript resources to ensure modularity. Note that the script logic assumes global modules like 'SurveyIndexModule' and 'SettingsModule' are pre-loaded in the browser environment."
}

-------------------------------------------------
File #183
Path: /axialy-production-ui/var/www/html/axialy-ui/offer/api/check_existing_user.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php

Purpose:
This file serves as a JSON API endpoint designed to facilitate user onboarding and offer redemption. Its primary purpose is to validate user eligibility for promotional offers by checking three criteria: whether an account exists for a provided email address, whether that account has an active subscription, and whether the user has previously redeemed a specific promotional code. It is intended to be called during the user checkout or sign-up flow to guide the client on whether to proceed with new registration, require a login, or apply a discount code.

Raw AI response:
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php"
  ],
  "purpose": "This file serves as a JSON API endpoint designed to facilitate user onboarding and offer redemption. Its primary purpose is to validate user eligibility for promotional offers by checking three criteria: whether an account exists for a provided email address, whether that account has an active subscription, and whether the user has previously redeemed a specific promotional code. It is intended to be called during the user checkout or sign-up flow to guide the client on whether to proceed with new registration, require a login, or apply a discount code."
}

-------------------------------------------------
File #184
Path: /axialy-production-ui/var/www/html/axialy-ui/offer/api/create_promo_subscription.php

Referenced files:
  - /axialy-production-ui/var/www/html/vendor/autoload.php
  - /axialy-production-ui/var/www/html/includes/db_connection.php
  - /axialy-production-ui/var/www/html/includes/Config.php

Purpose:
This file serves as a backend API endpoint to handle the registration of new users who are signing up using a promotional code. It coordinates a multi-step process: it validates user input and email verification status, processes payments via Stripe (supporting both lifetime discounts and limited-duration promotional pricing using Stripe Subscription Schedules), creates the user account and default organization in the local database, records the promo code redemption, and initializes a user session for immediate auto-login. The script includes rollback logic to ensure that if account creation fails after a Stripe subscription has been initiated, the subscription is cancelled.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/vendor/autoload.php",
    "/axialy-production-ui/var/www/html/includes/db_connection.php",
    "/axialy-production-ui/var/www/html/includes/Config.php"
  ],
  "purpose": "This file serves as a backend API endpoint to handle the registration of new users who are signing up using a promotional code. It coordinates a multi-step process: it validates user input and email verification status, processes payments via Stripe (supporting both lifetime discounts and limited-duration promotional pricing using Stripe Subscription Schedules), creates the user account and default organization in the local database, records the promo code redemption, and initializes a user session for immediate auto-login. The script includes rollback logic to ensure that if account creation fails after a Stripe subscription has been initiated, the subscription is cancelled."
}
```

-------------------------------------------------
File #185
Path: /axialy-production-ui/var/www/html/axialy-ui/offer/api/reactivate_subscription.php

Referenced files:
  - /axialy-production-ui/var/www/html/vendor/autoload.php
  - /axialy-production-ui/var/www/html/includes/db_connection.php
  - /axialy-production-ui/var/www/html/includes/Config.php

Purpose:
This script handles the backend logic for reactivating an existing user's subscription via a POST request. It validates the user's credentials and promo code eligibility, integrates with the Stripe API to create a subscription or subscription schedule (depending on the promo terms), updates the local database with the new subscription status and redemption history, and automatically logs the user into the system by creating a new session. It includes error handling for payment failures and 3D Secure verification requirements.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/vendor/autoload.php",
    "/axialy-production-ui/var/www/html/includes/db_connection.php",
    "/axialy-production-ui/var/www/html/includes/Config.php"
  ],
  "purpose": "This script handles the backend logic for reactivating an existing user's subscription via a POST request. It validates the user's credentials and promo code eligibility, integrates with the Stripe API to create a subscription or subscription schedule (depending on the promo terms), updates the local database with the new subscription status and redemption history, and automatically logs the user into the system by creating a new session. It includes error handling for payment failures and 3D Secure verification requirements."
}
```

-------------------------------------------------
File #186
Path: /axialy-production-ui/var/www/html/axialy-ui/offer/api/send_verification.php

Referenced files:
  - /axialy-production-ui/var/www/html/includes/db_connection.php
  - /axialy-production-ui/var/www/html/includes/Mailer.php

Purpose:
This script acts as a backend API endpoint (POST /offer/api/send_verification.php) responsible for generating and sending a 6-digit email verification code to users. It handles the validation of input, generates a time-limited verification token (stored in the `email_verifications` database table), and triggers an email dispatch via the `Mailer` utility class. The file is designed to support both new and existing users during the signup/offer flow, as noted in the file comments regarding the removal of an existing user check.

Raw AI response:
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/includes/db_connection.php",
    "/axialy-production-ui/var/www/html/includes/Mailer.php"
  ],
  "purpose": "This script acts as a backend API endpoint (POST /offer/api/send_verification.php) responsible for generating and sending a 6-digit email verification code to users. It handles the validation of input, generates a time-limited verification token (stored in the `email_verifications` database table), and triggers an email dispatch via the `Mailer` utility class. The file is designed to support both new and existing users during the signup/offer flow, as noted in the file comments regarding the removal of an existing user check."
}

-------------------------------------------------
File #187
Path: /axialy-production-ui/var/www/html/axialy-ui/offer/api/validate_promo.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/Config.php
  - /axialy-production-ui/var/www/html/axialy-ui/vendor/autoload.php

Purpose:
This file serves as a server-side API endpoint for validating promotional codes provided by users. It verifies the existence, activity status, expiration dates, and usage limits of a promo code against a database table ('promo_codes'). If valid, it interacts with the Stripe API using configuration details (API keys and price IDs) to fetch and return the promotional pricing and standard pricing, allowing the frontend to display accurate plan costs to the user.

Raw AI response:
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/Config.php",
    "/axialy-production-ui/var/www/html/axialy-ui/vendor/autoload.php"
  ],
  "purpose": "This file serves as a server-side API endpoint for validating promotional codes provided by users. It verifies the existence, activity status, expiration dates, and usage limits of a promo code against a database table ('promo_codes'). If valid, it interacts with the Stripe API using configuration details (API keys and price IDs) to fetch and return the promotional pricing and standard pricing, allowing the frontend to display accurate plan costs to the user."
}

-------------------------------------------------
File #188
Path: /axialy-production-ui/var/www/html/axialy-ui/offer/api/verify_code.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php

Purpose:
The primary purpose of this file is to handle the backend verification of a user-provided email verification code. It receives a POST request containing an email address and a 6-digit code, validates the inputs, checks the database ('email_verifications' table) to ensure the code is valid and not expired, and marks the code as 'used' upon successful verification. It serves as an API endpoint for the user registration or offer flow.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php"
  ],
  "purpose": "The primary purpose of this file is to handle the backend verification of a user-provided email verification code. It receives a POST request containing an email address and a 6-digit code, validates the inputs, checks the database ('email_verifications' table) to ensure the code is valid and not expired, and marks the code as 'used' upon successful verification. It serves as an API endpoint for the user registration or offer flow."
}
```

-------------------------------------------------
File #189
Path: /axialy-production-ui/var/www/html/axialy-ui/offer/index.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/Config.php
  - /axialy-production-ui/var/www/html/axialy-ui/offer/api/validate_promo.php
  - /axialy-production-ui/var/www/html/axialy-ui/offer/api/send_verification.php
  - /axialy-production-ui/var/www/html/axialy-ui/offer/api/verify_code.php
  - /axialy-production-ui/var/www/html/axialy-ui/offer/api/check_existing_user.php
  - /axialy-production-ui/var/www/html/axialy-ui/offer/api/create_promo_subscription.php
  - /axialy-production-ui/var/www/html/axialy-ui/offer/api/reactivate_subscription.php
  - /login.php
  - /index.php

Purpose:
This file serves as the landing page for an Axialy AI promotional offer. Its functional purpose is to allow users to redeem a promotional code by validating it, verifying their identity via email, and either creating a new user account or reactivating an existing subscription. It integrates with Stripe for secure payment processing and handles the multi-step user onboarding flow (Promo Validation -> Email Verification -> User Flow Detection -> Payment/Signup). Note that the client-side code dynamically references several API endpoints in the '/offer/api/' directory which are presumed to exist to support the backend logic.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/Config.php",
    "/axialy-production-ui/var/www/html/axialy-ui/offer/api/validate_promo.php",
    "/axialy-production-ui/var/www/html/axialy-ui/offer/api/send_verification.php",
    "/axialy-production-ui/var/www/html/axialy-ui/offer/api/verify_code.php",
    "/axialy-production-ui/var/www/html/axialy-ui/offer/api/check_existing_user.php",
    "/axialy-production-ui/var/www/html/axialy-ui/offer/api/create_promo_subscription.php",
    "/axialy-production-ui/var/www/html/axialy-ui/offer/api/reactivate_subscription.php",
    "/login.php",
    "/index.php"
  ],
  "purpose": "This file serves as the landing page for an Axialy AI promotional offer. Its functional purpose is to allow users to redeem a promotional code by validating it, verifying their identity via email, and either creating a new user account or reactivating an existing subscription. It integrates with Stripe for secure payment processing and handles the multi-step user onboarding flow (Promo Validation -> Email Verification -> User Flow Detection -> Payment/Signup). Note that the client-side code dynamically references several API endpoints in the '/offer/api/' directory which are presumed to exist to support the backend logic."
}
```

-------------------------------------------------
File #190
Path: /axialy-production-ui/var/www/html/axialy-ui/stakeholder-feedback/feedback-confirmation.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php
  - /assets/css/feedback-confirmation.css
  - /assets/img/product_logo.png
  - /js/feedback-confirmation.js
  - /axialy-production-ui/var/www/html/axialy-ui/receive_stakeholder_feedback.php

Purpose:
This file serves as a post-submission landing page for stakeholders after they have submitted feedback. Its primary functions are: 1) To confirm successful submission, 2) To provide an interface for stakeholders to submit additional 'user experience' feedback regarding the feedback process itself, and 3) To display a summary of any other pending feedback requests associated with the stakeholder's email address, allowing them to navigate directly to those tasks. The file handles session-based authentication, performs database queries to retrieve pending feedback items, and manages the ingestion of user experience feedback via POST requests.

Raw AI response:
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php",
    "/assets/css/feedback-confirmation.css",
    "/assets/img/product_logo.png",
    "/js/feedback-confirmation.js",
    "/axialy-production-ui/var/www/html/axialy-ui/receive_stakeholder_feedback.php"
  ],
  "purpose": "This file serves as a post-submission landing page for stakeholders after they have submitted feedback. Its primary functions are: 1) To confirm successful submission, 2) To provide an interface for stakeholders to submit additional 'user experience' feedback regarding the feedback process itself, and 3) To display a summary of any other pending feedback requests associated with the stakeholder's email address, allowing them to navigate directly to those tasks. The file handles session-based authentication, performs database queries to retrieve pending feedback items, and manages the ingestion of user experience feedback via POST requests."
}

-------------------------------------------------
File #191
Path: /axialy-production-ui/var/www/html/axialy-ui/stakeholder-feedback/feedback-form-request.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php
  - /assets/css/feedback-form-request.css

Purpose:
This file serves as a public-facing interface for stakeholders to request a specific feedback form associated with an analysis package and a defined focus area. It handles the request by validating the input parameters (package_id and focus_area_name) against the database, authenticating the user via an active session (storing the stakeholder's email), and persisting the request into the `stakeholder_feedback_header_requests` table upon form submission.

Raw AI response:
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php",
    "/assets/css/feedback-form-request.css"
  ],
  "purpose": "This file serves as a public-facing interface for stakeholders to request a specific feedback form associated with an analysis package and a defined focus area. It handles the request by validating the input parameters (package_id and focus_area_name) against the database, authenticating the user via an active session (storing the stakeholder's email), and persisting the request into the `stakeholder_feedback_header_requests` table upon form submission."
}

-------------------------------------------------
File #192
Path: /axialy-production-ui/var/www/html/axialy-ui/stakeholder-feedback/README.md

Referenced files:
  - /assets/css/feedback-confirmation.css
  - /assets/js/feedback-confirmation.js
  - /assets/css/feedback-form-request.css
  - /assets/css/stakeholder-content-review.css
  - /js/stakeholder-content-review.js
  - /axialy-production-ui/var/www/html/axialy-ui/stakeholder-feedback/feedback-confirmation.php
  - /axialy-production-ui/var/www/html/axialy-ui/stakeholder-feedback/feedback-form-request.php
  - /axialy-production-ui/var/www/html/axialy-ui/stakeholder-feedback/stakeholder-content-review.php

Purpose:
This file acts as the documentation and manifest for the stakeholder-feedback module. It outlines the architectural components that enable stakeholders to request, review, and submit feedback on analysis package focus areas within the Axialy platform. The module consists of a submission confirmation page, a request form handler, and the primary content review interface.

Raw AI response:
```json
{
  "referenced_files": [
    "/assets/css/feedback-confirmation.css",
    "/assets/js/feedback-confirmation.js",
    "/assets/css/feedback-form-request.css",
    "/assets/css/stakeholder-content-review.css",
    "/js/stakeholder-content-review.js",
    "/axialy-production-ui/var/www/html/axialy-ui/stakeholder-feedback/feedback-confirmation.php",
    "/axialy-production-ui/var/www/html/axialy-ui/stakeholder-feedback/feedback-form-request.php",
    "/axialy-production-ui/var/www/html/axialy-ui/stakeholder-feedback/stakeholder-content-review.php"
  ],
  "purpose": "This file acts as the documentation and manifest for the stakeholder-feedback module. It outlines the architectural components that enable stakeholders to request, review, and submit feedback on analysis package focus areas within the Axialy platform. The module consists of a submission confirmation page, a request form handler, and the primary content review interface."
}
```

-------------------------------------------------
File #193
Path: /axialy-production-ui/var/www/html/axialy-ui/stakeholder-feedback/stakeholder-content-review.php

Referenced files:
  - /axialy-production-ui/var/www/html/includes/db_connection.php
  - /serve_logo.php
  - /assets/css/stakeholder-content-review.css
  - /stakeholder-feedback/feedback-confirmation.php
  - /assets/img/product_logo.png
  - /js/stakeholder-content-review.js
  - /js/feedback-confirmation.js

Purpose:
This file serves as the public-facing portal for external stakeholders to review content and submit feedback on analysis packages. It manages the entire feedback workflow, including secure token-based authentication with a 4-digit PIN, dynamic rendering of content based on form type (General vs. Itemized), and processing of user submissions back into the database. It also handles organization-specific branding, print-to-PDF formatting, and session management to ensure data integrity during the review process.

Raw AI response:
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/includes/db_connection.php",
    "/serve_logo.php",
    "/assets/css/stakeholder-content-review.css",
    "/stakeholder-feedback/feedback-confirmation.php",
    "/assets/img/product_logo.png",
    "/js/stakeholder-content-review.js",
    "/js/feedback-confirmation.js"
  ],
  "purpose": "This file serves as the public-facing portal for external stakeholders to review content and submit feedback on analysis packages. It manages the entire feedback workflow, including secure token-based authentication with a 4-digit PIN, dynamic rendering of content based on form type (General vs. Itemized), and processing of user submissions back into the database. It also handles organization-specific branding, print-to-PDF formatting, and session management to ensure data integrity during the review process."
}

-------------------------------------------------
File #194
Path: /axialy-production-ui/var/www/html/axialy-ui/vendor/composer/autoload_namespaces.php

Referenced files:
  (none)

Purpose:
This file is a generated configuration file produced by Composer, PHP's dependency manager. Its specific purpose is to return a map of PSR-0 style namespace prefixes to their corresponding directory paths for class autoloading. In this specific instance, the array is empty, indicating that the project is likely using PSR-4 or classmap autoloading exclusively, rather than the legacy PSR-0 namespace standard.

Raw AI response:
{
  "referenced_files": [],
  "purpose": "This file is a generated configuration file produced by Composer, PHP's dependency manager. Its specific purpose is to return a map of PSR-0 style namespace prefixes to their corresponding directory paths for class autoloading. In this specific instance, the array is empty, indicating that the project is likely using PSR-4 or classmap autoloading exclusively, rather than the legacy PSR-0 namespace standard."
}

-------------------------------------------------
File #195
Path: /axialy-production-ui/var/www/html/axialy-ui/vendor/composer/autoload_psr4.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/vendor/stripe/stripe-php/lib
  - /axialy-production-ui/var/www/html/axialy-ui/vendor/phpmailer/phpmailer/src
  - /axialy-production-ui/var/www/html/axialy-ui/includes

Purpose:
This file is an auto-generated Composer configuration file used for PSR-4 compliant class loading. Its primary purpose is to map namespaces (Stripe, PHPMailer, and AxiaBA) to their corresponding directory paths within the project, enabling the application to automatically locate and load classes without manual 'require' or 'include' statements.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/vendor/stripe/stripe-php/lib",
    "/axialy-production-ui/var/www/html/axialy-ui/vendor/phpmailer/phpmailer/src",
    "/axialy-production-ui/var/www/html/axialy-ui/includes"
  ],
  "purpose": "This file is an auto-generated Composer configuration file used for PSR-4 compliant class loading. Its primary purpose is to map namespaces (Stripe, PHPMailer, and AxiaBA) to their corresponding directory paths within the project, enabling the application to automatically locate and load classes without manual 'require' or 'include' statements."
}
```

-------------------------------------------------
File #196
Path: /axialy-production-ui/var/www/html/axialy-ui/vendor/composer/autoload_real.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/vendor/composer/ClassLoader.php
  - /axialy-production-ui/var/www/html/axialy-ui/vendor/composer/platform_check.php
  - /axialy-production-ui/var/www/html/axialy-ui/vendor/composer/autoload_static.php

Purpose:
This file is a generated entry point for the Composer autoloader. Its primary responsibility is to initialize the PHP class-loading mechanism by instantiating the Composer\Autoload\ClassLoader, configuring it with class maps and namespace mappings defined in 'autoload_static.php', and performing a system platform check. It ensures that all dependencies managed by Composer are available to the application at runtime.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/vendor/composer/ClassLoader.php",
    "/axialy-production-ui/var/www/html/axialy-ui/vendor/composer/platform_check.php",
    "/axialy-production-ui/var/www/html/axialy-ui/vendor/composer/autoload_static.php"
  ],
  "purpose": "This file is a generated entry point for the Composer autoloader. Its primary responsibility is to initialize the PHP class-loading mechanism by instantiating the Composer\\Autoload\\ClassLoader, configuring it with class maps and namespace mappings defined in 'autoload_static.php', and performing a system platform check. It ensures that all dependencies managed by Composer are available to the application at runtime."
}
```

-------------------------------------------------
File #197
Path: /axialy-production-ui/var/www/html/axialy-ui/vendor/composer/autoload_static.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/Mailer.php
  - /axialy-production-ui/var/www/html/axialy-ui/vendor/composer/InstalledVersions.php
  - /axialy-production-ui/var/www/html/axialy-ui/vendor/phpmailer/phpmailer/src/DSNConfigurator.php
  - /axialy-production-ui/var/www/html/axialy-ui/vendor/phpmailer/phpmailer/src/Exception.php
  - /axialy-production-ui/var/www/html/axialy-ui/vendor/phpmailer/phpmailer/src/OAuth.php
  - /axialy-production-ui/var/www/html/axialy-ui/vendor/phpmailer/phpmailer/src/OAuthTokenProvider.php
  - /axialy-production-ui/var/www/html/axialy-ui/vendor/phpmailer/phpmailer/src/PHPMailer.php
  - /axialy-production-ui/var/www/html/axialy-ui/vendor/phpmailer/phpmailer/src/POP3.php
  - /axialy-production-ui/var/www/html/axialy-ui/vendor/phpmailer/phpmailer/src/SMTP.php
  - /axialy-production-ui/var/www/html/axialy-ui/vendor/stripe/stripe-php/lib/...

Purpose:
This file is a generated PHP class used by the Composer autoloader. It provides a static, high-performance lookup table (class map and PSR-4 prefixes) to map namespaces and class names to their corresponding file paths within the `vendor` directory and the local `includes` directory. It is essential for the application to resolve and load dependencies like Stripe, PHPMailer, and the internal 'AxiaBA' namespace automatically without needing manual 'require' or 'include' statements.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/Mailer.php",
    "/axialy-production-ui/var/www/html/axialy-ui/vendor/composer/InstalledVersions.php",
    "/axialy-production-ui/var/www/html/axialy-ui/vendor/phpmailer/phpmailer/src/DSNConfigurator.php",
    "/axialy-production-ui/var/www/html/axialy-ui/vendor/phpmailer/phpmailer/src/Exception.php",
    "/axialy-production-ui/var/www/html/axialy-ui/vendor/phpmailer/phpmailer/src/OAuth.php",
    "/axialy-production-ui/var/www/html/axialy-ui/vendor/phpmailer/phpmailer/src/OAuthTokenProvider.php",
    "/axialy-production-ui/var/www/html/axialy-ui/vendor/phpmailer/phpmailer/src/PHPMailer.php",
    "/axialy-production-ui/var/www/html/axialy-ui/vendor/phpmailer/phpmailer/src/POP3.php",
    "/axialy-production-ui/var/www/html/axialy-ui/vendor/phpmailer/phpmailer/src/SMTP.php",
    "/axialy-production-ui/var/www/html/axialy-ui/vendor/stripe/stripe-php/lib/..."
  ],
  "purpose": "This file is a generated PHP class used by the Composer autoloader. It provides a static, high-performance lookup table (class map and PSR-4 prefixes) to map namespaces and class names to their corresponding file paths within the `vendor` directory and the local `includes` directory. It is essential for the application to resolve and load dependencies like Stripe, PHPMailer, and the internal 'AxiaBA' namespace automatically without needing manual 'require' or 'include' statements."
}
```

-------------------------------------------------
File #198
Path: /axialy-production-ui/var/www/html/axialy-ui/vendor/composer/ClassLoader.php

Referenced files:
  (none)

Purpose:
This file is a core component of the Composer dependency manager. It defines the `ClassLoader` class, which is responsible for automatically loading PHP classes, interfaces, and traits. It implements support for PSR-0, PSR-4, and classmap-based autoloading standards. By registering itself with the PHP SPL (Standard PHP Library) autoloader, it enables the application to dynamically locate and include file dependencies based on namespace conventions and class maps, effectively managing the loading of the project's 'vendor' directory.

Raw AI response:
```json
{
  "referenced_files": [],
  "purpose": "This file is a core component of the Composer dependency manager. It defines the `ClassLoader` class, which is responsible for automatically loading PHP classes, interfaces, and traits. It implements support for PSR-0, PSR-4, and classmap-based autoloading standards. By registering itself with the PHP SPL (Standard PHP Library) autoloader, it enables the application to dynamically locate and include file dependencies based on namespace conventions and class maps, effectively managing the loading of the project's 'vendor' directory."
}
```

-------------------------------------------------
File #199
Path: /axialy-production-ui/var/www/html/axialy-ui/vendor/composer/installed.json

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/vendor/phpmailer/phpmailer
  - /axialy-production-ui/var/www/html/axialy-ui/vendor/stripe/stripe-php

Purpose:
The `installed.json` file is a metadata file automatically generated by the Composer dependency manager. It serves as an inventory of all PHP packages installed in the project's `vendor/` directory. It provides the application with details about the currently installed versions, autoloader configurations, and installation paths for dependencies such as `phpmailer/phpmailer` (for email functionality) and `stripe/stripe-php` (for payment processing). This file is critical for the application's autoloader to map namespaces to the correct directory structures at runtime.

Raw AI response:
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/vendor/phpmailer/phpmailer",
    "/axialy-production-ui/var/www/html/axialy-ui/vendor/stripe/stripe-php"
  ],
  "purpose": "The `installed.json` file is a metadata file automatically generated by the Composer dependency manager. It serves as an inventory of all PHP packages installed in the project's `vendor/` directory. It provides the application with details about the currently installed versions, autoloader configurations, and installation paths for dependencies such as `phpmailer/phpmailer` (for email functionality) and `stripe/stripe-php` (for payment processing). This file is critical for the application's autoloader to map namespaces to the correct directory structures at runtime."
}

-------------------------------------------------
File #200
Path: /axialy-production-ui/var/www/html/axialy-ui/vendor/composer/installed.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/vendor/phpmailer/phpmailer
  - /axialy-production-ui/var/www/html/axialy-ui/vendor/stripe/stripe-php

Purpose:
This file is a generated Composer metadata file (installed.php) that acts as a registry for the project's dependencies. It maps installed PHP packages to their respective versions, types, and file system install paths, allowing the application to programmatically determine which dependencies are present and where they are located. It includes metadata for the core 'axialy/ui-product' project as well as third-party libraries like PHPMailer and Stripe.

Raw AI response:
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/vendor/phpmailer/phpmailer",
    "/axialy-production-ui/var/www/html/axialy-ui/vendor/stripe/stripe-php"
  ],
  "purpose": "This file is a generated Composer metadata file (installed.php) that acts as a registry for the project's dependencies. It maps installed PHP packages to their respective versions, types, and file system install paths, allowing the application to programmatically determine which dependencies are present and where they are located. It includes metadata for the core 'axialy/ui-product' project as well as third-party libraries like PHPMailer and Stripe."
}

-------------------------------------------------
File #201
Path: /axialy-production-ui/var/www/html/axialy-ui/vendor/composer/InstalledVersions.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/vendor/composer/installed.php

Purpose:
The `InstalledVersions.php` class is a core component of the Composer dependency manager's runtime API. Its primary purpose is to provide a programmatic, reliable way for an application to query information about its installed Composer packages, including versions, install paths, and references, at runtime. It functions by introspecting the `installed.php` file(s) generated during the composer install/update process and supports environments where multiple autoloaders might be active, ensuring that the package metadata remains accessible throughout the application lifecycle.

Raw AI response:
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/vendor/composer/installed.php"
  ],
  "purpose": "The `InstalledVersions.php` class is a core component of the Composer dependency manager's runtime API. Its primary purpose is to provide a programmatic, reliable way for an application to query information about its installed Composer packages, including versions, install paths, and references, at runtime. It functions by introspecting the `installed.php` file(s) generated during the composer install/update process and supports environments where multiple autoloaders might be active, ensuring that the package metadata remains accessible throughout the application lifecycle."
}

-------------------------------------------------
File #202
Path: /axialy-production-ui/var/www/html/axialy-ui/vendor/composer/platform_check.php

Referenced files:
  (none)

Purpose:
This file is an auto-generated script created by Composer during the dependency installation process. Its primary purpose is to perform a runtime environment validation, specifically ensuring that the server is running a PHP version compatible with the project's dependencies (in this case, PHP 7.4.0 or higher). If the platform requirements are not met, the script prevents the application from executing by throwing a RuntimeException and returning a 500 Internal Server Error, thereby ensuring system stability and preventing undefined behavior resulting from unsupported PHP features.

Raw AI response:
{
  "referenced_files": [],
  "purpose": "This file is an auto-generated script created by Composer during the dependency installation process. Its primary purpose is to perform a runtime environment validation, specifically ensuring that the server is running a PHP version compatible with the project's dependencies (in this case, PHP 7.4.0 or higher). If the platform requirements are not met, the script prevents the application from executing by throwing a RuntimeException and returning a 500 Internal Server Error, thereby ensuring system stability and preventing undefined behavior resulting from unsupported PHP features."
}

-------------------------------------------------
File #203
Path: /axialy-production-ui/var/www/html/axialy-ui/vendor/autoload.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/vendor/composer/autoload_real.php

Purpose:
This file serves as the primary entry point for the Composer-generated autoloader in the application. Its purpose is to verify the PHP environment version requirements, include the actual initialization logic contained in 'autoload_real.php', and trigger the class loader registration process, which enables PSR-0/PSR-4 compliant dependency loading for the project.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/vendor/composer/autoload_real.php"
  ],
  "purpose": "This file serves as the primary entry point for the Composer-generated autoloader in the application. Its purpose is to verify the PHP environment version requirements, include the actual initialization logic contained in 'autoload_real.php', and trigger the class loader registration process, which enables PSR-0/PSR-4 compliant dependency loading for the project."
}
```

-------------------------------------------------
File #204
Path: /axialy-production-ui/var/www/html/axialy-ui/vendor/README.md

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/vendor/autoload.php
  - /axialy-production-ui/var/www/html/axialy-ui/vendor/composer/ClassLoader.php
  - /axialy-production-ui/var/www/html/axialy-ui/vendor/composer/autoload_real.php
  - /axialy-production-ui/var/www/html/axialy-ui/vendor/composer/autoload_static.php
  - /axialy-production-ui/var/www/html/axialy-ui/vendor/composer/autoload_classmap.php
  - /axialy-production-ui/var/www/html/axialy-ui/vendor/composer/autoload_psr4.php
  - /axialy-production-ui/var/www/html/axialy-ui/vendor/composer/autoload_namespaces.php
  - /axialy-production-ui/var/www/html/axialy-ui/vendor/composer/installed.php
  - /axialy-production-ui/var/www/html/axialy-ui/vendor/composer/installed.json
  - /axialy-production-ui/var/www/html/axialy-ui/vendor/composer/platform_check.php
  - /axialy-production-ui/var/www/html/axialy-ui/vendor/composer/LICENSE
  - /axialy-production-ui/var/www/html/axialy-ui/vendor/stripe/init.php
  - /axialy-production-ui/var/www/html/axialy-ui/vendor/stripe/lib/
  - /axialy-production-ui/var/www/html/axialy-ui/vendor/stripe/composer.json

Purpose:
This file serves as internal documentation for the /vendor/ directory within the Axialy UI project. Its primary purpose is to outline the structure and function of third-party dependencies managed by Composer, specifically highlighting the autoloader configuration and the integrated Stripe PHP SDK.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/vendor/autoload.php",
    "/axialy-production-ui/var/www/html/axialy-ui/vendor/composer/ClassLoader.php",
    "/axialy-production-ui/var/www/html/axialy-ui/vendor/composer/autoload_real.php",
    "/axialy-production-ui/var/www/html/axialy-ui/vendor/composer/autoload_static.php",
    "/axialy-production-ui/var/www/html/axialy-ui/vendor/composer/autoload_classmap.php",
    "/axialy-production-ui/var/www/html/axialy-ui/vendor/composer/autoload_psr4.php",
    "/axialy-production-ui/var/www/html/axialy-ui/vendor/composer/autoload_namespaces.php",
    "/axialy-production-ui/var/www/html/axialy-ui/vendor/composer/installed.php",
    "/axialy-production-ui/var/www/html/axialy-ui/vendor/composer/installed.json",
    "/axialy-production-ui/var/www/html/axialy-ui/vendor/composer/platform_check.php",
    "/axialy-production-ui/var/www/html/axialy-ui/vendor/composer/LICENSE",
    "/axialy-production-ui/var/www/html/axialy-ui/vendor/stripe/init.php",
    "/axialy-production-ui/var/www/html/axialy-ui/vendor/stripe/lib/",
    "/axialy-production-ui/var/www/html/axialy-ui/vendor/stripe/composer.json"
  ],
  "purpose": "This file serves as internal documentation for the /vendor/ directory within the Axialy UI project. Its primary purpose is to outline the structure and function of third-party dependencies managed by Composer, specifically highlighting the autoloader configuration and the integrated Stripe PHP SDK."
}
```

-------------------------------------------------
File #205
Path: /axialy-production-ui/var/www/html/axialy-ui/webhooks/README.md

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/webhooks/.htaccess
  - /axialy-production-ui/var/www/html/axialy-ui/webhooks/stripe.php
  - /axialy-production-ui/var/www/html/axialy-ui/vendor/autoload.php

Purpose:
This file serves as technical documentation for the /webhooks/ directory. Its primary purpose is to outline the architecture for handling Stripe webhook events, detailing how incoming requests are routed via Apache rewrite rules, how payloads are validated and processed by the Stripe PHP SDK, and how the application synchronizes subscription states with the 'ui_users' database table.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/webhooks/.htaccess",
    "/axialy-production-ui/var/www/html/axialy-ui/webhooks/stripe.php",
    "/axialy-production-ui/var/www/html/axialy-ui/vendor/autoload.php"
  ],
  "purpose": "This file serves as technical documentation for the /webhooks/ directory. Its primary purpose is to outline the architecture for handling Stripe webhook events, detailing how incoming requests are routed via Apache rewrite rules, how payloads are validated and processed by the Stripe PHP SDK, and how the application synchronizes subscription states with the 'ui_users' database table."
}
```

-------------------------------------------------
File #206
Path: /axialy-production-ui/var/www/html/axialy-ui/webhooks/stripe.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/Config.php
  - /axialy-production-ui/var/www/html/axialy-ui/vendor/autoload.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php

Purpose:
This file acts as an endpoint to process asynchronous notifications (webhooks) sent by Stripe. It validates incoming request signatures using a secret, parses the payload, and performs necessary database updates to the 'ui_users' table based on subscription events (such as creation, deletion, status updates, and payment results) to keep the local system's subscription records in sync with Stripe. It relies on internal configuration and database connection files to perform these operations.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/Config.php",
    "/axialy-production-ui/var/www/html/axialy-ui/vendor/autoload.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php"
  ],
  "purpose": "This file acts as an endpoint to process asynchronous notifications (webhooks) sent by Stripe. It validates incoming request signatures using a secret, parses the payload, and performs necessary database updates to the 'ui_users' table based on subscription events (such as creation, deletion, status updates, and payment results) to keep the local system's subscription records in sync with Stripe. It relies on internal configuration and database connection files to perform these operations."
}
```

-------------------------------------------------
File #207
Path: /axialy-production-ui/var/www/html/axialy-ui/.env

Referenced files:
  (none)

Purpose:
This file is a standard environment configuration file (.env) used by the Axialy UI application. Its primary purpose is to centralize sensitive environment variables and connection strings, allowing the application to interface with various external services and infrastructure components without hardcoding these values into the source code. It provides critical configuration for the production environment, including database credentials (RDS), email provider settings (Postmark/Sendgrid), external API base URLs, AWS S3 storage settings, and Stripe payment integration parameters. The file also includes backward compatibility settings and application-specific metadata (version and environment name).

Raw AI response:
```json
{
  "referenced_files": [],
  "purpose": "This file is a standard environment configuration file (.env) used by the Axialy UI application. Its primary purpose is to centralize sensitive environment variables and connection strings, allowing the application to interface with various external services and infrastructure components without hardcoding these values into the source code. It provides critical configuration for the production environment, including database credentials (RDS), email provider settings (Postmark/Sendgrid), external API base URLs, AWS S3 storage settings, and Stripe payment integration parameters. The file also includes backward compatibility settings and application-specific metadata (version and environment name)."
}
```

-------------------------------------------------
File #208
Path: /axialy-production-ui/var/www/html/axialy-ui/.htaccess

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/sitemap.php

Purpose:
This .htaccess file serves as a server-level configuration for an Apache web server. Its primary function is to perform URL rewriting, specifically intercepting requests for 'sitemap.xml' and silently redirecting them to 'sitemap.php' to serve dynamic sitemap content while maintaining a static-looking URL structure.

Raw AI response:
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/sitemap.php"
  ],
  "purpose": "This .htaccess file serves as a server-level configuration for an Apache web server. Its primary function is to perform URL rewriting, specifically intercepting requests for 'sitemap.xml' and silently redirecting them to 'sitemap.php' to serve dynamic sitemap content while maintaining a static-looking URL structure."
}

-------------------------------------------------
File #209
Path: /axialy-production-ui/var/www/html/axialy-ui/accept_tos.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/auth.php
  - /login.php
  - /index.php
  - /assets/css/desktop.css
  - /docs/view_document.php

Purpose:
The purpose of this file is to enforce compliance with the current Terms of Service (ToS) for authenticated users. It checks if the active version of the 'tos' document in the database has been accepted by the currently logged-in user. If the user has not accepted the current version, it forces them to view the terms and interact with an acceptance checkbox before they are permitted to proceed to 'index.php'. It serves as a gatekeeper to ensure legal compliance without requiring an active subscription check.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/auth.php",
    "/login.php",
    "/index.php",
    "/assets/css/desktop.css",
    "/docs/view_document.php"
  ],
  "purpose": "The purpose of this file is to enforce compliance with the current Terms of Service (ToS) for authenticated users. It checks if the active version of the 'tos' document in the database has been accepted by the currently logged-in user. If the user has not accepted the current version, it forces them to view the terms and interact with an acceptance checkbox before they are permitted to proceed to 'index.php'. It serves as a gatekeeper to ensure legal compliance without requiring an active subscription check."
}
```

-------------------------------------------------
File #210
Path: /axialy-production-ui/var/www/html/axialy-ui/cancel_stakeholder_feedback_request.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/auth.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/debug_utils.php

Purpose:
This file serves as a backend API endpoint (handling POST requests) to cancel an existing stakeholder feedback request. It validates the user's session, ensures the requester has ownership of the feedback entry via database relation checks, and marks the feedback request as 'cancelled' by updating the record's token and timestamp. The file uses transaction management to ensure data integrity during the update process and logs the outcome for auditing purposes.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/auth.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/debug_utils.php"
  ],
  "purpose": "This file serves as a backend API endpoint (handling POST requests) to cancel an existing stakeholder feedback request. It validates the user's session, ensures the requester has ownership of the feedback entry via database relation checks, and marks the feedback request as 'cancelled' by updating the record's token and timestamp. The file uses transaction management to ensure data integrity during the update process and logs the outcome for auditing purposes."
}
```

-------------------------------------------------
File #211
Path: /axialy-production-ui/var/www/html/axialy-ui/check_deployed_mailer.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/Mailer.php

Purpose:
This file serves as a diagnostic debugging utility to verify the runtime configuration and behavior of the application's email subsystem. It allows developers to inspect current SMTP settings, evaluate the 'From' address logic (specifically identifying if the system is incorrectly using the SMTP username as the sender), and validate environment variable configuration. It includes a basic security gate requiring a 'debug' GET parameter to prevent unauthorized exposure of SMTP settings.

Raw AI response:
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/Mailer.php"
  ],
  "purpose": "This file serves as a diagnostic debugging utility to verify the runtime configuration and behavior of the application's email subsystem. It allows developers to inspect current SMTP settings, evaluate the 'From' address logic (specifically identifying if the system is incorrectly using the SMTP username as the sender), and validate environment variable configuration. It includes a basic security gate requiring a 'debug' GET parameter to prevent unauthorized exposure of SMTP settings."
}

-------------------------------------------------
File #212
Path: /axialy-production-ui/var/www/html/axialy-ui/check_error_logs.php

Referenced files:
  - /var/log/apache2/error.log
  - /var/log/httpd/error_log
  - /var/log/php_errors.log
  - /tmp/php_errors.log
  - /axialy-production-ui/var/www/html/axialy-ui/error.log
  - /axialy-production-ui/var/www/html/axialy-ui/php_errors.log

Purpose:
This file acts as a diagnostic utility for troubleshooting PHP application environments. It provides a web-accessible interface to verify current PHP configuration settings (such as error reporting and display status), inspect the most recent PHP error, read the final 20 lines of various common server/PHP error log paths, and verify that the application has the ability to write to the system's error log. Access to this diagnostic page is protected by a simple URL query parameter 'debug' with a hardcoded secret value.

Raw AI response:
```json
{
  "referenced_files": [
    "/var/log/apache2/error.log",
    "/var/log/httpd/error_log",
    "/var/log/php_errors.log",
    "/tmp/php_errors.log",
    "/axialy-production-ui/var/www/html/axialy-ui/error.log",
    "/axialy-production-ui/var/www/html/axialy-ui/php_errors.log"
  ],
  "purpose": "This file acts as a diagnostic utility for troubleshooting PHP application environments. It provides a web-accessible interface to verify current PHP configuration settings (such as error reporting and display status), inspect the most recent PHP error, read the final 20 lines of various common server/PHP error log paths, and verify that the application has the ability to write to the system's error log. Access to this diagnostic page is protected by a simple URL query parameter 'debug' with a hardcoded secret value."
}
```

-------------------------------------------------
File #213
Path: /axialy-production-ui/var/www/html/axialy-ui/check_file_versions.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/Mailer.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/account_creation.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/aws_ses_mailer.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/old_mailer.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/ses_mailer.php
  - /axialy-production-ui/var/www/html/axialy-ui/composer.lock
  - /axialy-production-ui/var/www/html/axialy-ui/vendor

Purpose:
This file serves as an administrative diagnostic utility used to verify the deployment status and versioning of critical application files. It inspects key files (such as Mailer.php and account_creation.php) for specific branding changes (AxiaBA to Axialy AI) and configuration updates (SMTP settings), identifies the presence of deprecated legacy files, and checks for the correct installation of PHP dependencies via Composer. Access to this output is gated by a simple shared-secret query parameter (?check=files123).

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/Mailer.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/account_creation.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/aws_ses_mailer.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/old_mailer.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/ses_mailer.php",
    "/axialy-production-ui/var/www/html/axialy-ui/composer.lock",
    "/axialy-production-ui/var/www/html/axialy-ui/vendor"
  ],
  "purpose": "This file serves as an administrative diagnostic utility used to verify the deployment status and versioning of critical application files. It inspects key files (such as Mailer.php and account_creation.php) for specific branding changes (AxiaBA to Axialy AI) and configuration updates (SMTP settings), identifies the presence of deprecated legacy files, and checks for the correct installation of PHP dependencies via Composer. Access to this output is gated by a simple shared-secret query parameter (?check=files123)."
}
```

-------------------------------------------------
File #214
Path: /axialy-production-ui/var/www/html/axialy-ui/cleanup_expired_tokens.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/debug_utils.php

Purpose:
This script acts as a maintenance utility to prune expired security tokens from the database. Specifically, it removes stale records from the 'password_resets' and 'email_verifications' tables where the expiration timestamp has passed. It is designed to be executed via a CLI cron job or triggered periodically to maintain database hygiene, and includes logging and error handling via the referenced utility files.

Raw AI response:
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/debug_utils.php"
  ],
  "purpose": "This script acts as a maintenance utility to prune expired security tokens from the database. Specifically, it removes stale records from the 'password_resets' and 'email_verifications' tables where the expiration timestamp has passed. It is designed to be executed via a CLI cron job or triggered periodically to maintain database hygiene, and includes logging and error handling via the referenced utility files."
}

-------------------------------------------------
File #215
Path: /axialy-production-ui/var/www/html/axialy-ui/clone_published_artifact.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/auth.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/debug_utils.php

Purpose:
This script provides an API endpoint to facilitate the duplication of existing 'published artifacts'. It retrieves an active artifact from the database by its ID, formats its existing data (title, description, and HTML content) into a structure compatible with the system's 'generate artifact' API, and returns this metadata as a JSON response. It is intended to be used as a front-end helper to allow users to create a new artifact based on the content of a previously published one.

Raw AI response:
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/auth.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/debug_utils.php"
  ],
  "purpose": "This script provides an API endpoint to facilitate the duplication of existing 'published artifacts'. It retrieves an active artifact from the database by its ID, formats its existing data (title, description, and HTML content) into a structure compatible with the system's 'generate artifact' API, and returns this metadata as a JSON response. It is intended to be used as a front-end helper to allow users to create a new artifact based on the content of a previously published one."
}

-------------------------------------------------
File #216
Path: /axialy-production-ui/var/www/html/axialy-ui/composer.json

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/

Purpose:
The `composer.json` file serves as the dependency management and project configuration file for the 'axialy/ui-product' web application. It defines the project's PHP runtime requirements (>=7.4), integrates third-party libraries for payment processing (Stripe) and email delivery (PHPMailer), and establishes the PSR-4 autoloading standard for the application's core codebase located in the 'includes/' directory. It also enforces build-time security and performance configurations, such as optimizing the autoloader and restricting plugin execution.

Raw AI response:
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/"
  ],
  "purpose": "The `composer.json` file serves as the dependency management and project configuration file for the 'axialy/ui-product' web application. It defines the project's PHP runtime requirements (>=7.4), integrates third-party libraries for payment processing (Stripe) and email delivery (PHPMailer), and establishes the PSR-4 autoloading standard for the application's core codebase located in the 'includes/' directory. It also enforces build-time security and performance configurations, such as optimizing the autoloader and restricting plugin execution."
}

-------------------------------------------------
File #217
Path: /axialy-production-ui/var/www/html/axialy-ui/content-review-form.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php
  - /axialy-production-ui/var/www/html/axialy-ui/assets/css/overlay.css
  - /axialy-production-ui/var/www/html/axialy-ui/assets/css/refine-tab.css

Purpose:
This file provides a public-facing web interface for users to submit feedback on specific content review requests. It validates a 'token' parameter from the URL to identify a pending review record in the 'content_reviews' database table. Once validated, it renders a form that, upon submission, updates the database with the user's feedback, marks the review as completed, and timestamps the entry.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php",
    "/axialy-production-ui/var/www/html/axialy-ui/assets/css/overlay.css",
    "/axialy-production-ui/var/www/html/axialy-ui/assets/css/refine-tab.css"
  ],
  "purpose": "This file provides a public-facing web interface for users to submit feedback on specific content review requests. It validates a 'token' parameter from the URL to identify a pending review record in the 'content_reviews' database table. Once validated, it renders a form that, upon submission, updates the database with the user's feedback, marks the review as completed, and timestamps the entry."
}
```

-------------------------------------------------
File #218
Path: /axialy-production-ui/var/www/html/axialy-ui/create-customer.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/Config.php
  - /axialy-production-ui/var/www/html/axialy-ui/vendor/autoload.php

Purpose:
The file serves as a server-side endpoint for creating new customers in Stripe. It handles incoming POST requests containing an email address, validates the input, initializes the Stripe client using configuration credentials retrieved from a custom Config class, and returns the newly created Stripe customer ID as a JSON response. Note that a secondary path to '/home/i17z4s936h3j/private_axiaba/includes/Config.php' is present in the code but commented out, indicating a legacy or alternative configuration path.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/Config.php",
    "/axialy-production-ui/var/www/html/axialy-ui/vendor/autoload.php"
  ],
  "purpose": "The file serves as a server-side endpoint for creating new customers in Stripe. It handles incoming POST requests containing an email address, validates the input, initializes the Stripe client using configuration credentials retrieved from a custom Config class, and returns the newly created Stripe customer ID as a JSON response. Note that a secondary path to '/home/i17z4s936h3j/private_axiaba/includes/Config.php' is present in the code but commented out, indicating a legacy or alternative configuration path."
}
```

-------------------------------------------------
File #219
Path: /axialy-production-ui/var/www/html/axialy-ui/create_custom_organization.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/auth.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/validation.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/debug_utils.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/Config.php

Purpose:
This file acts as a server-side API endpoint for creating new custom organization records. It performs user authentication, validates input data (including a file upload for an organization logo), securely uploads the logo to an S3-compatible cloud storage service using the AWS CLI, and persists the organization details into the database. The file outputs a JSON response indicating the success or failure of the creation process.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/auth.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/validation.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/debug_utils.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/Config.php"
  ],
  "purpose": "This file acts as a server-side API endpoint for creating new custom organization records. It performs user authentication, validates input data (including a file upload for an organization logo), securely uploads the logo to an S3-compatible cloud storage service using the AWS CLI, and persists the organization details into the database. The file outputs a JSON response indicating the success or failure of the creation process."
}
```

-------------------------------------------------
File #220
Path: /axialy-production-ui/var/www/html/axialy-ui/create_subscription.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/vendor/autoload.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/auth.php
  - /axialy-production-ui/var/www/html/axialy-ui/.env

Purpose:
This file acts as a backend API endpoint for processing user subscription and day-pass purchases via the Stripe payment gateway. It handles the secure authentication of users, initializes the Stripe SDK, and manages the logic for two specific transaction types: a one-time 24-hour day pass and a recurring monthly subscription with a 14-day free trial. Upon successful payment or subscription initiation, it updates the application database (`ui_users` table) to reflect the user's active status and plan details.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/vendor/autoload.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/auth.php",
    "/axialy-production-ui/var/www/html/axialy-ui/.env"
  ],
  "purpose": "This file acts as a backend API endpoint for processing user subscription and day-pass purchases via the Stripe payment gateway. It handles the secure authentication of users, initializes the Stripe SDK, and manages the logic for two specific transaction types: a one-time 24-hour day pass and a recurring monthly subscription with a 14-day free trial. Upon successful payment or subscription initiation, it updates the application database (`ui_users` table) to reflect the user's active status and plan details."
}
```

-------------------------------------------------
File #221
Path: /axialy-production-ui/var/www/html/axialy-ui/download_content_review_form.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/auth.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php
  - /serve_logo.php
  - /assets/img/rainbow-logo.png
  - /assets/img/product_logo.png

Purpose:
This file serves as a view-only, PDF-ready interface for displaying a stakeholder content review form. It fetches feedback request details (header information, focus area records, and stakeholder responses if available) from the database based on a provided 'request_id'. It dynamically renders the content, including organization-specific branding and sanitizing stored HTML content. The page also provides a 'Download as PDF' feature, which leverages the browser's native print functionality, triggered by the `downloadAsPDF()` JavaScript function.

Raw AI response:
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/auth.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php",
    "/serve_logo.php",
    "/assets/img/rainbow-logo.png",
    "/assets/img/product_logo.png"
  ],
  "purpose": "This file serves as a view-only, PDF-ready interface for displaying a stakeholder content review form. It fetches feedback request details (header information, focus area records, and stakeholder responses if available) from the database based on a provided 'request_id'. It dynamically renders the content, including organization-specific branding and sanitizing stored HTML content. The page also provides a 'Download as PDF' feature, which leverages the browser's native print functionality, triggered by the `downloadAsPDF()` JavaScript function."
}

-------------------------------------------------
File #222
Path: /axialy-production-ui/var/www/html/axialy-ui/favicon.ico

Referenced files:
  (none)

Purpose:
This file is the favicon for the Axialy Production UI system. It serves as the browser tab icon (shortcut icon) displayed to users when accessing the web interface.

Raw AI response:
{
  "referenced_files": [],
  "purpose": "This file is the favicon for the Axialy Production UI system. It serves as the browser tab icon (shortcut icon) displayed to users when accessing the web interface."
}

-------------------------------------------------
File #223
Path: /axialy-production-ui/var/www/html/axialy-ui/fetch_active_packages_for_save.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/auth.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/focus_org_session.php

Purpose:
This file serves as a backend API endpoint that returns a JSON-formatted list of active (non-deleted) analysis packages for a specific user. It filters results based on the user's default organization and their current 'focus' organization (managed via session state) to ensure that users only view packages relevant to their active context. This data is primarily used by the frontend to populate dropdowns or lists, allowing a user to select an existing package for updates.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/auth.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/focus_org_session.php"
  ],
  "purpose": "This file serves as a backend API endpoint that returns a JSON-formatted list of active (non-deleted) analysis packages for a specific user. It filters results based on the user's default organization and their current 'focus' organization (managed via session state) to ensure that users only view packages relevant to their active context. This data is primarily used by the frontend to populate dropdowns or lists, allowing a user to select an existing package for updates."
}
```

-------------------------------------------------
File #224
Path: /axialy-production-ui/var/www/html/axialy-ui/fetch_analysis_packages.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/focus_org_session.php

Purpose:
This file serves as a JSON API endpoint responsible for retrieving a list of analysis packages. It filters these packages based on the user's current organization context (default vs. custom) and an optional search term. It joins 'analysis_package_headers' with focus area and version tables to aggregate the most recent version number for each package, providing a concise dataset suitable for UI display components.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/focus_org_session.php"
  ],
  "purpose": "This file serves as a JSON API endpoint responsible for retrieving a list of analysis packages. It filters these packages based on the user's current organization context (default vs. custom) and an optional search term. It joins 'analysis_package_headers' with focus area and version tables to aggregate the most recent version number for each package, providing a concise dataset suitable for UI display components."
}
```

-------------------------------------------------
File #225
Path: /axialy-production-ui/var/www/html/axialy-ui/fetch_analysis_package_focus_areas_with_metrics.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/auth.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php

Purpose:
This script acts as a JSON API endpoint that retrieves the structure and content of an analysis package. It performs three main tasks: (1) fetches all 'focus areas' associated with a specific analysis package ID; (2) retrieves all associated records for those focus areas using a dynamic SQL IN clause; and (3) calculates the number of unreviewed stakeholder feedback entries (both general and itemized) for each focus area. The final output provides a comprehensive object containing focus area names, versioning information, associated records (including metadata and summarized input text), and the count of pending feedback.

Raw AI response:
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/auth.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php"
  ],
  "purpose": "This script acts as a JSON API endpoint that retrieves the structure and content of an analysis package. It performs three main tasks: (1) fetches all 'focus areas' associated with a specific analysis package ID; (2) retrieves all associated records for those focus areas using a dynamic SQL IN clause; and (3) calculates the number of unreviewed stakeholder feedback entries (both general and itemized) for each focus area. The final output provides a comprehensive object containing focus area names, versioning information, associated records (including metadata and summarized input text), and the count of pending feedback."
}

-------------------------------------------------
File #226
Path: /axialy-production-ui/var/www/html/axialy-ui/fetch_analysis_package_focus_area_records.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/auth.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php

Purpose:
This file functions as a backend API endpoint that retrieves structured data for analysis package focus areas and their associated records. It validates user authentication via '/includes/auth.php', establishes a database connection using '/includes/db_connection.php', and executes a multi-step query process: first, it identifies all focus areas linked to a provided 'package_id' and their current active versions; second, it fetches all corresponding data records for those versions from the database. Finally, it aggregates this data into a JSON response, including metadata such as properties, grid indices, and associated input text summaries, specifically formatted for consumption by the UI.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/auth.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php"
  ],
  "purpose": "This file functions as a backend API endpoint that retrieves structured data for analysis package focus areas and their associated records. It validates user authentication via '/includes/auth.php', establishes a database connection using '/includes/db_connection.php', and executes a multi-step query process: first, it identifies all focus areas linked to a provided 'package_id' and their current active versions; second, it fetches all corresponding data records for those versions from the database. Finally, it aggregates this data into a JSON response, including metadata such as properties, grid indices, and associated input text summaries, specifically formatted for consumption by the UI."
}
```

-------------------------------------------------
File #227
Path: /axialy-production-ui/var/www/html/axialy-ui/fetch_feedback_details.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php

Purpose:
This script acts as a JSON API endpoint to retrieve specific stakeholder feedback content. It processes requests based on either a single general feedback record ID or one or more comma-separated itemized feedback record IDs. It joins the relevant feedback tables (`stakeholder_general_feedback` or `stakeholder_itemized_feedback`) with the `stakeholder_feedback_headers` table to associate feedback text with the stakeholder's email, returning the result as a structured JSON response.

Raw AI response:
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php"
  ],
  "purpose": "This script acts as a JSON API endpoint to retrieve specific stakeholder feedback content. It processes requests based on either a single general feedback record ID or one or more comma-separated itemized feedback record IDs. It joins the relevant feedback tables (`stakeholder_general_feedback` or `stakeholder_itemized_feedback`) with the `stakeholder_feedback_headers` table to associate feedback text with the stakeholder's email, returning the result as a structured JSON response."
}

-------------------------------------------------
File #228
Path: /axialy-production-ui/var/www/html/axialy-ui/fetch_past_versions.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/auth.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php

Purpose:
This file serves as a JSON API endpoint designed to retrieve the historical version history of a specific 'focus area' associated with an analysis package. It validates user authentication, verifies the existence of the focus area within the database based on provided parameters (focus_area_name and package_id), and returns a list of all associated versions (including version numbers, revision summaries, and timestamps) sorted by version number in descending order.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/auth.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php"
  ],
  "purpose": "This file serves as a JSON API endpoint designed to retrieve the historical version history of a specific 'focus area' associated with an analysis package. It validates user authentication, verifies the existence of the focus area within the database based on provided parameters (focus_area_name and package_id), and returns a list of all associated versions (including version numbers, revision summaries, and timestamps) sorted by version number in descending order."
}
```

-------------------------------------------------
File #229
Path: /axialy-production-ui/var/www/html/axialy-ui/fetch_stakeholder_details.php

Referenced files:
  (none)

Purpose:
(not defined)

Raw AI response:
Please provide the content of the file `/axialy-production-ui/var/www/html/axialy-ui/fetch_stakeholder_details.php`. 

The "Content" field in your request was empty, so I am unable to analyze the specific implementation details, identify referenced files (such as database configuration files or utility classes), or describe the exact functional purpose. 

Once you provide the code, I will be able to return the requested JSON format immediately.

-------------------------------------------------
File #230
Path: /axialy-production-ui/var/www/html/axialy-ui/fetch_stakeholder_feedback.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php

Purpose:
The script serves as an API endpoint that aggregates unresolved stakeholder feedback for a specific analysis package and focus area. It retrieves two categories of feedback: 'general' (associated with the feedback header) and 'itemized' (associated with specific grid indices within a focus area). It also fetches the current version's configuration records (focus_area_records) to map feedback to the appropriate UI layout, ensuring compatibility with data structures where focus area associations might be null for certain versioned records.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php"
  ],
  "purpose": "The script serves as an API endpoint that aggregates unresolved stakeholder feedback for a specific analysis package and focus area. It retrieves two categories of feedback: 'general' (associated with the feedback header) and 'itemized' (associated with specific grid indices within a focus area). It also fetches the current version's configuration records (focus_area_records) to map feedback to the appropriate UI layout, ensuring compatibility with data structures where focus area associations might be null for certain versioned records."
}
```

-------------------------------------------------
File #231
Path: /axialy-production-ui/var/www/html/axialy-ui/fetch_stakeholder_profile_data.php

Referenced files:
  - /axialy-production-ui/var/www/html/includes/db_connection.php

Purpose:
This file serves as a JSON API endpoint designed to retrieve specific stakeholder profile information from the database based on a provided email address. It queries the 'stakeholder_feedback_headers' table to fetch personal and professional details (such as name, handle, company, and role) and returns the data as a JSON object, or an empty response if no match is found.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/includes/db_connection.php"
  ],
  "purpose": "This file serves as a JSON API endpoint designed to retrieve specific stakeholder profile information from the database based on a provided email address. It queries the 'stakeholder_feedback_headers' table to fetch personal and professional details (such as name, handle, company, and role) and returns the data as a JSON object, or an empty response if no match is found."
}
```

-------------------------------------------------
File #232
Path: /axialy-production-ui/var/www/html/axialy-ui/fetch_survey_feedback_details.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/auth.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php

Purpose:
The primary purpose of this script is to provide a JSON-formatted API endpoint that retrieves comprehensive details for a specific stakeholder feedback request. It fetches metadata from 'stakeholder_feedback_headers' (along with associated analysis package information), retrieves the structural records for the relevant focus area, and—if the stakeholder has already submitted feedback—joins and returns the specific general and itemized responses associated with that request ID. This data is intended to populate a UI component (likely a modal) in the dashboard to display the status and contents of a stakeholder's feedback.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/auth.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php"
  ],
  "purpose": "The primary purpose of this script is to provide a JSON-formatted API endpoint that retrieves comprehensive details for a specific stakeholder feedback request. It fetches metadata from 'stakeholder_feedback_headers' (along with associated analysis package information), retrieves the structural records for the relevant focus area, and—if the stakeholder has already submitted feedback—joins and returns the specific general and itemized responses associated with that request ID. This data is intended to populate a UI component (likely a modal) in the dashboard to display the status and contents of a stakeholder's feedback."
}
```

-------------------------------------------------
File #233
Path: /axialy-production-ui/var/www/html/axialy-ui/fetch_survey_feedback_details_responses.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/auth.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php

Purpose:
This file serves as a JSON API endpoint designed to retrieve detailed survey feedback responses from the database. It handles two specific types of feedback: 'general' feedback (text-based comments) and 'itemized' feedback (linked to specific grid indices). The script validates the user's session, queries the 'stakeholder_general_feedback' or 'stakeholder_itemized_feedback' tables based on the provided input parameters, and returns the aggregated results as a JSON-encoded response.

Raw AI response:
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/auth.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php"
  ],
  "purpose": "This file serves as a JSON API endpoint designed to retrieve detailed survey feedback responses from the database. It handles two specific types of feedback: 'general' feedback (text-based comments) and 'itemized' feedback (linked to specific grid indices). The script validates the user's session, queries the 'stakeholder_general_feedback' or 'stakeholder_itemized_feedback' tables based on the provided input parameters, and returns the aggregated results as a JSON-encoded response."
}

-------------------------------------------------
File #234
Path: /axialy-production-ui/var/www/html/axialy-ui/generate_publication_artifact.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/auth.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/debug_utils.php

Purpose:
This file serves as a backend API endpoint responsible for aggregating data related to a specific 'analysis package'. It retrieves the package header, associated organization details, and selected focus areas (including their specific version records) from the database. It processes these into a structured JSON format, combined with user-provided instructions, to prepare a dataset for the generation of a publication artifact. The file includes authentication checks and error handling for robust integration with the UI frontend.

Raw AI response:
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/auth.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/debug_utils.php"
  ],
  "purpose": "This file serves as a backend API endpoint responsible for aggregating data related to a specific 'analysis package'. It retrieves the package header, associated organization details, and selected focus areas (including their specific version records) from the database. It processes these into a structured JSON format, combined with user-provided instructions, to prepare a dataset for the generation of a publication artifact. The file includes authentication checks and error handling for robust integration with the UI frontend."
}

-------------------------------------------------
File #235
Path: /axialy-production-ui/var/www/html/axialy-ui/generate_publication_suggestions.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/auth.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/debug_utils.php

Purpose:
This file serves as a backend API endpoint that gathers and returns structured data for an analysis package to assist in generating publication suggestions. It fetches package headers, custom organization information, associated focus areas, and a sampling of records for those focus areas from the database. The resulting JSON payload is intended for consumption by a frontend JavaScript process that likely uses this information to interface with a generative AI or content-processing service.

Raw AI response:
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/auth.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/debug_utils.php"
  ],
  "purpose": "This file serves as a backend API endpoint that gathers and returns structured data for an analysis package to assist in generating publication suggestions. It fetches package headers, custom organization information, associated focus areas, and a sampling of records for those focus areas from the database. The resulting JSON payload is intended for consumption by a frontend JavaScript process that likely uses this information to interface with a generative AI or content-processing service."
}

-------------------------------------------------
File #236
Path: /axialy-production-ui/var/www/html/axialy-ui/get-refine-activities.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/config/refine-activities.json

Purpose:
This file serves as a JSON API endpoint that retrieves and filters configuration data for UI 'refine' activities. It reads a local configuration file (/config/refine-activities.json), extracts only those activities marked as active, and returns a sanitized JSON response containing the essential fields ('label', 'actionType', and 'action') for frontend consumption.

Raw AI response:
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/config/refine-activities.json"
  ],
  "purpose": "This file serves as a JSON API endpoint that retrieves and filters configuration data for UI 'refine' activities. It reads a local configuration file (/config/refine-activities.json), extracts only those activities marked as active, and returns a sanitized JSON response containing the essential fields ('label', 'actionType', and 'action') for frontend consumption."
}

-------------------------------------------------
File #237
Path: /axialy-production-ui/var/www/html/axialy-ui/get-stakeholders.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/data/stakeholders_<packageId>.json

Purpose:
This file acts as a server-side API endpoint that retrieves and processes stakeholder information for a specific package. It accepts a 'package_id' via a GET request, dynamically constructs the path to a corresponding JSON data file located in the '/data/' subdirectory, validates the existence and format of that file, and outputs a simplified JSON object containing only the 'email' and 'handle' fields for each stakeholder found.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/data/stakeholders_<packageId>.json"
  ],
  "purpose": "This file acts as a server-side API endpoint that retrieves and processes stakeholder information for a specific package. It accepts a 'package_id' via a GET request, dynamically constructs the path to a corresponding JSON data file located in the '/data/' subdirectory, validates the existence and format of that file, and outputs a simplified JSON object containing only the 'email' and 'handle' fields for each stakeholder found."
}
```

-------------------------------------------------
File #238
Path: /axialy-production-ui/var/www/html/axialy-ui/get_analysis_packages.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/auth.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/debug_utils.php

Purpose:
This file serves as a JSON API endpoint designed to fetch a filtered list of analysis packages for the currently authenticated user. It retrieves the user's default organization ID from the database and returns all associated 'analysis_package_headers' that contain at least one related entry in the 'stakeholder_feedback_headers' table. The script includes comprehensive error handling and internal logging, and relies on common utility files for database connectivity, session-based authentication, and debugging.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/auth.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/debug_utils.php"
  ],
  "purpose": "This file serves as a JSON API endpoint designed to fetch a filtered list of analysis packages for the currently authenticated user. It retrieves the user's default organization ID from the database and returns all associated 'analysis_package_headers' that contain at least one related entry in the 'stakeholder_feedback_headers' table. The script includes comprehensive error handling and internal logging, and relies on common utility files for database connectivity, session-based authentication, and debugging."
}
```

-------------------------------------------------
File #239
Path: /axialy-production-ui/var/www/html/axialy-ui/get_analysis_packages_for_publish.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/auth.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/focus_org_session.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/debug_utils.php

Purpose:
This file serves as a JSON API endpoint responsible for retrieving a list of 'analysis packages' associated with a specific organization. It validates the user's session and current 'focus organization', ensuring that a custom organization is selected before fetching package metadata (e.g., summary, description). It also aggregates various metrics for each package—including counts of focus areas, data records, feedback requests, responses, unique responding stakeholders, and pending (unreviewed) feedback—to provide a comprehensive summary of an analysis package's state for the UI.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/auth.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/focus_org_session.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/debug_utils.php"
  ],
  "purpose": "This file serves as a JSON API endpoint responsible for retrieving a list of 'analysis packages' associated with a specific organization. It validates the user's session and current 'focus organization', ensuring that a custom organization is selected before fetching package metadata (e.g., summary, description). It also aggregates various metrics for each package—including counts of focus areas, data records, feedback requests, responses, unique responding stakeholders, and pending (unreviewed) feedback—to provide a comprehensive summary of an analysis package's state for the UI."
}
```

-------------------------------------------------
File #240
Path: /axialy-production-ui/var/www/html/axialy-ui/get_custom_organizations.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/auth.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/debug_utils.php

Purpose:
This file serves as a JSON API endpoint responsible for retrieving a list of 'custom organizations' associated with the currently authenticated user. It fetches two sets of data: organizations owned by the user and additional organizations linked to the user's current session via analysis package headers. It handles authentication verification, performs database queries using PDO, merges and deduplicates the results, and returns the final list as a JSON response. Extensive debug logging is included to track the request lifecycle and query outcomes.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/auth.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/debug_utils.php"
  ],
  "purpose": "This file serves as a JSON API endpoint responsible for retrieving a list of 'custom organizations' associated with the currently authenticated user. It fetches two sets of data: organizations owned by the user and additional organizations linked to the user's current session via analysis package headers. It handles authentication verification, performs database queries using PDO, merges and deduplicates the results, and returns the final list as a JSON response. Extensive debug logging is included to track the request lifecycle and query outcomes."
}
```

-------------------------------------------------
File #241
Path: /axialy-production-ui/var/www/html/axialy-ui/get_dashboard_analysis_packages.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/auth.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/debug_utils.php

Purpose:
This file serves as a JSON API endpoint for the dashboard UI. Its primary purpose is to retrieve and return a list of unique 'analysis packages' (names and IDs) associated with the currently authenticated user's default organization. The logic specifically filters for packages that have at least one associated record in the 'stakeholder_feedback_headers' table, ensuring that only active or relevant packages are displayed to the user.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/auth.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/debug_utils.php"
  ],
  "purpose": "This file serves as a JSON API endpoint for the dashboard UI. Its primary purpose is to retrieve and return a list of unique 'analysis packages' (names and IDs) associated with the currently authenticated user's default organization. The logic specifically filters for packages that have at least one associated record in the 'stakeholder_feedback_headers' table, ensuring that only active or relevant packages are displayed to the user."
}
```

-------------------------------------------------
File #242
Path: /axialy-production-ui/var/www/html/axialy-ui/get_dashboard_custom_organizations.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/auth.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/debug_utils.php

Purpose:
This file serves as a JSON API endpoint responsible for retrieving a filtered list of 'Focus Organizations' for the authenticated user's dashboard. It determines the user's default organization and then queries the database for custom organizations that are associated with that default organization and contain at least one stakeholder feedback request. It includes built-in authentication validation via an external library and extensive logging for observability.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/auth.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/debug_utils.php"
  ],
  "purpose": "This file serves as a JSON API endpoint responsible for retrieving a filtered list of 'Focus Organizations' for the authenticated user's dashboard. It determines the user's default organization and then queries the database for custom organizations that are associated with that default organization and contain at least one stakeholder feedback request. It includes built-in authentication validation via an external library and extensive logging for observability."
}
```

-------------------------------------------------
File #243
Path: /axialy-production-ui/var/www/html/axialy-ui/get_dashboard_focus_areas.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/auth.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/debug_utils.php

Purpose:
This script acts as a backend API endpoint that provides a list of unique 'focus areas' for the authenticated user's default organization. It retrieves the user's organization ID from the database, then queries feedback data to identify distinct focus areas associated with that organization's analysis packages. The result is returned as a JSON object, with comprehensive logging and error handling provided via the referenced include files.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/auth.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/debug_utils.php"
  ],
  "purpose": "This script acts as a backend API endpoint that provides a list of unique 'focus areas' for the authenticated user's default organization. It retrieves the user's organization ID from the database, then queries feedback data to identify distinct focus areas associated with that organization's analysis packages. The result is returned as a JSON object, with comprehensive logging and error handling provided via the referenced include files."
}
```

-------------------------------------------------
File #244
Path: /axialy-production-ui/var/www/html/axialy-ui/get_dashboard_stakeholder_emails.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/auth.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/debug_utils.php

Purpose:
This script acts as a backend API endpoint that retrieves a unique list of stakeholder email addresses associated with the current user's default organization. It validates the user's session, queries the database to map the user to their organization, and then performs a JOIN query across the 'stakeholder_feedback_headers' and 'analysis_package_headers' tables to fetch relevant email data. The output is provided as a JSON response for use in the dashboard frontend, and the script includes detailed error logging and debugging functionality.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/auth.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/debug_utils.php"
  ],
  "purpose": "This script acts as a backend API endpoint that retrieves a unique list of stakeholder email addresses associated with the current user's default organization. It validates the user's session, queries the database to map the user to their organization, and then performs a JOIN query across the 'stakeholder_feedback_headers' and 'analysis_package_headers' tables to fetch relevant email data. The output is provided as a JSON response for use in the dashboard frontend, and the script includes detailed error logging and debugging functionality."
}
```

-------------------------------------------------
File #245
Path: /axialy-production-ui/var/www/html/axialy-ui/get_focus_organization.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/auth.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/debug_utils.php

Purpose:
This file serves as a JSON API endpoint responsible for retrieving the 'focus organization' currently assigned to an authenticated user. It validates the user's session, queries the `user_focus_organizations` database table to find their active organization ID, and returns the result as a JSON object. If no organization is explicitly set for the user, it defaults to returning 'default'.

Raw AI response:
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/auth.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/debug_utils.php"
  ],
  "purpose": "This file serves as a JSON API endpoint responsible for retrieving the 'focus organization' currently assigned to an authenticated user. It validates the user's session, queries the `user_focus_organizations` database table to find their active organization ID, and returns the result as a JSON object. If no organization is explicitly set for the user, it defaults to returning 'default'."
}

-------------------------------------------------
File #246
Path: /axialy-production-ui/var/www/html/axialy-ui/get_package_contributors.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/auth.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php

Purpose:
This script provides an API endpoint to retrieve a list of unique email addresses for stakeholders who have provided feedback on a specific analysis package. It validates user authentication, accepts a 'package_id' via JSON input, queries the database for records in 'stakeholder_feedback_headers' that have corresponding entries in either the 'stakeholder_general_feedback' or 'stakeholder_itemized_feedback' tables, and returns the result as a JSON object.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/auth.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php"
  ],
  "purpose": "This script provides an API endpoint to retrieve a list of unique email addresses for stakeholders who have provided feedback on a specific analysis package. It validates user authentication, accepts a 'package_id' via JSON input, queries the database for records in 'stakeholder_feedback_headers' that have corresponding entries in either the 'stakeholder_general_feedback' or 'stakeholder_itemized_feedback' tables, and returns the result as a JSON object."
}
```

-------------------------------------------------
File #247
Path: /axialy-production-ui/var/www/html/axialy-ui/get_package_data_for_revision.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/auth.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/debug_utils.php

Purpose:
This file serves as a backend API endpoint designed to retrieve the full configuration and content of an 'analysis package' for the purpose of creating a revision or clone. It validates user authentication, queries the database for the package header, associated focus areas, and the latest versions of records within those focus areas. The output is a structured JSON response containing the package summary and its nested focus area record properties.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/auth.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/debug_utils.php"
  ],
  "purpose": "This file serves as a backend API endpoint designed to retrieve the full configuration and content of an 'analysis package' for the purpose of creating a revision or clone. It validates user authentication, queries the database for the package header, associated focus areas, and the latest versions of records within those focus areas. The output is a structured JSON response containing the package summary and its nested focus area record properties."
}
```

-------------------------------------------------
File #248
Path: /axialy-production-ui/var/www/html/axialy-ui/get_package_focus_areas_for_publish.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/auth.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php

Purpose:
This file serves as a JSON API endpoint designed to retrieve a summary of 'focus areas' associated with a specific analysis package for the purpose of publishing. It validates user authentication, retrieves the focus areas linked to a provided 'package_id', and calculates metadata for each area—specifically the total count of records and a 3-record sample preview—before returning the aggregated data to the client-side UI.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/auth.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php"
  ],
  "purpose": "This file serves as a JSON API endpoint designed to retrieve a summary of 'focus areas' associated with a specific analysis package for the purpose of publishing. It validates user authentication, retrieves the focus areas linked to a provided 'package_id', and calculates metadata for each area—specifically the total count of records and a 3-record sample preview—before returning the aggregated data to the client-side UI."
}
```

-------------------------------------------------
File #249
Path: /axialy-production-ui/var/www/html/axialy-ui/get_package_stakeholders.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/auth.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/debug_utils.php

Purpose:
The file serves as a JSON API endpoint that retrieves a unique list of stakeholder email addresses associated with a specific 'Analysis Package'. It performs authentication checks, queries the database for records related to the 'Analysis Package Stakeholders' focus area, parses the 'properties' JSON field for an 'Email' key, and returns the deduplicated results.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/auth.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/debug_utils.php"
  ],
  "purpose": "The file serves as a JSON API endpoint that retrieves a unique list of stakeholder email addresses associated with a specific 'Analysis Package'. It performs authentication checks, queries the database for records related to the 'Analysis Package Stakeholders' focus area, parses the 'properties' JSON field for an 'Email' key, and returns the deduplicated results."
}
```

-------------------------------------------------
File #250
Path: /axialy-production-ui/var/www/html/axialy-ui/get_published_artifacts.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/auth.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/focus_org_session.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/debug_utils.php

Purpose:
This file serves as a JSON API endpoint that retrieves a list of active 'published artifacts' for a currently selected organization. It handles user authentication, validates the existence of a 'focus organization' session, executes a database query to join artifact data with analysis package and invitation metrics, and performs data processing (including calculating response rates, relative timestamps, and expiration status) before returning the results to the client.

Raw AI response:
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/auth.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/focus_org_session.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/debug_utils.php"
  ],
  "purpose": "This file serves as a JSON API endpoint that retrieves a list of active 'published artifacts' for a currently selected organization. It handles user authentication, validates the existence of a 'focus organization' session, executes a database query to join artifact data with analysis package and invitation metrics, and performs data processing (including calculating response rates, relative timestamps, and expiration status) before returning the results to the client."
}

-------------------------------------------------
File #251
Path: /axialy-production-ui/var/www/html/axialy-ui/get_stakeholder_emails.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/auth.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/debug_utils.php

Purpose:
This file serves as a backend API endpoint that returns a list of unique stakeholder email addresses associated with the current user's custom organizations. It authenticates the user, retrieves the organization IDs linked to their account, and queries the 'stakeholder_feedback_headers' and 'analysis_package_headers' tables to aggregate relevant emails. The final result is returned as a JSON object, with detailed logging enabled for debugging purposes.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/auth.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/debug_utils.php"
  ],
  "purpose": "This file serves as a backend API endpoint that returns a list of unique stakeholder email addresses associated with the current user's custom organizations. It authenticates the user, retrieves the organization IDs linked to their account, and queries the 'stakeholder_feedback_headers' and 'analysis_package_headers' tables to aggregate relevant emails. The final result is returned as a JSON object, with detailed logging enabled for debugging purposes."
}
```

-------------------------------------------------
File #252
Path: /axialy-production-ui/var/www/html/axialy-ui/get_stakeholder_feedback_requests.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/auth.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/debug_utils.php

Purpose:
This file acts as a backend API endpoint that retrieves paginated stakeholder feedback requests. It validates user authentication, filters feedback data based on organization and specific request parameters (email, analysis package, focus area, and response status), and returns the results as a JSON object, including aggregate counts of approval, revision, and skip actions for each request.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/auth.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/debug_utils.php"
  ],
  "purpose": "This file acts as a backend API endpoint that retrieves paginated stakeholder feedback requests. It validates user authentication, filters feedback data based on organization and specific request parameters (email, analysis package, focus area, and response status), and returns the results as a JSON object, including aggregate counts of approval, revision, and skip actions for each request."
}
```

-------------------------------------------------
File #253
Path: /axialy-production-ui/var/www/html/axialy-ui/get_survey_stakeholder_feedback_requests.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/auth.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/debug_utils.php

Purpose:
This script acts as a JSON API endpoint responsible for retrieving, filtering, and paginating stakeholder feedback records. It authenticates the user, determines their organizational scope, and executes complex database queries to aggregate feedback data (including detailed/categorical response counts and resolution status) from the `stakeholder_feedback_headers` table and related feedback tables. It returns the result set along with a total count for pagination purposes.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/auth.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/debug_utils.php"
  ],
  "purpose": "This script acts as a JSON API endpoint responsible for retrieving, filtering, and paginating stakeholder feedback records. It authenticates the user, determines their organizational scope, and executes complex database queries to aggregate feedback data (including detailed/categorical response counts and resolution status) from the `stakeholder_feedback_headers` table and related feedback tables. It returns the result set along with a total count for pagination purposes."
}
```

-------------------------------------------------
File #254
Path: /axialy-production-ui/var/www/html/axialy-ui/get_user_email.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/auth.php

Purpose:
This file serves as a backend API endpoint that retrieves the email address of the currently authenticated user. It validates the user's session, queries the 'ui_users' table using the 'user_id' stored in the session, and returns the result as a JSON object. Note that the file relies on 'includes/db_connection.php' for the database object ($pdo) and 'includes/auth.php' for session/authentication management, which are assumed to exist in the relative 'includes/' subdirectory.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/auth.php"
  ],
  "purpose": "This file serves as a backend API endpoint that retrieves the email address of the currently authenticated user. It validates the user's session, queries the 'ui_users' table using the 'user_id' stored in the session, and returns the result as a JSON object. Note that the file relies on 'includes/db_connection.php' for the database object ($pdo) and 'includes/auth.php' for session/authentication management, which are assumed to exist in the relative 'includes/' subdirectory."
}
```

-------------------------------------------------
File #255
Path: /axialy-production-ui/var/www/html/axialy-ui/health_check.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/.env
  - /axialy-production-ui/var/www/html/axialy-ui/vendor/autoload.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php

Purpose:
This file serves as a system health monitoring endpoint. It performs diagnostic checks on critical infrastructure dependencies—specifically the existence and configuration of the environment file (.env), connectivity to the Stripe API, the responsiveness of the database (via a PDO instance), and the availability of the Composer autoloader. It outputs the aggregated status in a JSON format and returns a 503 HTTP status code if any of these checks fail, facilitating automated system monitoring or load balancer health probes.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/.env",
    "/axialy-production-ui/var/www/html/axialy-ui/vendor/autoload.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php"
  ],
  "purpose": "This file serves as a system health monitoring endpoint. It performs diagnostic checks on critical infrastructure dependencies—specifically the existence and configuration of the environment file (.env), connectivity to the Stripe API, the responsiveness of the database (via a PDO instance), and the availability of the Composer autoloader. It outputs the aggregated status in a JSON format and returns a 503 HTTP status code if any of these checks fail, facilitating automated system monitoring or load balancer health probes."
}
```

-------------------------------------------------
File #256
Path: /axialy-production-ui/var/www/html/axialy-ui/index.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/auth.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/Config.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php
  - /axialy-production-ui/var/www/html/axialy-ui/config/control-panel-menu.json
  - /axialy-production-ui/var/www/html/axialy-ui/config/account-actions.json
  - /axialy-production-ui/var/www/html/axialy-ui/config/support-actions.json
  - /get_user_email.php

Purpose:
The index.php file serves as the main entry point and primary dashboard shell for the AxiaBA Business Analysis Platform. It handles user authentication, loads global application configurations, and dynamically generates the UI structure (header, control panel, and main container) based on server-side configuration files. It also serves as the host for the application's client-side environment, injecting necessary API credentials and loading the extensive suite of JavaScript modules and CSS stylesheets required to power the single-page-style application experience.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/auth.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/Config.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php",
    "/axialy-production-ui/var/www/html/axialy-ui/config/control-panel-menu.json",
    "/axialy-production-ui/var/www/html/axialy-ui/config/account-actions.json",
    "/axialy-production-ui/var/www/html/axialy-ui/config/support-actions.json",
    "/get_user_email.php"
  ],
  "purpose": "The index.php file serves as the main entry point and primary dashboard shell for the AxiaBA Business Analysis Platform. It handles user authentication, loads global application configurations, and dynamically generates the UI structure (header, control panel, and main container) based on server-side configuration files. It also serves as the host for the application's client-side environment, injecting necessary API credentials and loading the extensive suite of JavaScript modules and CSS stylesheets required to power the single-page-style application experience."
}
```

-------------------------------------------------
File #257
Path: /axialy-production-ui/var/www/html/axialy-ui/issue_ajax_actions.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/auth.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php

Purpose:
This file acts as a backend controller for AJAX-based support ticket operations. It enforces user authentication via `includes/auth.php`, establishes a database connection via `includes/db_connection.php`, and processes incoming requests for listing, viewing, and creating support tickets. The file handles the request routing through a switch statement and returns responses formatted as JSON.

Raw AI response:
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/auth.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php"
  ],
  "purpose": "This file acts as a backend controller for AJAX-based support ticket operations. It enforces user authentication via `includes/auth.php`, establishes a database connection via `includes/db_connection.php`, and processes incoming requests for listing, viewing, and creating support tickets. The file handles the request routing through a switch statement and returns responses formatted as JSON."
}

-------------------------------------------------
File #258
Path: /axialy-production-ui/var/www/html/axialy-ui/login.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/auth.php
  - /assets/css/desktop.css
  - /start_verification.php
  - /start_account_recovery.php

Purpose:
The login.php file serves as the primary authentication entry point for the Axialy UI. It handles user credentials via a POST request, interacts with the 'ui_users' and 'ui_user_sessions' database tables to validate identities, and manages PHP sessions. It also provides a frontend interface for users to sign in, request account creation, or initiate account recovery processes. Note that the file includes external assets and AJAX endpoints ('/start_verification.php' and '/start_account_recovery.php') which are not provided in the current context.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/auth.php",
    "/assets/css/desktop.css",
    "/start_verification.php",
    "/start_account_recovery.php"
  ],
  "purpose": "The login.php file serves as the primary authentication entry point for the Axialy UI. It handles user credentials via a POST request, interacts with the 'ui_users' and 'ui_user_sessions' database tables to validate identities, and manages PHP sessions. It also provides a frontend interface for users to sign in, request account creation, or initiate account recovery processes. Note that the file includes external assets and AJAX endpoints ('/start_verification.php' and '/start_account_recovery.php') which are not provided in the current context."
}
```

-------------------------------------------------
File #259
Path: /axialy-production-ui/var/www/html/axialy-ui/logout.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/debug_utils.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/auth.php
  - /axialy-production-ui/var/www/html/axialy-ui/login.php

Purpose:
The logout.php script manages the user session termination process for the Axialy UI. Its primary responsibilities include: 1) invalidating the user's session in the database by removing the 'ui' product session record associated with the user_id and session_token; 2) clearing PHP session variables and destroying the session object; 3) removing the session cookie from the client's browser; and 4) logging these actions via debug_utils for auditability. Finally, it redirects the user to the login page with a status parameter indicating either a successful logout or a handled error.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/debug_utils.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/auth.php",
    "/axialy-production-ui/var/www/html/axialy-ui/login.php"
  ],
  "purpose": "The logout.php script manages the user session termination process for the Axialy UI. Its primary responsibilities include: 1) invalidating the user's session in the database by removing the 'ui' product session record associated with the user_id and session_token; 2) clearing PHP session variables and destroying the session object; 3) removing the session cookie from the client's browser; and 4) logging these actions via debug_utils for auditability. Finally, it redirects the user to the login page with a status parameter indicating either a successful logout or a handled error."
}
```

-------------------------------------------------
File #260
Path: /axialy-production-ui/var/www/html/axialy-ui/log_errors.php

Referenced files:
  (none)

Purpose:
This file acts as a server-side endpoint for capturing and logging diagnostic messages sent via HTTP POST requests. It extracts a 'message' parameter from the request body and routes it to the system's internal PHP error logger (error_log), typically to assist in remote debugging or client-side error tracking. It returns a simple 'OK' response to confirm receipt of the payload.

Raw AI response:
{
  "referenced_files": [],
  "purpose": "This file acts as a server-side endpoint for capturing and logging diagnostic messages sent via HTTP POST requests. It extracts a 'message' parameter from the request body and routes it to the system's internal PHP error logger (error_log), typically to assist in remote debugging or client-side error tracking. It returns a simple 'OK' response to confirm receipt of the payload."
}

-------------------------------------------------
File #261
Path: /axialy-production-ui/var/www/html/axialy-ui/manage-subscription.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/Config.php
  - /axialy-production-ui/var/www/html/axialy-ui/vendor/autoload.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/auth.php
  - /axialy-production-ui/var/www/html/axialy-ui/login.php
  - /axialy-production-ui/var/www/html/axialy-ui/subscription.php
  - /axialy-production-ui/var/www/html/axialy-ui/assets/css/account-modal.css

Purpose:
The file `manage-subscription.php` acts as a user dashboard for managing account subscriptions. It retrieves and displays the current subscription status (e.g., Monthly, Promo, or Day Pass), handles subscription cancellations via the Stripe API, and provides UI elements for users to monitor their billing period or expiration dates. The file includes logic to interact with the database to update subscription states and includes a cancellation modal mechanism.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/Config.php",
    "/axialy-production-ui/var/www/html/axialy-ui/vendor/autoload.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/auth.php",
    "/axialy-production-ui/var/www/html/axialy-ui/login.php",
    "/axialy-production-ui/var/www/html/axialy-ui/subscription.php",
    "/axialy-production-ui/var/www/html/axialy-ui/assets/css/account-modal.css"
  ],
  "purpose": "The file `manage-subscription.php` acts as a user dashboard for managing account subscriptions. It retrieves and displays the current subscription status (e.g., Monthly, Promo, or Day Pass), handles subscription cancellations via the Stripe API, and provides UI elements for users to monitor their billing period or expiration dates. The file includes logic to interact with the database to update subscription states and includes a cancellation modal mechanism."
}
```

-------------------------------------------------
File #262
Path: /axialy-production-ui/var/www/html/axialy-ui/mirror_start_verification.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/account_creation.php

Purpose:
This file serves as a debugging and diagnostic mirror of the production `start_verification.php` script. It replicates the exact email verification flow—validating input, checking for existing accounts, creating tokens, and attempting to send verification emails—while providing detailed JSON-encoded debugging output at every stage of the execution. It includes a basic hardcoded security check to ensure it can only be triggered by authorized users.

Raw AI response:
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/account_creation.php"
  ],
  "purpose": "This file serves as a debugging and diagnostic mirror of the production `start_verification.php` script. It replicates the exact email verification flow—validating input, checking for existing accounts, creating tokens, and attempting to send verification emails—while providing detailed JSON-encoded debugging output at every stage of the execution. It includes a basic hardcoded security check to ensure it can only be triggered by authorized users."
}

-------------------------------------------------
File #263
Path: /axialy-production-ui/var/www/html/axialy-ui/php.ini

Referenced files:
  - /home/i17z4s936h3j/public_html/app.axialy.ai/php/ext
  - /tmp
  - /home/i17z4s936h3j/public_html/certs/cacert.pem
  - /usr/lib/php
  - /usr/local/lib/php

Purpose:
This file is the primary configuration file (php.ini) for the PHP runtime environment used by the axialy-ui application. It defines global system settings, including resource limits (memory/execution time), error logging levels, directory paths for extensions and temporary files, session management parameters, and security-related SSL certificate configurations for CURL and OpenSSL. It also explicitly loads necessary PHP extensions (e.g., mysqli, pdo_mysql, curl) to support database connectivity and web communication.

Raw AI response:
{
  "referenced_files": [
    "/home/i17z4s936h3j/public_html/app.axialy.ai/php/ext",
    "/tmp",
    "/home/i17z4s936h3j/public_html/certs/cacert.pem",
    "/usr/lib/php",
    "/usr/local/lib/php"
  ],
  "purpose": "This file is the primary configuration file (php.ini) for the PHP runtime environment used by the axialy-ui application. It defines global system settings, including resource limits (memory/execution time), error logging levels, directory paths for extensions and temporary files, session management parameters, and security-related SSL certificate configurations for CURL and OpenSSL. It also explicitly loads necessary PHP extensions (e.g., mysqli, pdo_mysql, curl) to support database connectivity and web communication."
}

-------------------------------------------------
File #264
Path: /axialy-production-ui/var/www/html/axialy-ui/process_content_review_request.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/validation.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/debug_utils.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/Mailer.php
  - /axialy-production-ui/var/www/html/axialy-ui/receive_stakeholder_feedback.php

Purpose:
This script acts as an API endpoint to process content review requests. It receives JSON input containing stakeholder email addresses, package metadata, and feedback configuration. It persists these requests into the `stakeholder_feedback_headers` database table (generating a secure token and PIN for each recipient) and then triggers an email to each stakeholder via the `Mailer` class. The emails include custom, branded HTML templates that provide the recipient with a link to `receive_stakeholder_feedback.php` and their unique access PIN to participate in the review process.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/validation.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/debug_utils.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/Mailer.php",
    "/axialy-production-ui/var/www/html/axialy-ui/receive_stakeholder_feedback.php"
  ],
  "purpose": "This script acts as an API endpoint to process content review requests. It receives JSON input containing stakeholder email addresses, package metadata, and feedback configuration. It persists these requests into the `stakeholder_feedback_headers` database table (generating a secure token and PIN for each recipient) and then triggers an email to each stakeholder via the `Mailer` class. The emails include custom, branded HTML templates that provide the recipient with a link to `receive_stakeholder_feedback.php` and their unique access PIN to participate in the review process."
}
```

-------------------------------------------------
File #265
Path: /axialy-production-ui/var/www/html/axialy-ui/process_content_revision.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php

Purpose:
This script handles the manual revisioning process for specific 'focus areas' within an analysis package. It acts as an API endpoint (accepting POST requests with JSON payloads) to create a new version of a focus area by copying existing record data (including display order) into a new version entry in the database. It then applies user-submitted updates, deletions, or additions to these records and finally updates the primary focus area record to point to the newly created version. This ensures auditability and version control for content changes within the analysis package.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php"
  ],
  "purpose": "This script handles the manual revisioning process for specific 'focus areas' within an analysis package. It acts as an API endpoint (accepting POST requests with JSON payloads) to create a new version of a focus area by copying existing record data (including display order) into a new version entry in the database. It then applies user-submitted updates, deletions, or additions to these records and finally updates the primary focus area record to point to the newly created version. This ensures auditability and version control for content changes within the analysis package."
}
```

-------------------------------------------------
File #266
Path: /axialy-production-ui/var/www/html/axialy-ui/process_delete_focus_area_data.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php

Purpose:
The primary purpose of this script is to handle the secure deletion of a 'focus area' within an analysis package. It follows a transactional workflow to ensure data integrity: it verifies current version concurrency, increments the version number for the focus area, creates a revision record logging the deletion, marks the focus area as deleted in the database, and preserves the historical state of the focus area's records by copying them into the new version marked as 'deleted'. This prevents hard deletion of historical data while effectively removing the item from active use.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php"
  ],
  "purpose": "The primary purpose of this script is to handle the secure deletion of a 'focus area' within an analysis package. It follows a transactional workflow to ensure data integrity: it verifies current version concurrency, increments the version number for the focus area, creates a revision record logging the deletion, marks the focus area as deleted in the database, and preserves the historical state of the focus area's records by copying them into the new version marked as 'deleted'. This prevents hard deletion of historical data while effectively removing the item from active use."
}
```

-------------------------------------------------
File #267
Path: /axialy-production-ui/var/www/html/axialy-ui/process_html_for_publication.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/auth.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/html_sanitizer.php

Purpose:
The primary purpose of this file is to serve as an authenticated API endpoint that processes raw HTML content for publication. It sanitizes the input HTML based on specific security and interactivity requirements (allowing or stripping JavaScript and CSS) and returns a JSON response containing the processed HTML, metadata (extracted title), a content summary, and a structural analysis of the document.

Raw AI response:
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/auth.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/html_sanitizer.php"
  ],
  "purpose": "The primary purpose of this file is to serve as an authenticated API endpoint that processes raw HTML content for publication. It sanitizes the input HTML based on specific security and interactivity requirements (allowing or stripping JavaScript and CSS) and returns a JSON response containing the processed HTML, metadata (extracted title), a content summary, and a structural analysis of the document."
}

-------------------------------------------------
File #268
Path: /axialy-production-ui/var/www/html/axialy-ui/process_new_focus_area.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php

Purpose:
This file serves as a backend API endpoint that processes HTTP POST requests to create a new 'Focus Area' within an existing analysis package. It performs data validation, verifies the parent package's existence, and executes a multi-step database transaction: creating the focus area record, initializing the first version (version 0), linking the current version to the new focus area, and inserting the associated data records into the database. It returns a JSON response indicating success or providing an error message if the operation fails.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php"
  ],
  "purpose": "This file serves as a backend API endpoint that processes HTTP POST requests to create a new 'Focus Area' within an existing analysis package. It performs data validation, verifies the parent package's existence, and executes a multi-step database transaction: creating the focus area record, initializing the first version (version 0), linking the current version to the new focus area, and inserting the associated data records into the database. It returns a JSON response indicating success or providing an error message if the operation fails."
}
```

-------------------------------------------------
File #269
Path: /axialy-production-ui/var/www/html/axialy-ui/process_new_focus_area_enhanced.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php

Purpose:
This file serves as a server-side API endpoint designed to ingest and store AI-generated 'focus area' data within an analysis package. It performs data validation, checks for duplicate naming, and executes a multi-step database transaction to create a new focus area record, initialize its first version, and populate associated records (such as grid data and stakeholder metadata). The script is specifically enhanced to handle additional fields like 'focus_area_value' and 'collaboration_approach' typically provided by an AI assistant interface.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php"
  ],
  "purpose": "This file serves as a server-side API endpoint designed to ingest and store AI-generated 'focus area' data within an analysis package. It performs data validation, checks for duplicate naming, and executes a multi-step database transaction to create a new focus area record, initialize its first version, and populate associated records (such as grid data and stakeholder metadata). The script is specifically enhanced to handle additional fields like 'focus_area_value' and 'collaboration_approach' typically provided by an AI assistant interface."
}
```

-------------------------------------------------
File #270
Path: /axialy-production-ui/var/www/html/axialy-ui/process_recover_focus_area.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/auth.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php

Purpose:
This script handles the 'recovery' of a specific version of a focus area within an analysis package. It functions as an API endpoint that receives a JSON payload identifying a target focus area and a previous version number. It then creates a new version entry by copying the data records from the specified historical version, effectively promoting that historical state to the 'current' version. It also includes logic to restore the focus area to an active state (is_deleted = 0) if it was previously soft-deleted.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/auth.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php"
  ],
  "purpose": "This script handles the 'recovery' of a specific version of a focus area within an analysis package. It functions as an API endpoint that receives a JSON payload identifying a target focus area and a previous version number. It then creates a new version entry by copying the data records from the specified historical version, effectively promoting that historical state to the 'current' version. It also includes logic to restore the focus area to an active state (is_deleted = 0) if it was previously soft-deleted."
}
```

-------------------------------------------------
File #271
Path: /axialy-production-ui/var/www/html/axialy-ui/publish_artifact.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/auth.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/debug_utils.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/Config.php

Purpose:
This file serves as a backend API endpoint for publishing analysis artifacts. It validates user authentication, processes incoming JSON request data (such as HTML content, package IDs, and optional expiry dates), and creates a new entry in the 'published_artifacts' database table. It includes a deduplication mechanism to prevent redundant database entries within a 5-minute window. Notably, it explicitly decouples the artifact publication from stakeholder notification processes, deferring email invitations to a separate, subsequent step.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/auth.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/debug_utils.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/Config.php"
  ],
  "purpose": "This file serves as a backend API endpoint for publishing analysis artifacts. It validates user authentication, processes incoming JSON request data (such as HTML content, package IDs, and optional expiry dates), and creates a new entry in the 'published_artifacts' database table. It includes a deduplication mechanism to prevent redundant database entries within a 5-minute window. Notably, it explicitly decouples the artifact publication from stakeholder notification processes, deferring email invitations to a separate, subsequent step."
}
```

-------------------------------------------------
File #272
Path: /axialy-production-ui/var/www/html/axialy-ui/README.md

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/accepts_tos.php
  - /axialy-production-ui/var/www/html/axialy-ui/index.php
  - /axialy-production-ui/var/www/html/axialy-ui/login.php
  - /axialy-production-ui/var/www/html/axialy-ui/logout.php
  - /axialy-production-ui/var/www/html/axialy-ui/user-documentation.php
  - /axialy-production-ui/var/www/html/axialy-ui/subscription.php
  - /axialy-production-ui/var/www/html/axialy-ui/config/control-panel-menu.json
  - /axialy-production-ui/var/www/html/axialy-ui/config/account-actions.json
  - /axialy-production-ui/var/www/html/axialy-ui/config/support-actions.json
  - /axialy-production-ui/var/www/html/axialy-ui/assets/css/
  - /axialy-production-ui/var/www/html/axialy-ui/assets/img/
  - /axialy-production-ui/var/www/html/axialy-ui/js/
  - /axialy-production-ui/var/www/html/axialy-ui/vendor/
  - /axialy-production-ui/var/www/html/axialy-ui/includes/
  - /axialy-production-ui/var/www/html/axialy-ui/data/
  - /axialy-production-ui/var/www/html/axialy-ui/process_content_review_request.php
  - /axialy-production-ui/var/www/html/axialy-ui/process_content_revision.php
  - /axialy-production-ui/var/www/html/axialy-ui/process_delete_focus_area_data.php
  - /axialy-production-ui/var/www/html/axialy-ui/process_new_focus_area.php
  - /axialy-production-ui/var/www/html/axialy-ui/process_recover_focus_area.php
  - /axialy-production-ui/var/www/html/axialy-ui/save_analysis_package.php
  - /axialy-production-ui/var/www/html/axialy-ui/save_data_existing_package.php
  - /axialy-production-ui/var/www/html/axialy-ui/remove_analysis_package.php
  - /axialy-production-ui/var/www/html/axialy-ui/recover_analysis_package.php
  - /axialy-production-ui/var/www/html/axialy-ui/update_analysis_package.php
  - /axialy-production-ui/var/www/html/axialy-ui/save_enhanced_records.php
  - /axialy-production-ui/var/www/html/axialy-ui/save_revised_records.php
  - /axialy-production-ui/var/www/html/axialy-ui/store_feedback_data.php
  - /axialy-production-ui/var/www/html/axialy-ui/store_summary.php
  - /axialy-production-ui/var/www/html/axialy-ui/store_analysis_package_focus_area_version.php
  - /axialy-production-ui/var/www/html/axialy-ui/store_analysis_package_header.php
  - /axialy-production-ui/var/www/html/axialy-ui/redeem_promo_code.php
  - /axialy-production-ui/var/www/html/axialy-ui/webhook.php
  - /axialy-production-ui/var/www/html/axialy-ui/start_verification.php
  - /axialy-production-ui/var/www/html/axialy-ui/verify_email.php
  - /axialy-production-ui/var/www/html/axialy-ui/update_custom_organization.php
  - /axialy-production-ui/var/www/html/axialy-ui/update_focus_organization.php
  - /axialy-production-ui/var/www/html/axialy-ui/serve_logo.php
  - /axialy-production-ui/var/www/html/axialy-ui/submit_issue.php
  - /axialy-production-ui/var/www/html/axialy-ui/view_document.php
  - /axialy-production-ui/var/www/html/axialy-ui/receive_stakeholder_feedback.php
  - /axialy-production-ui/var/www/html/axialy-ui/submit_content_review.php
  - /axialy-production-ui/var/www/html/axialy-ui/send_content_review_emails.php
  - /axialy-production-ui/var/www/html/axialy-ui/php.ini
  - /axialy-production-ui/var/www/html/axialy-ui/includes/Config.php

Purpose:
The README.md serves as the primary documentation for the Axialy UI front-end application. It outlines the system's architecture, setup requirements (PHP 7.4+, MySQL, Composer), feature set (analysis packages, stakeholder feedback, Stripe subscriptions), and the directory structure necessary for developers to deploy and maintain the web interface for the Axia Business Analysis platform.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/accepts_tos.php",
    "/axialy-production-ui/var/www/html/axialy-ui/index.php",
    "/axialy-production-ui/var/www/html/axialy-ui/login.php",
    "/axialy-production-ui/var/www/html/axialy-ui/logout.php",
    "/axialy-production-ui/var/www/html/axialy-ui/user-documentation.php",
    "/axialy-production-ui/var/www/html/axialy-ui/subscription.php",
    "/axialy-production-ui/var/www/html/axialy-ui/config/control-panel-menu.json",
    "/axialy-production-ui/var/www/html/axialy-ui/config/account-actions.json",
    "/axialy-production-ui/var/www/html/axialy-ui/config/support-actions.json",
    "/axialy-production-ui/var/www/html/axialy-ui/assets/css/",
    "/axialy-production-ui/var/www/html/axialy-ui/assets/img/",
    "/axialy-production-ui/var/www/html/axialy-ui/js/",
    "/axialy-production-ui/var/www/html/axialy-ui/vendor/",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/",
    "/axialy-production-ui/var/www/html/axialy-ui/data/",
    "/axialy-production-ui/var/www/html/axialy-ui/process_content_review_request.php",
    "/axialy-production-ui/var/www/html/axialy-ui/process_content_revision.php",
    "/axialy-production-ui/var/www/html/axialy-ui/process_delete_focus_area_data.php",
    "/axialy-production-ui/var/www/html/axialy-ui/process_new_focus_area.php",
    "/axialy-production-ui/var/www/html/axialy-ui/process_recover_focus_area.php",
    "/axialy-production-ui/var/www/html/axialy-ui/save_analysis_package.php",
    "/axialy-production-ui/var/www/html/axialy-ui/save_data_existing_package.php",
    "/axialy-production-ui/var/www/html/axialy-ui/remove_analysis_package.php",
    "/axialy-production-ui/var/www/html/axialy-ui/recover_analysis_package.php",
    "/axialy-production-ui/var/www/html/axialy-ui/update_analysis_package.php",
    "/axialy-production-ui/var/www/html/axialy-ui/save_enhanced_records.php",
    "/axialy-production-ui/var/www/html/axialy-ui/save_revised_records.php",
    "/axialy-production-ui/var/www/html/axialy-ui/store_feedback_data.php",
    "/axialy-production-ui/var/www/html/axialy-ui/store_summary.php",
    "/axialy-production-ui/var/www/html/axialy-ui/store_analysis_package_focus_area_version.php",
    "/axialy-production-ui/var/www/html/axialy-ui/store_analysis_package_header.php",
    "/axialy-production-ui/var/www/html/axialy-ui/redeem_promo_code.php",
    "/axialy-production-ui/var/www/html/axialy-ui/webhook.php",
    "/axialy-production-ui/var/www/html/axialy-ui/start_verification.php",
    "/axialy-production-ui/var/www/html/axialy-ui/verify_email.php",
    "/axialy-production-ui/var/www/html/axialy-ui/update_custom_organization.php",
    "/axialy-production-ui/var/www/html/axialy-ui/update_focus_organization.php",
    "/axialy-production-ui/var/www/html/axialy-ui/serve_logo.php",
    "/axialy-production-ui/var/www/html/axialy-ui/submit_issue.php",
    "/axialy-production-ui/var/www/html/axialy-ui/view_document.php",
    "/axialy-production-ui/var/www/html/axialy-ui/receive_stakeholder_feedback.php",
    "/axialy-production-ui/var/www/html/axialy-ui/submit_content_review.php",
    "/axialy-production-ui/var/www/html/axialy-ui/send_content_review_emails.php",
    "/axialy-production-ui/var/www/html/axialy-ui/php.ini",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/Config.php"
  ],
  "purpose": "The README.md serves as the primary documentation for the Axialy UI front-end application. It outlines the system's architecture, setup requirements (PHP 7.4+, MySQL, Composer), feature set (analysis packages, stakeholder feedback, Stripe subscriptions), and the directory structure necessary for developers to deploy and maintain the web interface for the Axia Business Analysis platform."
}
```

-------------------------------------------------
File #273
Path: /axialy-production-ui/var/www/html/axialy-ui/receive_stakeholder_feedback.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php
  - /assets/css/stakeholder-content-review.css
  - /stakeholder-feedback/stakeholder-content-review.php
  - /stakeholder-feedback/feedback-confirmation.php

Purpose:
This file serves as a secure gateway for stakeholders to access their feedback forms. It verifies a 4-digit PIN associated with a unique access token provided via URL. Upon successful validation, it establishes a user session, records an entry in the 'stakeholder_sessions' database table for audit/tracking, and redirects the user to the content review interface. It also provides basic UI for inputting the PIN and retrieves package metadata to confirm the context of the feedback request.

Raw AI response:
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php",
    "/assets/css/stakeholder-content-review.css",
    "/stakeholder-feedback/stakeholder-content-review.php",
    "/stakeholder-feedback/feedback-confirmation.php"
  ],
  "purpose": "This file serves as a secure gateway for stakeholders to access their feedback forms. It verifies a 4-digit PIN associated with a unique access token provided via URL. Upon successful validation, it establishes a user session, records an entry in the 'stakeholder_sessions' database table for audit/tracking, and redirects the user to the content review interface. It also provides basic UI for inputting the PIN and retrieves package metadata to confirm the context of the feedback request."
}

-------------------------------------------------
File #274
Path: /axialy-production-ui/var/www/html/axialy-ui/recover_analysis_package.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/auth.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php

Purpose:
This file serves as a backend API endpoint designed to restore 'soft-deleted' analysis packages. It validates the user's session via an authentication include, parses a JSON request body to obtain a 'package_id', and performs a database update on the 'analysis_package_headers' table to set the 'is_deleted' column to 0. It returns a JSON response indicating whether the recovery was successful or if an error occurred.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/auth.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php"
  ],
  "purpose": "This file serves as a backend API endpoint designed to restore 'soft-deleted' analysis packages. It validates the user's session via an authentication include, parses a JSON request body to obtain a 'package_id', and performs a database update on the 'analysis_package_headers' table to set the 'is_deleted' column to 0. It returns a JSON response indicating whether the recovery was successful or if an error occurred."
}
```

-------------------------------------------------
File #275
Path: /axialy-production-ui/var/www/html/axialy-ui/redeem_promo_code.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/auth.php

Purpose:
This file serves as a backend API endpoint for processing user promo code redemptions. It validates the promo code against a database table (`promo_codes`), checks for expiration, usage limits, and user-specific redemption history. Upon validation, it updates the current user's subscription status in the `ui_users` table (either setting an 'unlimited' status or a limited trial period), records the transaction in `promo_code_redemptions`, and increments the global usage count for that promo code. It also handles conditional statement acceptance requirements required by certain promo codes.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/auth.php"
  ],
  "purpose": "This file serves as a backend API endpoint for processing user promo code redemptions. It validates the promo code against a database table (`promo_codes`), checks for expiration, usage limits, and user-specific redemption history. Upon validation, it updates the current user's subscription status in the `ui_users` table (either setting an 'unlimited' status or a limited trial period), records the transaction in `promo_code_redemptions`, and increments the global usage count for that promo code. It also handles conditional statement acceptance requirements required by certain promo codes."
}
```

-------------------------------------------------
File #276
Path: /axialy-production-ui/var/www/html/axialy-ui/remove_analysis_package.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/auth.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php

Purpose:
This file serves as a backend API endpoint for soft-deleting analysis packages from the system. It validates an incoming JSON request to ensure a valid numeric 'package_id' is provided, authenticates the user session, and performs a database update operation to set the 'is_deleted' flag to 1 in the 'analysis_package_headers' table. It returns a JSON response indicating either success or failure.

Raw AI response:
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/auth.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php"
  ],
  "purpose": "This file serves as a backend API endpoint for soft-deleting analysis packages from the system. It validates an incoming JSON request to ensure a valid numeric 'package_id' is provided, authenticates the user session, and performs a database update operation to set the 'is_deleted' flag to 1 in the 'analysis_package_headers' table. It returns a JSON response indicating either success or failure."
}

-------------------------------------------------
File #277
Path: /axialy-production-ui/var/www/html/axialy-ui/reset_password.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/debug_utils.php

Purpose:
This file serves as the server-side controller and frontend template for the user password reset flow. It validates a password reset token provided via a URL query parameter against the `password_resets` database table. If the token is valid and not expired, it displays a form allowing the user to set a new password. Upon submission, it performs client-side and server-side validation (matching, length), hashes the new password using BCRYPT, updates the `ui_users` table, and marks the reset token as used to prevent replay attacks.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/debug_utils.php"
  ],
  "purpose": "This file serves as the server-side controller and frontend template for the user password reset flow. It validates a password reset token provided via a URL query parameter against the `password_resets` database table. If the token is valid and not expired, it displays a form allowing the user to set a new password. Upon submission, it performs client-side and server-side validation (matching, length), hashes the new password using BCRYPT, updates the `ui_users` table, and marks the reset token as used to prevent replay attacks."
}
```

-------------------------------------------------
File #278
Path: /axialy-production-ui/var/www/html/axialy-ui/save_analysis_package.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/validation.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/auth.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/focus_org_session.php

Purpose:
The primary purpose of this file is to handle the creation and update of 'Analysis Packages' within the system. It processes incoming JSON data representing package headers, associated focus areas (and their nested records), and optional Axialy output data. The script validates user sessions, manages database transactions to ensure data integrity during multi-table inserts/updates (affecting `analysis_package_headers`, `analysis_package_focus_areas`, `analysis_package_focus_area_versions`, `analysis_package_focus_area_records`, and `axialy_outputs`), and ensures correct linking between these entities. It also includes logic to handle organization scoping and supports both legacy and modern data formats for focus area records.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/validation.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/auth.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/focus_org_session.php"
  ],
  "purpose": "The primary purpose of this file is to handle the creation and update of 'Analysis Packages' within the system. It processes incoming JSON data representing package headers, associated focus areas (and their nested records), and optional Axialy output data. The script validates user sessions, manages database transactions to ensure data integrity during multi-table inserts/updates (affecting `analysis_package_headers`, `analysis_package_focus_areas`, `analysis_package_focus_area_versions`, `analysis_package_focus_area_records`, and `axialy_outputs`), and ensures correct linking between these entities. It also includes logic to handle organization scoping and supports both legacy and modern data formats for focus area records."
}
```

-------------------------------------------------
File #279
Path: /axialy-production-ui/var/www/html/axialy-ui/save_data_existing_package.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/auth.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php

Purpose:
This file serves as a backend API endpoint designed to receive, process, and persist data collected from UI interface ribbons into an existing analysis package. It validates incoming JSON payloads, authenticates the session, and performs database operations within a transaction to either create a new focus area (if one does not exist for the package) or generate a new version of an existing focus area by copying previous records and appending the newly submitted data. It ensures data integrity by linking input text summaries and maintaining correct versioning/ordering for analysis records.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/auth.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php"
  ],
  "purpose": "This file serves as a backend API endpoint designed to receive, process, and persist data collected from UI interface ribbons into an existing analysis package. It validates incoming JSON payloads, authenticates the session, and performs database operations within a transaction to either create a new focus area (if one does not exist for the package) or generate a new version of an existing focus area by copying previous records and appending the newly submitted data. It ensures data integrity by linking input text summaries and maintaining correct versioning/ordering for analysis records."
}
```

-------------------------------------------------
File #280
Path: /axialy-production-ui/var/www/html/axialy-ui/save_enhanced_records.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php

Purpose:
The file implements the server-side logic for the 'Enhance Content' workflow. It facilitates version control for focus area records by creating a new entry in 'analysis_package_focus_area_versions' (incrementing the version number), cloning existing records into this new version, and applying user-submitted updates or insertions to those records. It includes a concurrency check using a provided 'focus_area_version_id' to prevent data conflicts and ensures critical foreign key relationships ('analysis_package_focus_areas_id' and 'analysis_package_headers_id') are maintained in the database.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php"
  ],
  "purpose": "The file implements the server-side logic for the 'Enhance Content' workflow. It facilitates version control for focus area records by creating a new entry in 'analysis_package_focus_area_versions' (incrementing the version number), cloning existing records into this new version, and applying user-submitted updates or insertions to those records. It includes a concurrency check using a provided 'focus_area_version_id' to prevent data conflicts and ensures critical foreign key relationships ('analysis_package_focus_areas_id' and 'analysis_package_headers_id') are maintained in the database."
}
```

-------------------------------------------------
File #281
Path: /axialy-production-ui/var/www/html/axialy-ui/save_revised_records.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php

Purpose:
This file serves as a backend API endpoint that processes updates to 'focus area' records within an analysis package. Its primary function is to version control these records by creating a new version entry, cloning all existing records into that new version, applying user-submitted modifications (updates or additions), and resolving associated stakeholder feedback. It enforces data integrity by checking the current version ID (concurrency check) and ensuring that grid indices for records are preserved or incremented correctly.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php"
  ],
  "purpose": "This file serves as a backend API endpoint that processes updates to 'focus area' records within an analysis package. Its primary function is to version control these records by creating a new version entry, cloning all existing records into that new version, applying user-submitted modifications (updates or additions), and resolving associated stakeholder feedback. It enforces data integrity by checking the current version ID (concurrency check) and ensuring that grid indices for records are preserved or incremented correctly."
}
```

-------------------------------------------------
File #282
Path: /axialy-production-ui/var/www/html/axialy-ui/send_publication_invitations.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/auth.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/debug_utils.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/Config.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/Mailer.php

Purpose:
This file serves as a backend API endpoint for processing bulk publication invitations. Its primary purpose is to receive a request containing an artifact ID and a list of stakeholder emails, validate the input, perform a deduplication check to prevent spamming, generate a unique access token and 5-digit PIN for each recipient, persist these credentials in the 'publication_stakeholder_invitations' database table, and finally trigger an email notification via the centralized 'Mailer' class.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/auth.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/debug_utils.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/Config.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/Mailer.php"
  ],
  "purpose": "This file serves as a backend API endpoint for processing bulk publication invitations. Its primary purpose is to receive a request containing an artifact ID and a list of stakeholder emails, validate the input, perform a deduplication check to prevent spamming, generate a unique access token and 5-digit PIN for each recipient, persist these credentials in the 'publication_stakeholder_invitations' database table, and finally trigger an email notification via the centralized 'Mailer' class."
}
```

-------------------------------------------------
File #283
Path: /axialy-production-ui/var/www/html/axialy-ui/send_stakeholder_reminder.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/auth.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/debug_utils.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/Mailer.php

Purpose:
This file serves as a server-side endpoint for triggering reminder emails to stakeholders who have not yet provided feedback on an analysis package. It validates the user's session, checks ownership of the feedback request in the database, generates customized HTML and plain-text email content (including a personal message from the user and access credentials), and utilizes the `AxiaBA\Mailer` class to dispatch the email. It also handles request logging and error reporting.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/auth.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/debug_utils.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/Mailer.php"
  ],
  "purpose": "This file serves as a server-side endpoint for triggering reminder emails to stakeholders who have not yet provided feedback on an analysis package. It validates the user's session, checks ownership of the feedback request in the database, generates customized HTML and plain-text email content (including a personal message from the user and access credentials), and utilizes the `AxiaBA\\Mailer` class to dispatch the email. It also handles request logging and error reporting."
}
```

-------------------------------------------------
File #284
Path: /axialy-production-ui/var/www/html/axialy-ui/serve_logo.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/auth.php
  - /axialy-production-ui/var/www/html/axialy-ui/.env

Purpose:
The file serves as a secure, authenticated proxy for retrieving organization-specific logo images stored in an S3 bucket. It performs three main tasks: (1) validates that the requested file exists in the 'custom_organizations' database table; (2) verifies the requester's identity through multiple methods (standard session, stakeholder feedback session, or publication-specific session) to ensure they have authorized access to the organization associated with that logo; and (3) securely downloads the image from S3 using temporary AWS credentials generated at runtime, setting appropriate HTTP headers to stream the image to the browser.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/auth.php",
    "/axialy-production-ui/var/www/html/axialy-ui/.env"
  ],
  "purpose": "The file serves as a secure, authenticated proxy for retrieving organization-specific logo images stored in an S3 bucket. It performs three main tasks: (1) validates that the requested file exists in the 'custom_organizations' database table; (2) verifies the requester's identity through multiple methods (standard session, stakeholder feedback session, or publication-specific session) to ensure they have authorized access to the organization associated with that logo; and (3) securely downloads the image from S3 using temporary AWS credentials generated at runtime, setting appropriate HTTP headers to stream the image to the browser."
}
```

-------------------------------------------------
File #285
Path: /axialy-production-ui/var/www/html/axialy-ui/sitemap.php

Referenced files:
  (none)

Purpose:
This file serves as a server-side script to generate an XML sitemap for the ui.axialy.ai domain. It is designed to provide search engines with a list of publicly accessible pages (such as the homepage, login, registration, and documentation) while explicitly excluding any sensitive or private user data, ensuring that the site remains secure and compliant with data privacy practices.

Raw AI response:
```json
{
  "referenced_files": [],
  "purpose": "This file serves as a server-side script to generate an XML sitemap for the ui.axialy.ai domain. It is designed to provide search engines with a list of publicly accessible pages (such as the homepage, login, registration, and documentation) while explicitly excluding any sensitive or private user data, ensuring that the site remains secure and compliant with data privacy practices."
}
```

-------------------------------------------------
File #286
Path: /axialy-production-ui/var/www/html/axialy-ui/start_account_recovery.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/Config.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/Mailer.php

Purpose:
This file acts as an API endpoint handler for user account recovery. It processes POST requests to facilitate either username retrieval, password reset initiation, or both. It verifies the user's email address against the database, generates a secure time-limited token for password resets if required, and triggers the appropriate email communication via the Mailer service. For security, it returns a generic success message regardless of whether the email address exists in the system.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/Config.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/Mailer.php"
  ],
  "purpose": "This file acts as an API endpoint handler for user account recovery. It processes POST requests to facilitate either username retrieval, password reset initiation, or both. It verifies the user's email address against the database, generates a secure time-limited token for password resets if required, and triggers the appropriate email communication via the Mailer service. For security, it returns a generic success message regardless of whether the email address exists in the system."
}
```

-------------------------------------------------
File #287
Path: /axialy-production-ui/var/www/html/axialy-ui/start_verification.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/account_creation.php

Purpose:
This file serves as a server-side endpoint for initiating the e-mail verification flow during the AxiaBA account creation process. It validates that the request is a POST, performs input sanitization on the provided e-mail, checks for duplicate registrations, generates a verification token using the AccountCreation helper class, and attempts to send the verification e-mail to the user. It manages the full lifecycle of this initiation step, including cleanup (token deletion) upon email delivery failure and standardized JSON error/success messaging.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/account_creation.php"
  ],
  "purpose": "This file serves as a server-side endpoint for initiating the e-mail verification flow during the AxiaBA account creation process. It validates that the request is a POST, performs input sanitization on the provided e-mail, checks for duplicate registrations, generates a verification token using the AccountCreation helper class, and attempts to send the verification e-mail to the user. It manages the full lifecycle of this initiation step, including cleanup (token deletion) upon email delivery failure and standardized JSON error/success messaging."
}
```

-------------------------------------------------
File #288
Path: /axialy-production-ui/var/www/html/axialy-ui/store_analysis_package_focus_area_version.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/validation.php

Purpose:
This file acts as a backend API endpoint that processes JSON requests to persist versioning information for specific analysis focus areas. It reads the 'analysis_package_focus_areas_id' and 'focus_area_version_number' from the request body and inserts a new entry into the 'analysis_package_focus_area_versions' database table. It relies on included helper files for database connectivity and request validation, and it returns a JSON response indicating success or failure.

Raw AI response:
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/validation.php"
  ],
  "purpose": "This file acts as a backend API endpoint that processes JSON requests to persist versioning information for specific analysis focus areas. It reads the 'analysis_package_focus_areas_id' and 'focus_area_version_number' from the request body and inserts a new entry into the 'analysis_package_focus_area_versions' database table. It relies on included helper files for database connectivity and request validation, and it returns a JSON response indicating success or failure."
}

-------------------------------------------------
File #289
Path: /axialy-production-ui/var/www/html/axialy-ui/store_analysis_package_header.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/validation.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php

Purpose:
This file serves as a backend API endpoint designed to receive JSON-formatted input from a client, validate the data, and persist a new record into the 'analysis_package_headers' table of the database. It handles the creation of analysis packages within the system's updated schema, explicitly deprecating legacy [redacted] functionality, and returns a JSON response indicating either success (with the new record ID) or failure (with error details).

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/validation.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php"
  ],
  "purpose": "This file serves as a backend API endpoint designed to receive JSON-formatted input from a client, validate the data, and persist a new record into the 'analysis_package_headers' table of the database. It handles the creation of analysis packages within the system's updated schema, explicitly deprecating legacy [redacted] functionality, and returns a JSON response indicating either success (with the new record ID) or failure (with error details)."
}
```

-------------------------------------------------
File #290
Path: /axialy-production-ui/var/www/html/axialy-ui/store_feedback_data.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/Config.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php

Purpose:
This file serves as a backend API endpoint designed to receive and persist 'focus-area' record data via a POST request. It processes a JSON payload containing multiple records, calculates a 'display_order' (derived as grid_index + 1), determines the associated analysis package ID based on the provided focus_area_version_id, and inserts the data into the 'analysis_package_focus_area_records' database table. It ensures secure CORS headers, provides JSON-formatted error/success responses, and uses database transactions logic via PDO.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/Config.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php"
  ],
  "purpose": "This file serves as a backend API endpoint designed to receive and persist 'focus-area' record data via a POST request. It processes a JSON payload containing multiple records, calculates a 'display_order' (derived as grid_index + 1), determines the associated analysis package ID based on the provided focus_area_version_id, and inserts the data into the 'analysis_package_focus_area_records' database table. It ensures secure CORS headers, provides JSON-formatted error/success responses, and uses database transactions logic via PDO."
}
```

-------------------------------------------------
File #291
Path: /axialy-production-ui/var/www/html/axialy-ui/store_summary.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/api_auth.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php

Purpose:
This file serves as a server-side API endpoint designed to accept, sanitize, and persist text summarization data into the database. It handles both single and batch (multiple) summary submissions via HTTP POST requests, enforces authentication, ensures data integrity through required field validation and regex datetime checks, and provides JSON-formatted responses indicating success or failure.

Raw AI response:
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/api_auth.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php"
  ],
  "purpose": "This file serves as a server-side API endpoint designed to accept, sanitize, and persist text summarization data into the database. It handles both single and batch (multiple) summary submissions via HTTP POST requests, enforces authentication, ensures data integrity through required field validation and regex datetime checks, and provides JSON-formatted responses indicating success or failure."
}

-------------------------------------------------
File #292
Path: /axialy-production-ui/var/www/html/axialy-ui/submit_content_review.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/error_log

Purpose:
This script acts as a backend endpoint for submitting content review requests. It processes POST requests containing a list of 'stakeholders', validates the input, and appends a formatted timestamped log entry to a local 'error_log' file. It returns a JSON response indicating either success or failure (via HTTP status codes and JSON messages).

Raw AI response:
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/error_log"
  ],
  "purpose": "This script acts as a backend endpoint for submitting content review requests. It processes POST requests containing a list of 'stakeholders', validates the input, and appends a formatted timestamped log entry to a local 'error_log' file. It returns a JSON response indicating either success or failure (via HTTP status codes and JSON messages)."
}

-------------------------------------------------
File #293
Path: /axialy-production-ui/var/www/html/axialy-ui/submit_issue.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/auth.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php

Purpose:
This file serves as a backend API endpoint for submitting user-reported issues. It authenticates the requester using a custom session handler, accepts a JSON payload containing an issue title and description, performs basic validation, and persists the data to the 'issues' table in the database with a default status of 'Open'.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/auth.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php"
  ],
  "purpose": "This file serves as a backend API endpoint for submitting user-reported issues. It authenticates the requester using a custom session handler, accepts a JSON payload containing an issue title and description, performs basic validation, and persists the data to the 'issues' table in the database with a default status of 'Open'."
}
```

-------------------------------------------------
File #294
Path: /axialy-production-ui/var/www/html/axialy-ui/subscription.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/Config.php
  - /axialy-production-ui/var/www/html/axialy-ui/vendor/autoload.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/auth.php
  - /assets/css/promo-modal.css
  - /assets/img/product_logo.png
  - /js/promo-modal.js
  - /create_subscription.php
  - /redeem_promo_code.php
  - /index.php
  - /login.php
  - /manage-subscription.php

Purpose:
The `subscription.php` file serves as the primary subscription management and billing interface for the application. It handles user authentication, checks existing subscription status to prevent unauthorized access or duplicate billing, and provides a front-end interface for users to select between subscription tiers (Monthly vs. Day Pass). The file integrates with Stripe to process payments and supports promotional code redemption, including dynamic UI updates for special terms or mandatory disclaimers.

Raw AI response:
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/Config.php",
    "/axialy-production-ui/var/www/html/axialy-ui/vendor/autoload.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/auth.php",
    "/assets/css/promo-modal.css",
    "/assets/img/product_logo.png",
    "/js/promo-modal.js",
    "/create_subscription.php",
    "/redeem_promo_code.php",
    "/index.php",
    "/login.php",
    "/manage-subscription.php"
  ],
  "purpose": "The `subscription.php` file serves as the primary subscription management and billing interface for the application. It handles user authentication, checks existing subscription status to prevent unauthorized access or duplicate billing, and provides a front-end interface for users to select between subscription tiers (Monthly vs. Day Pass). The file integrates with Stripe to process payments and supports promotional code redemption, including dynamic UI updates for special terms or mandatory disclaimers."
}

-------------------------------------------------
File #295
Path: /axialy-production-ui/var/www/html/axialy-ui/subscription_25_per_month.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/Config.php
  - /axialy-production-ui/var/www/html/axialy-ui/vendor/autoload.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/auth.php
  - /login.php
  - /manage-subscription.php
  - /assets/img/product_logo.png
  - /create_subscription.php
  - /index.php
  - /redeem_promo_code.php

Purpose:
This file serves as the user-facing subscription and payment interface for the AxiaBA platform. Its primary functions include: authenticating the user via existing sessions, checking for any existing active subscriptions or valid day passes to prevent redundant billing (redirecting to 'manage-subscription.php' if active), and providing a Stripe-integrated checkout form for users to purchase either a monthly subscription or a 24-hour day pass. It also includes client-side logic to handle promo code redemption, dynamic UI updates for payment processing, and final redirection to the main dashboard ('index.php') upon successful transaction.

Raw AI response:
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/Config.php",
    "/axialy-production-ui/var/www/html/axialy-ui/vendor/autoload.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/auth.php",
    "/login.php",
    "/manage-subscription.php",
    "/assets/img/product_logo.png",
    "/create_subscription.php",
    "/index.php",
    "/redeem_promo_code.php"
  ],
  "purpose": "This file serves as the user-facing subscription and payment interface for the AxiaBA platform. Its primary functions include: authenticating the user via existing sessions, checking for any existing active subscriptions or valid day passes to prevent redundant billing (redirecting to 'manage-subscription.php' if active), and providing a Stripe-integrated checkout form for users to purchase either a monthly subscription or a 24-hour day pass. It also includes client-side logic to handle promo code redemption, dynamic UI updates for payment processing, and final redirection to the main dashboard ('index.php') upon successful transaction."
}

-------------------------------------------------
File #296
Path: /axialy-production-ui/var/www/html/axialy-ui/test_actual_endpoint.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/start_verification.php

Purpose:
This file is a diagnostic utility script designed to verify the operational status of the 'start_verification.php' endpoint. It uses cURL to simulate a POST request to the production URL ('https://ui.axialy.ai/start_verification.php') and outputs the HTTP status code, headers, and the raw/parsed JSON response body for troubleshooting. It includes a basic security mechanism ('test=endpoint123') to prevent unauthorized execution of the test.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/start_verification.php"
  ],
  "purpose": "This file is a diagnostic utility script designed to verify the operational status of the 'start_verification.php' endpoint. It uses cURL to simulate a POST request to the production URL ('https://ui.axialy.ai/start_verification.php') and outputs the HTTP status code, headers, and the raw/parsed JSON response body for troubleshooting. It includes a basic security mechanism ('test=endpoint123') to prevent unauthorized execution of the test."
}
```

-------------------------------------------------
File #297
Path: /axialy-production-ui/var/www/html/axialy-ui/update_analysis_package.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/auth.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/focus_org_session.php

Purpose:
This file acts as a backend API endpoint designed to update the details of an existing analysis package in the database. It processes JSON input containing package metadata (name, summaries, and custom organization mapping), validates the user's session and authorization, and performs a secure SQL update against the 'analysis_package_headers' table. It ensures that users can only update packages that belong to their authorized 'default_organization_id', providing error handling for concurrency or permission mismatches.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/auth.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/focus_org_session.php"
  ],
  "purpose": "This file acts as a backend API endpoint designed to update the details of an existing analysis package in the database. It processes JSON input containing package metadata (name, summaries, and custom organization mapping), validates the user's session and authorization, and performs a secure SQL update against the 'analysis_package_headers' table. It ensures that users can only update packages that belong to their authorized 'default_organization_id', providing error handling for concurrency or permission mismatches."
}
```

-------------------------------------------------
File #298
Path: /axialy-production-ui/var/www/html/axialy-ui/update_custom_organization.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/auth.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/validation.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/debug_utils.php
  - /axialy-production-ui/var/www/html/axialy-ui/.env

Purpose:
This file is a backend API endpoint responsible for updating existing custom organization records in the database. It validates user authentication, ensures the user owns the organization, handles optional logo file uploads to an AWS S3 bucket using the AWS CLI, and persists the updated profile data (name, contact info, website, etc.) to the `custom_organizations` table. It also performs cleanup of old logo files on S3 when a new logo is uploaded.

Raw AI response:
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/auth.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/validation.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/debug_utils.php",
    "/axialy-production-ui/var/www/html/axialy-ui/.env"
  ],
  "purpose": "This file is a backend API endpoint responsible for updating existing custom organization records in the database. It validates user authentication, ensures the user owns the organization, handles optional logo file uploads to an AWS S3 bucket using the AWS CLI, and persists the updated profile data (name, contact info, website, etc.) to the `custom_organizations` table. It also performs cleanup of old logo files on S3 when a new logo is uploaded."
}

-------------------------------------------------
File #299
Path: /axialy-production-ui/var/www/html/axialy-ui/update_focus_organization.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/auth.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/debug_utils.php

Purpose:
This script functions as an API endpoint designed to update the 'focus organization' preference for the currently authenticated user. It handles JSON input containing a 'focus_org_id', validates the input against the user's authorized custom organizations, and then manages the persistence of this preference in the 'user_focus_organizations' database table (performing inserts, updates, or deletions depending on whether a default or custom ID is provided).

Raw AI response:
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/auth.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/debug_utils.php"
  ],
  "purpose": "This script functions as an API endpoint designed to update the 'focus organization' preference for the currently authenticated user. It handles JSON input containing a 'focus_org_id', validates the input against the user's authorized custom organizations, and then manages the persistence of this preference in the 'user_focus_organizations' database table (performing inserts, updates, or deletions depending on whether a default or custom ID is provided)."
}

-------------------------------------------------
File #300
Path: /axialy-production-ui/var/www/html/axialy-ui/update_publication_expiry.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/auth.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/debug_utils.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/focus_org_session.php

Purpose:
This file serves as a JSON-based API endpoint used to update the expiry date of a specific published artifact. It verifies the user's session and organizational permissions, validates the new expiry date, updates the database (published_artifacts table), and returns a status object including formatted time-remaining metadata for the frontend UI.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/auth.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/debug_utils.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/focus_org_session.php"
  ],
  "purpose": "This file serves as a JSON-based API endpoint used to update the expiry date of a specific published artifact. It verifies the user's session and organizational permissions, validates the new expiry date, updates the database (published_artifacts table), and returns a status object including formatted time-remaining metadata for the frontend UI."
}
```

-------------------------------------------------
File #301
Path: /axialy-production-ui/var/www/html/axialy-ui/user-documentation.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/auth.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php
  - /axialy-production-ui/var/www/html/axialy-ui/docs/view_document.php
  - /content/user-documentation.html

Purpose:
This file serves as the main user-facing documentation portal within the AxiaBA application. It enforces user authentication and subscription checks, fetches a list of authorized customer-facing documents from the database, and renders a split-pane interface (sidebar for document navigation and an iframe for content rendering) to allow users to view documentation.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/auth.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php",
    "/axialy-production-ui/var/www/html/axialy-ui/docs/view_document.php",
    "/content/user-documentation.html"
  ],
  "purpose": "This file serves as the main user-facing documentation portal within the AxiaBA application. It enforces user authentication and subscription checks, fetches a list of authorized customer-facing documents from the database, and renders a split-pane interface (sidebar for document navigation and an iframe for content rendering) to allow users to view documentation."
}
```

-------------------------------------------------
File #302
Path: /axialy-production-ui/var/www/html/axialy-ui/verify_email.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/account_creation.php
  - /assets/css/desktop.css
  - login.php

Purpose:
This file acts as a landing page for email verification links. It serves two primary functions: (1) It validates a token passed via URL to confirm an email address; and (2) upon successful verification, it presents a form to the user to finalize their account creation by choosing a username and setting a password. It utilizes the 'AccountCreation' class to handle database logic and redirects users to 'login.php' once their account is successfully created.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/account_creation.php",
    "/assets/css/desktop.css",
    "login.php"
  ],
  "purpose": "This file acts as a landing page for email verification links. It serves two primary functions: (1) It validates a token passed via URL to confirm an email address; and (2) upon successful verification, it presents a form to the user to finalize their account creation by choosing a username and setting a password. It utilizes the 'AccountCreation' class to handle database logic and redirects users to 'login.php' once their account is successfully created."
}
```

-------------------------------------------------
File #303
Path: /axialy-production-ui/var/www/html/axialy-ui/view_publication.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php
  - /axialy-production-ui/var/www/html/axialy-ui/includes/debug_utils.php
  - /serve_logo.php

Purpose:
The file serves as a public-facing (or authenticated) portal for viewing published business analysis artifacts. It handles two distinct access workflows: 1) authenticated platform users accessing reports directly, and 2) external stakeholders accessing reports via a unique URL token and a mandatory 5-digit PIN. The script validates publication expiry dates, manages sessions for authorized access, and dynamically renders the report content while applying custom organization branding (logos/links).

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/db_connection.php",
    "/axialy-production-ui/var/www/html/axialy-ui/includes/debug_utils.php",
    "/serve_logo.php"
  ],
  "purpose": "The file serves as a public-facing (or authenticated) portal for viewing published business analysis artifacts. It handles two distinct access workflows: 1) authenticated platform users accessing reports directly, and 2) external stakeholders accessing reports via a unique URL token and a mandatory 5-digit PIN. The script validates publication expiry dates, manages sessions for authorized access, and dynamically renders the report content while applying custom organization branding (logos/links)."
}
```

-------------------------------------------------
File #304
Path: /axialy-production-ui/var/www/html/axialy-ui/webhook.php

Referenced files:
  - /axialy-production-ui/var/www/html/axialy-ui/includes/Config.php
  - /axialy-production-ui/var/www/html/axialy-ui/vendor/autoload.php

Purpose:
The file serves as a Stripe webhook endpoint handler for the application. Its primary function is to receive and verify incoming HTTP POST requests sent by Stripe, validate the event signature using a secret retrieved from the local configuration, and process specific events (currently 'invoice.payment_succeeded') to update subscription statuses within the system's database.

Raw AI response:
{
  "referenced_files": [
    "/axialy-production-ui/var/www/html/axialy-ui/includes/Config.php",
    "/axialy-production-ui/var/www/html/axialy-ui/vendor/autoload.php"
  ],
  "purpose": "The file serves as a Stripe webhook endpoint handler for the application. Its primary function is to receive and verify incoming HTTP POST requests sent by Stripe, validate the event signature using a secret retrieved from the local configuration, and process specific events (currently 'invoice.payment_succeeded') to update subscription statuses within the system's database."
}

-------------------------------------------------
File #305
Path: /axialy-production-ui/var/www/html/archive-test.txt

Referenced files:
  (none)

Purpose:
This file is a simple text file containing only the string 'archive-test'. Based on its filename and content, it serves no functional role in the application logic and appears to be a leftover test artifact or placeholder file used for verifying file system access or archival processes.

Raw AI response:
```json
{
  "referenced_files": [],
  "purpose": "This file is a simple text file containing only the string 'archive-test'. Based on its filename and content, it serves no functional role in the application logic and appears to be a leftover test artifact or placeholder file used for verifying file system access or archival processes."
}
```

-------------------------------------------------
File #306
Path: /axialy-production-ui/README.md

Referenced files:
  (none)

Purpose:
The README.md file serves as an informational manifest and system documentation for the `axialy-production-ui` server. Its primary purpose is to provide administrative context regarding the infrastructure (AWS EC2 instance details), the server's role in hosting the Axialy AI platform's frontend, and an overview of the key functional features implemented within the application, such as stakeholder engagement, AI-driven analysis, Stripe billing integration, and multi-tenant organization management. No specific source code files are referenced within this document.

Raw AI response:
{
  "referenced_files": [],
  "purpose": "The README.md file serves as an informational manifest and system documentation for the `axialy-production-ui` server. Its primary purpose is to provide administrative context regarding the infrastructure (AWS EC2 instance details), the server's role in hosting the Axialy AI platform's frontend, and an overview of the key functional features implemented within the application, such as stakeholder engagement, AI-driven analysis, Stripe billing integration, and multi-tenant organization management. No specific source code files are referenced within this document."
}

-------------------------------------------------