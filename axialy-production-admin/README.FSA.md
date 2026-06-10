File System Analysis (APRO):

Analyzed file count: 36 / 36

-------------------------------------------------
File #1
Path: /axialy-production-admin/README.md

Referenced files:
  (none)

Purpose:
The README.md file serves as the high-level technical documentation and architectural manifest for the 'axialy-production-admin' repository. Its primary purpose is to outline the infrastructure details (AWS instance configuration) and define the functional scope of the admin control panel, which manages the Axialy AI platform's databases, documentation, support ticketing, and promotional operations. It acts as an overview document rather than an executable component, and does not explicitly reference specific file paths within the system.

Raw AI response:
```json
{
  "referenced_files": [],
  "purpose": "The README.md file serves as the high-level technical documentation and architectural manifest for the 'axialy-production-admin' repository. Its primary purpose is to outline the infrastructure details (AWS instance configuration) and define the functional scope of the admin control panel, which manages the Axialy AI platform's databases, documentation, support ticketing, and promotional operations. It acts as an overview document rather than an executable component, and does not explicitly reference specific file paths within the system."
}
```

-------------------------------------------------
File #2
Path: /axialy-production-admin/var/www/html/admin-api/.htaccess

Referenced files:
  - /axialy-production-admin/var/www/html/admin-api/index.php

Purpose:
This .htaccess file acts as the front-controller configuration for the admin-api directory. Its primary purpose is to intercept all incoming HTTP requests that do not map to an existing physical file or directory and route them internally to 'index.php'. The [QSA] (Query String Append) flag ensures that any original query parameters are preserved during this rewrite, effectively enabling a single-entry-point architecture for the API.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-admin/var/www/html/admin-api/index.php"
  ],
  "purpose": "This .htaccess file acts as the front-controller configuration for the admin-api directory. Its primary purpose is to intercept all incoming HTTP requests that do not map to an existing physical file or directory and route them internally to 'index.php'. The [QSA] (Query String Append) flag ensures that any original query parameters are preserved during this rewrite, effectively enabling a single-entry-point architecture for the API."
}
```

-------------------------------------------------
File #3
Path: /axialy-production-admin/var/www/html/admin-api/index.php

Referenced files:
  - /etc/mfp/api_key
  - /etc/mfp/allowed_root
  - /var/www/html/.env.master
  - /usr/local/sbin/mfp-apro-install-file
  - /usr/local/sbin/mfp-apro-archive-file

Purpose:
This file serves as a centralized administrative API endpoint for the MaxFlex system. Its primary role is to provide a secure, authenticated interface for file management and system configuration tasks, including: navigating the filesystem (tree view), reading file contents, archiving/versioning files, deploying updates via .tar.gz archives, managing an environment configuration file (.env.master), and restoring previous file versions from archives. The script enforces security via an API key check and strict path normalization to prevent directory traversal outside of defined allowed roots, often leveraging external shell helpers for privileged filesystem operations.

Raw AI response:
```json
{
  "referenced_files": [
    "/etc/mfp/api_key",
    "/etc/mfp/allowed_root",
    "/var/www/html/.env.master",
    "/usr/local/sbin/mfp-apro-install-file",
    "/usr/local/sbin/mfp-apro-archive-file"
  ],
  "purpose": "This file serves as a centralized administrative API endpoint for the MaxFlex system. Its primary role is to provide a secure, authenticated interface for file management and system configuration tasks, including: navigating the filesystem (tree view), reading file contents, archiving/versioning files, deploying updates via .tar.gz archives, managing an environment configuration file (.env.master), and restoring previous file versions from archives. The script enforces security via an API key check and strict path normalization to prevent directory traversal outside of defined allowed roots, often leveraging external shell helpers for privileged filesystem operations."
}
```

-------------------------------------------------
File #4
Path: /axialy-production-admin/var/www/html/axialy-admin/assets/css/styles.css

Referenced files:
  (none)

Purpose:
This file is the primary CSS stylesheet for the Axialy Admin dashboard. Its functional purpose is to provide a comprehensive, mobile-first responsive design framework for the entire administrative interface. It defines global styles (reset, base typography, layout systems), UI component styles (headers, forms, buttons, tables, pagination, and status messages), and utility classes. It also includes specific responsive design logic to ensure the interface functions effectively across mobile devices and desktops, including accessibility enhancements and touch-friendly optimizations.

Raw AI response:
```json
{
  "referenced_files": [],
  "purpose": "This file is the primary CSS stylesheet for the Axialy Admin dashboard. Its functional purpose is to provide a comprehensive, mobile-first responsive design framework for the entire administrative interface. It defines global styles (reset, base typography, layout systems), UI component styles (headers, forms, buttons, tables, pagination, and status messages), and utility classes. It also includes specific responsive design logic to ensure the interface functions effectively across mobile devices and desktops, including accessibility enhancements and touch-friendly optimizations."
}
```

-------------------------------------------------
File #5
Path: /axialy-production-admin/var/www/html/axialy-admin/assets/js/dashboard.js

Referenced files:
  (none)

Purpose:
The file serves as a client-side controller for the Axialy Admin dashboard. Its primary functional purposes are to manage UI interactions—specifically handling form submissions for environment switching—and to apply responsive design adjustments to improve usability on mobile devices (such as enforcing minimum touch target sizes and preventing iOS auto-zooming on inputs).

Raw AI response:
```json
{
  "referenced_files": [],
  "purpose": "The file serves as a client-side controller for the Axialy Admin dashboard. Its primary functional purposes are to manage UI interactions—specifically handling form submissions for environment switching—and to apply responsive design adjustments to improve usability on mobile devices (such as enforcing minimum touch target sizes and preventing iOS auto-zooming on inputs)."
}
```

-------------------------------------------------
File #6
Path: /axialy-production-admin/var/www/html/axialy-admin/assets/js/db_viewer_admin.js

Referenced files:
  - db_viewer_ajax.php

Purpose:
This file provides the client-side JavaScript logic for the 'Database Viewer' administration interface. It handles dynamic interaction with the backend (via `db_viewer_ajax.php`), including listing database tables, fetching and paginating table data, applying column filters, and exporting table data to CSV. Additionally, it enhances the user interface by providing features such as collapsing/expanding sidebar panels, truncating long text fields with modal-based inspection, and managing UI state for data loading and pagination.

Raw AI response:
{
  "referenced_files": [
    "db_viewer_ajax.php"
  ],
  "purpose": "This file provides the client-side JavaScript logic for the 'Database Viewer' administration interface. It handles dynamic interaction with the backend (via `db_viewer_ajax.php`), including listing database tables, fetching and paginating table data, applying column filters, and exporting table data to CSV. Additionally, it enhances the user interface by providing features such as collapsing/expanding sidebar panels, truncating long text fields with modal-based inspection, and managing UI state for data loading and pagination."
}

-------------------------------------------------
File #7
Path: /axialy-production-admin/var/www/html/axialy-admin/assets/js/docs_admin.js

Referenced files:
  - /axialy-production-admin/var/www/html/axialy-admin/assets/js/doc_ajax_actions.php

Purpose:
This JavaScript file powers the client-side user interface for the 'Documents Management' section of the Axialy admin panel. It manages the lifecycle of documents and their versions by communicating with the backend via `doc_ajax_actions.php`. Key functionalities include listing documents, creating/updating document metadata, managing version history (creating versions, setting active versions), triggering document generation (PDF/DOCX), and handling file uploads for documents. It assumes the existence of specific DOM elements (e.g., forms, containers) in the corresponding HTML view.

Raw AI response:
{
  "referenced_files": [
    "/axialy-production-admin/var/www/html/axialy-admin/assets/js/doc_ajax_actions.php"
  ],
  "purpose": "This JavaScript file powers the client-side user interface for the 'Documents Management' section of the Axialy admin panel. It manages the lifecycle of documents and their versions by communicating with the backend via `doc_ajax_actions.php`. Key functionalities include listing documents, creating/updating document metadata, managing version history (creating versions, setting active versions), triggering document generation (PDF/DOCX), and handling file uploads for documents. It assumes the existence of specific DOM elements (e.g., forms, containers) in the corresponding HTML view."
}

-------------------------------------------------
File #8
Path: /axialy-production-admin/var/www/html/axialy-admin/assets/js/issues_admin.js

Referenced files:
  - /axialy-production-admin/var/www/html/axialy-admin/assets/js/issues_ajax_actions.php

Purpose:
This file provides the client-side JavaScript logic for the 'Issues Management' interface within the admin panel. It manages the lifecycle of the issues UI, including fetching and rendering the list of issues, toggling UI panels, handling form interactions for editing issue details, and triggering email notifications to users. It acts as the frontend controller, communicating asynchronously with 'issues_ajax_actions.php' to perform CRUD-like operations and retrieve data without page reloads. Note: The referenced 'issues_ajax_actions.php' is assumed to be in the same directory context as the calling script based on the relative fetch path.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-admin/var/www/html/axialy-admin/assets/js/issues_ajax_actions.php"
  ],
  "purpose": "This file provides the client-side JavaScript logic for the 'Issues Management' interface within the admin panel. It manages the lifecycle of the issues UI, including fetching and rendering the list of issues, toggling UI panels, handling form interactions for editing issue details, and triggering email notifications to users. It acts as the frontend controller, communicating asynchronously with 'issues_ajax_actions.php' to perform CRUD-like operations and retrieve data without page reloads. Note: The referenced 'issues_ajax_actions.php' is assumed to be in the same directory context as the calling script based on the relative fetch path."
}
```

-------------------------------------------------
File #9
Path: /axialy-production-admin/var/www/html/axialy-admin/assets/js/promo_codes_admin.js

Referenced files:
  - promo_codes_ajax_actions.php

Purpose:
This file serves as the client-side controller for managing promotional codes within the Axialy Admin system. It provides an interface to list, create, and edit promo codes by interacting with a backend endpoint (`promo_codes_ajax_actions.php`). The script handles DOM event binding, dynamic form rendering/toggling, form data serialization for API submissions, and validation logic for different promo types (unlimited, limited, and discounted). Note: The code references an external function `handleTypeChange()` which is not defined within this file and is expected to be provided by the host HTML page or another included script.

Raw AI response:
{
  "referenced_files": [
    "promo_codes_ajax_actions.php"
  ],
  "purpose": "This file serves as the client-side controller for managing promotional codes within the Axialy Admin system. It provides an interface to list, create, and edit promo codes by interacting with a backend endpoint (`promo_codes_ajax_actions.php`). The script handles DOM event binding, dynamic form rendering/toggling, form data serialization for API submissions, and validation logic for different promo types (unlimited, limited, and discounted). Note: The code references an external function `handleTypeChange()` which is not defined within this file and is expected to be provided by the host HTML page or another included script."
}

-------------------------------------------------
File #10
Path: /axialy-production-admin/var/www/html/axialy-admin/assets/js/README.md

Referenced files:
  (none)

Purpose:
The file is an empty README.md located within the project's JavaScript assets directory. As it contains no content, it serves no functional purpose in the system and does not reference any other files.

Raw AI response:
```json
{
  "referenced_files": [],
  "purpose": "The file is an empty README.md located within the project's JavaScript assets directory. As it contains no content, it serves no functional purpose in the system and does not reference any other files."
}
```

-------------------------------------------------
File #11
Path: /axialy-production-admin/var/www/html/axialy-admin/includes/AdminDBConfig.php

Referenced files:
  - /axialy-production-admin/var/www/html/axialy-admin/.env

Purpose:
The AdminDBConfig class serves as a singleton-based database connection and configuration manager for the Axialy Admin system. Its primary responsibilities include: 1) Managing PDO connection pooling for both the administration database and the UI database, 2) Bootstrapping configuration from an optional '.env' file located in the parent directory, and 3) Automating database schema initialization (specifically for the admin tables) to ensure necessary structures like 'admin_users' and 'admin_user_sessions' exist upon application access.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-admin/var/www/html/axialy-admin/.env"
  ],
  "purpose": "The AdminDBConfig class serves as a singleton-based database connection and configuration manager for the Axialy Admin system. Its primary responsibilities include: 1) Managing PDO connection pooling for both the administration database and the UI database, 2) Bootstrapping configuration from an optional '.env' file located in the parent directory, and 3) Automating database schema initialization (specifically for the admin tables) to ensure necessary structures like 'admin_users' and 'admin_user_sessions' exist upon application access."
}
```

-------------------------------------------------
File #12
Path: /axialy-production-admin/var/www/html/axialy-admin/includes/admin_auth.php

Referenced files:
  - /axialy-production-admin/var/www/html/axialy-admin/includes/AdminDBConfig.php

Purpose:
This file serves as a centralized authentication gatekeeper for the administrative dashboard. It provides the `requireAdminAuth()` function, which validates the current user's session against the `admin_user_sessions` and `admin_users` tables in the database to ensure the user is logged in, their session is active/not expired, and their account is enabled. It also provides a utility function, `logoutAndRedirect()`, which safely terminates the session (both locally and in the database) and redirects the user to the login page.

Raw AI response:
{
  "referenced_files": [
    "/axialy-production-admin/var/www/html/axialy-admin/includes/AdminDBConfig.php"
  ],
  "purpose": "This file serves as a centralized authentication gatekeeper for the administrative dashboard. It provides the `requireAdminAuth()` function, which validates the current user's session against the `admin_user_sessions` and `admin_users` tables in the database to ensure the user is logged in, their session is active/not expired, and their account is enabled. It also provides a utility function, `logoutAndRedirect()`, which safely terminates the session (both locally and in the database) and redirects the user to the login page."
}

-------------------------------------------------
File #13
Path: /axialy-production-admin/var/www/html/axialy-admin/includes/Config.php

Referenced files:
  (none)

Purpose:
The file serves as a centralized configuration manager that bridges legacy code requirements with modern environment-variable-based infrastructure. It implements a singleton pattern to maintain a cache of application settings (such as database credentials and various API keys), allowing existing codebases to continue using a standard 'getInstance()->get()' API while decoupling configuration values from the application source code.

Raw AI response:
```json
{
  "referenced_files": [],
  "purpose": "The file serves as a centralized configuration manager that bridges legacy code requirements with modern environment-variable-based infrastructure. It implements a singleton pattern to maintain a cache of application settings (such as database credentials and various API keys), allowing existing codebases to continue using a standard 'getInstance()->get()' API while decoupling configuration values from the application source code."
}
```

-------------------------------------------------
File #14
Path: /axialy-production-admin/var/www/html/axialy-admin/includes/db_connection.php

Referenced files:
  - /axialy-production-admin/var/www/html/.env
  - /axialy-production-admin/var/www/.env

Purpose:
This file serves as a centralized database connection utility for the Axialy UI application. It manages the configuration and instantiation of a PDO object by dynamically loading environment variables. It prioritizes system-level environment variables (injected by Docker or Ansible) and provides a fallback mechanism that attempts to parse local .env files located at specific relative directory levels (two or three levels above the script's directory) for development environments. Once successfully executed, it makes a global $pdo instance available for use by other scripts in the application.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-admin/var/www/html/.env",
    "/axialy-production-admin/var/www/.env"
  ],
  "purpose": "This file serves as a centralized database connection utility for the Axialy UI application. It manages the configuration and instantiation of a PDO object by dynamically loading environment variables. It prioritizes system-level environment variables (injected by Docker or Ansible) and provides a fallback mechanism that attempts to parse local .env files located at specific relative directory levels (two or three levels above the script's directory) for development environments. Once successfully executed, it makes a global $pdo instance available for use by other scripts in the application."
}
```

-------------------------------------------------
File #15
Path: /axialy-production-admin/var/www/html/axialy-admin/includes/environment_selector.php

Referenced files:
  (none)

Purpose:
This file serves as a configuration utility to establish the operational environment (e.g., development, staging, production) for the admin interface. It manages PHP session state to retrieve the current 'admin_env' value, defaulting to 'production' if no environment has been explicitly set in the session. It is designed to be included by other scripts to ensure consistent environment-aware logic across the admin panel.

Raw AI response:
```json
{
  "referenced_files": [],
  "purpose": "This file serves as a configuration utility to establish the operational environment (e.g., development, staging, production) for the admin interface. It manages PHP session state to retrieve the current 'admin_env' value, defaulting to 'production' if no environment has been explicitly set in the session. It is designed to be included by other scripts to ensure consistent environment-aware logic across the admin panel."
}
```

-------------------------------------------------
File #16
Path: /axialy-production-admin/var/www/html/axialy-admin/includes/README.md

Referenced files:
  - /axialy-production-admin/var/www/html/axialy-admin/includes/AdminDBConfig.php
  - /axialy-production-admin/var/www/html/axialy-admin/includes/Config.php
  - /axialy-production-admin/var/www/html/axialy-admin/includes/admin_auth.php
  - /axialy-production-admin/var/www/html/axialy-admin/includes/db_connection.php
  - /axialy-production-admin/var/www/html/axialy-admin/includes/environment_selector.php
  - /axialy-production-admin/var/www/html/axialy-admin/includes/ui_db_connection.php

Purpose:
This file serves as the technical documentation (README) for the 'includes' directory of the Axialy Admin Product. Its purpose is to define and describe the foundational PHP modules required for the system's administrative operations, including database connectivity, authentication/authorization services, configuration management, and environment detection. It acts as a manifest for the directory's contents, outlining how each file contributes to the platform's security, modularity, and database interaction.

Raw AI response:
{
  "referenced_files": [
    "/axialy-production-admin/var/www/html/axialy-admin/includes/AdminDBConfig.php",
    "/axialy-production-admin/var/www/html/axialy-admin/includes/Config.php",
    "/axialy-production-admin/var/www/html/axialy-admin/includes/admin_auth.php",
    "/axialy-production-admin/var/www/html/axialy-admin/includes/db_connection.php",
    "/axialy-production-admin/var/www/html/axialy-admin/includes/environment_selector.php",
    "/axialy-production-admin/var/www/html/axialy-admin/includes/ui_db_connection.php"
  ],
  "purpose": "This file serves as the technical documentation (README) for the 'includes' directory of the Axialy Admin Product. Its purpose is to define and describe the foundational PHP modules required for the system's administrative operations, including database connectivity, authentication/authorization services, configuration management, and environment detection. It acts as a manifest for the directory's contents, outlining how each file contributes to the platform's security, modularity, and database interaction."
}

-------------------------------------------------
File #17
Path: /axialy-production-admin/var/www/html/axialy-admin/includes/ui_db_connection.php

Referenced files:
  - /axialy-production-admin/var/www/html/axialy-admin/.env

Purpose:
The purpose of this file is to establish a dynamic PDO database connection for the Axialy Admin UI. It functions as a central utility that parses configuration from a `.env` file, detects available deployment environments, and selects the appropriate database connection parameters based on the current user session or server defaults. It ensures that the admin interface can interact with multiple backend environments seamlessly while providing error handling and configuration fallback mechanisms.

Raw AI response:
{
  "referenced_files": [
    "/axialy-production-admin/var/www/html/axialy-admin/.env"
  ],
  "purpose": "The purpose of this file is to establish a dynamic PDO database connection for the Axialy Admin UI. It functions as a central utility that parses configuration from a `.env` file, detects available deployment environments, and selects the appropriate database connection parameters based on the current user session or server defaults. It ensures that the admin interface can interact with multiple backend environments seamlessly while providing error handling and configuration fallback mechanisms."
}

-------------------------------------------------
File #18
Path: /axialy-production-admin/var/www/html/axialy-admin/.env

Referenced files:
  (none)

Purpose:
This file is a central configuration environment file (.env) for the Axialy administration system. Its primary purpose is to store sensitive environment-specific variables, including database credentials (for both the admin-specific database and multiple UI environments: Production, Test, and Dev), SMTP email delivery settings, default administrative user credentials, and global application environment state (e.g., CURRENT_ENVIRONMENT). It serves as the single source of truth for the application's infrastructure connectivity and authentication configuration.

Raw AI response:
{
  "referenced_files": [],
  "purpose": "This file is a central configuration environment file (.env) for the Axialy administration system. Its primary purpose is to store sensitive environment-specific variables, including database credentials (for both the admin-specific database and multiple UI environments: Production, Test, and Dev), SMTP email delivery settings, default administrative user credentials, and global application environment state (e.g., CURRENT_ENVIRONMENT). It serves as the single source of truth for the application's infrastructure connectivity and authentication configuration."
}

-------------------------------------------------
File #19
Path: /axialy-production-admin/var/www/html/axialy-admin/.htaccess

Referenced files:
  - /axialy-production-admin/var/www/html/axialy-admin/sitemap.php

Purpose:
This file serves as a server configuration file for Apache, specifically designed to handle URL rewriting. Its primary purpose is to intercept requests for 'sitemap.xml' and internally route them to 'sitemap.php', allowing for the dynamic generation or serving of the sitemap while maintaining a clean URL structure for search engine crawlers.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-admin/var/www/html/axialy-admin/sitemap.php"
  ],
  "purpose": "This file serves as a server configuration file for Apache, specifically designed to handle URL rewriting. Its primary purpose is to intercept requests for 'sitemap.xml' and internally route them to 'sitemap.php', allowing for the dynamic generation or serving of the sitemap while maintaining a clean URL structure for search engine crawlers."
}
```

-------------------------------------------------
File #20
Path: /axialy-production-admin/var/www/html/axialy-admin/admin_login.http.php

Referenced files:
  - /axialy-production-admin/var/www/html/axialy-admin/includes/AdminDBConfig.php

Purpose:
This file serves as the administrative authentication gateway for the system. It handles secure session initialization, processes user login credentials against the 'admin_users' database table, enforces account status checks, and manages the creation of new persistent session records in the 'admin_user_sessions' table upon successful authentication. It also implements session persistence logic (handling cookie scenarios and SID resurrection) and provides the UI form for user login.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-admin/var/www/html/axialy-admin/includes/AdminDBConfig.php"
  ],
  "purpose": "This file serves as the administrative authentication gateway for the system. It handles secure session initialization, processes user login credentials against the 'admin_users' database table, enforces account status checks, and manages the creation of new persistent session records in the 'admin_user_sessions' table upon successful authentication. It also implements session persistence logic (handling cookie scenarios and SID resurrection) and provides the UI form for user login."
}
```

-------------------------------------------------
File #21
Path: /axialy-production-admin/var/www/html/axialy-admin/admin_login.php

Referenced files:
  - /axialy-production-admin/var/www/html/axialy-admin/includes/AdminDBConfig.php

Purpose:
This file serves as the authentication gateway for the Axialy admin panel. It handles secure session initialization, enforces CSRF protection, validates admin credentials against the 'admin_users' database table, and manages user session persistence by creating entries in the 'admin_user_sessions' table upon successful login. It redirects authenticated users to 'index.php' and renders the login user interface for unauthenticated requests.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-admin/var/www/html/axialy-admin/includes/AdminDBConfig.php"
  ],
  "purpose": "This file serves as the authentication gateway for the Axialy admin panel. It handles secure session initialization, enforces CSRF protection, validates admin credentials against the 'admin_users' database table, and manages user session persistence by creating entries in the 'admin_user_sessions' table upon successful login. It redirects authenticated users to 'index.php' and renders the login user interface for unauthenticated requests."
}
```

-------------------------------------------------
File #22
Path: /axialy-production-admin/var/www/html/axialy-admin/create_minimal_docx.php

Referenced files:
  (none)

Purpose:
The file provides a utility function, `createDocxFromText()`, which generates a minimal, valid Microsoft Word DOCX file from a provided string. It accomplishes this by utilizing the PHP `ZipArchive` extension to construct the Open XML package structure (including necessary XML parts like [Content_Types].xml, relationship files, and document properties) and injecting the provided text into the core document body. It does not reference external physical files, as all structural XML content is defined within the functions contained in the file.

Raw AI response:
{
  "referenced_files": [],
  "purpose": "The file provides a utility function, `createDocxFromText()`, which generates a minimal, valid Microsoft Word DOCX file from a provided string. It accomplishes this by utilizing the PHP `ZipArchive` extension to construct the Open XML package structure (including necessary XML parts like [Content_Types].xml, relationship files, and document properties) and injecting the provided text into the core document body. It does not reference external physical files, as all structural XML content is defined within the functions contained in the file."
}

-------------------------------------------------
File #23
Path: /axialy-production-admin/var/www/html/axialy-admin/db_viewer_admin.php

Referenced files:
  - /axialy-production-admin/var/www/html/axialy-admin/includes/admin_auth.php
  - /axialy-production-admin/var/www/html/axialy-admin/includes/ui_db_connection.php
  - /axialy-production-admin/var/www/html/axialy-admin/assets/css/styles.css
  - /axialy-production-admin/var/www/html/axialy-admin/index.php
  - /axialy-production-admin/var/www/html/axialy-admin/assets/js/db_viewer_admin.js

Purpose:
This file serves as the administrative interface for viewing, filtering, and exporting data from the system's database. It enforces access control by requiring authentication via 'admin_auth.php' and initializes the database environment through 'ui_db_connection.php'. The file provides a browser-based dashboard featuring a table navigation panel and a dynamic content area where admins can query, filter, paginate, and export data in CSV format, with the frontend interactivity handled by the referenced JavaScript file.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-admin/var/www/html/axialy-admin/includes/admin_auth.php",
    "/axialy-production-admin/var/www/html/axialy-admin/includes/ui_db_connection.php",
    "/axialy-production-admin/var/www/html/axialy-admin/assets/css/styles.css",
    "/axialy-production-admin/var/www/html/axialy-admin/index.php",
    "/axialy-production-admin/var/www/html/axialy-admin/assets/js/db_viewer_admin.js"
  ],
  "purpose": "This file serves as the administrative interface for viewing, filtering, and exporting data from the system's database. It enforces access control by requiring authentication via 'admin_auth.php' and initializes the database environment through 'ui_db_connection.php'. The file provides a browser-based dashboard featuring a table navigation panel and a dynamic content area where admins can query, filter, paginate, and export data in CSV format, with the frontend interactivity handled by the referenced JavaScript file."
}
```

-------------------------------------------------
File #24
Path: /axialy-production-admin/var/www/html/axialy-admin/db_viewer_ajax.php

Referenced files:
  - /axialy-production-admin/var/www/html/axialy-admin/includes/admin_auth.php
  - /axialy-production-admin/var/www/html/axialy-admin/includes/ui_db_connection.php

Purpose:
This file serves as a backend AJAX controller for a database management dashboard. Its primary functions are to provide administrative access to view and export data from the application's UI database. It enforces admin authentication, handles table discovery (listing tables and row counts), performs paginated data retrieval (with logic to exclude or handle binary/BLOB columns to prevent JSON serialization errors), and provides a CSV export feature that includes basic filtering capabilities.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-admin/var/www/html/axialy-admin/includes/admin_auth.php",
    "/axialy-production-admin/var/www/html/axialy-admin/includes/ui_db_connection.php"
  ],
  "purpose": "This file serves as a backend AJAX controller for a database management dashboard. Its primary functions are to provide administrative access to view and export data from the application's UI database. It enforces admin authentication, handles table discovery (listing tables and row counts), performs paginated data retrieval (with logic to exclude or handle binary/BLOB columns to prevent JSON serialization errors), and provides a CSV export feature that includes basic filtering capabilities."
}
```

-------------------------------------------------
File #25
Path: /axialy-production-admin/var/www/html/axialy-admin/desktop.php

Referenced files:
  - /axialy-production-admin/var/www/html/axialy-admin/includes/AdminDBConfig.php
  - /axialy-production-admin/var/www/html/axialy-admin/init_user.php
  - /axialy-production-admin/var/www/html/axialy-admin/includes/admin_auth.php
  - /index.php
  - /logout.php
  - /docs_admin.php
  - /promo_codes_admin.php
  - /issues_admin.php
  - /db_viewer_admin.php

Purpose:
This file serves as the main dashboard and entry point for the Axialy Admin interface. Its primary functions are: 1) To enforce an initial system 'bootstrap' by checking for the existence of a specific admin user and providing an overlay to initialize the account if missing. 2) To serve as a gatekeeper for administrative access by requiring authentication via 'includes/admin_auth.php'. 3) To provide a central UI for administrators to toggle between different application environments (e.g., production, beta, UAT) via session-managed variables. 4) To act as a navigation hub, providing links to various administrative modules like documentation management, promo code management, issue tracking, and a database inspector.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-admin/var/www/html/axialy-admin/includes/AdminDBConfig.php",
    "/axialy-production-admin/var/www/html/axialy-admin/init_user.php",
    "/axialy-production-admin/var/www/html/axialy-admin/includes/admin_auth.php",
    "/index.php",
    "/logout.php",
    "/docs_admin.php",
    "/promo_codes_admin.php",
    "/issues_admin.php",
    "/db_viewer_admin.php"
  ],
  "purpose": "This file serves as the main dashboard and entry point for the Axialy Admin interface. Its primary functions are: 1) To enforce an initial system 'bootstrap' by checking for the existence of a specific admin user and providing an overlay to initialize the account if missing. 2) To serve as a gatekeeper for administrative access by requiring authentication via 'includes/admin_auth.php'. 3) To provide a central UI for administrators to toggle between different application environments (e.g., production, beta, UAT) via session-managed variables. 4) To act as a navigation hub, providing links to various administrative modules like documentation management, promo code management, issue tracking, and a database inspector."
}
```

-------------------------------------------------
File #26
Path: /axialy-production-admin/var/www/html/axialy-admin/docs_admin.php

Referenced files:
  - /axialy-production-admin/var/www/html/axialy-admin/includes/admin_auth.php
  - /axialy-production-admin/var/www/html/axialy-admin/includes/ui_db_connection.php
  - /axialy-production-admin/var/www/html/axialy-admin/assets/css/styles.css
  - /axialy-production-admin/var/www/html/axialy-admin/assets/js/docs_admin.js
  - /axialy-production-admin/var/www/html/axialy-admin/index.php

Purpose:
This file serves as the administrative dashboard interface for managing system documentation. It provides a UI for creating and editing document records, managing version history (supporting various formats like Markdown, HTML, JSON, and XML), and uploading supporting documentation files (PDF/DOCX). The script enforces administrative authentication via 'admin_auth.php' and establishes a database connection via 'ui_db_connection.php' to facilitate these operations.

Raw AI response:
{
  "referenced_files": [
    "/axialy-production-admin/var/www/html/axialy-admin/includes/admin_auth.php",
    "/axialy-production-admin/var/www/html/axialy-admin/includes/ui_db_connection.php",
    "/axialy-production-admin/var/www/html/axialy-admin/assets/css/styles.css",
    "/axialy-production-admin/var/www/html/axialy-admin/assets/js/docs_admin.js",
    "/axialy-production-admin/var/www/html/axialy-admin/index.php"
  ],
  "purpose": "This file serves as the administrative dashboard interface for managing system documentation. It provides a UI for creating and editing document records, managing version history (supporting various formats like Markdown, HTML, JSON, and XML), and uploading supporting documentation files (PDF/DOCX). The script enforces administrative authentication via 'admin_auth.php' and establishes a database connection via 'ui_db_connection.php' to facilitate these operations."
}

-------------------------------------------------
File #27
Path: /axialy-production-admin/var/www/html/axialy-admin/doc_ajax_actions.php

Referenced files:
  - /axialy-production-admin/var/www/html/axialy-admin/includes/admin_auth.php
  - /axialy-production-admin/var/www/html/axialy-admin/includes/ui_db_connection.php

Purpose:
This file serves as a centralized AJAX controller (API endpoint) for document management tasks within the admin interface. It processes requests (via GET or POST) to perform CRUD operations on document metadata and versions, including creating new documents, managing version history, generating/triggering file creation (PDF/DOCX), and uploading or downloading document-level binary files. It ensures authorized access via the included authentication and database connection files.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-admin/var/www/html/axialy-admin/includes/admin_auth.php",
    "/axialy-production-admin/var/www/html/axialy-admin/includes/ui_db_connection.php"
  ],
  "purpose": "This file serves as a centralized AJAX controller (API endpoint) for document management tasks within the admin interface. It processes requests (via GET or POST) to perform CRUD operations on document metadata and versions, including creating new documents, managing version history, generating/triggering file creation (PDF/DOCX), and uploading or downloading document-level binary files. It ensures authorized access via the included authentication and database connection files."
}
```

-------------------------------------------------
File #28
Path: /axialy-production-admin/var/www/html/axialy-admin/index.php

Referenced files:
  - /axialy-production-admin/var/www/html/axialy-admin/includes/AdminDBConfig.php
  - /axialy-production-admin/var/www/html/axialy-admin/.env
  - /axialy-production-admin/var/www/html/axialy-admin/init_user.php
  - /axialy-production-admin/var/www/html/axialy-admin/includes/admin_auth.php
  - /axialy-production-admin/var/www/html/axialy-admin/assets/css/styles.css
  - /axialy-production-admin/var/www/html/axialy-admin/logout.php
  - /axialy-production-admin/var/www/html/axialy-admin/docs_admin.php
  - /axialy-production-admin/var/www/html/axialy-admin/promo_codes_admin.php
  - /axialy-production-admin/var/www/html/axialy-admin/issues_admin.php
  - /axialy-production-admin/var/www/html/axialy-admin/db_viewer_admin.php
  - /axialy-production-admin/var/www/html/axialy-admin/assets/js/dashboard.js

Purpose:
This file serves as the main entry point and administrative dashboard for the Axialy Admin interface. Its primary responsibilities include: 1) Performing a one-time system bootstrap to initialize the first admin user; 2) Managing dynamic environment discovery based on server secrets or a local .env file; 3) Enforcing authentication via 'includes/admin_auth.php'; 4) Providing a dashboard interface to switch between configured environments and access various administrative sub-modules (Documentation, Promo Codes, Issue Management, and Database Inspection).

Raw AI response:
{
  "referenced_files": [
    "/axialy-production-admin/var/www/html/axialy-admin/includes/AdminDBConfig.php",
    "/axialy-production-admin/var/www/html/axialy-admin/.env",
    "/axialy-production-admin/var/www/html/axialy-admin/init_user.php",
    "/axialy-production-admin/var/www/html/axialy-admin/includes/admin_auth.php",
    "/axialy-production-admin/var/www/html/axialy-admin/assets/css/styles.css",
    "/axialy-production-admin/var/www/html/axialy-admin/logout.php",
    "/axialy-production-admin/var/www/html/axialy-admin/docs_admin.php",
    "/axialy-production-admin/var/www/html/axialy-admin/promo_codes_admin.php",
    "/axialy-production-admin/var/www/html/axialy-admin/issues_admin.php",
    "/axialy-production-admin/var/www/html/axialy-admin/db_viewer_admin.php",
    "/axialy-production-admin/var/www/html/axialy-admin/assets/js/dashboard.js"
  ],
  "purpose": "This file serves as the main entry point and administrative dashboard for the Axialy Admin interface. Its primary responsibilities include: 1) Performing a one-time system bootstrap to initialize the first admin user; 2) Managing dynamic environment discovery based on server secrets or a local .env file; 3) Enforcing authentication via 'includes/admin_auth.php'; 4) Providing a dashboard interface to switch between configured environments and access various administrative sub-modules (Documentation, Promo Codes, Issue Management, and Database Inspection)."
}

-------------------------------------------------
File #29
Path: /axialy-production-admin/var/www/html/axialy-admin/init_user.php

Referenced files:
  - /axialy-production-admin/var/www/html/axialy-admin/.env
  - /axialy-production-admin/var/www/html/axialy-admin/includes/AdminDBConfig.php

Purpose:
This file serves as a one-time administrative bootstrap script designed to initialize the first system administrator account in the `admin_users` database table. It validates an 'initialization_code' provided via a POST request against an 'ADMIN_DEFAULT_PASSWORD' defined in the environment configuration. If the code matches and the user does not yet exist, it creates the admin record with BCRYPT-hashed credentials, effectively securing the initial access to the administrative system.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-admin/var/www/html/axialy-admin/.env",
    "/axialy-production-admin/var/www/html/axialy-admin/includes/AdminDBConfig.php"
  ],
  "purpose": "This file serves as a one-time administrative bootstrap script designed to initialize the first system administrator account in the `admin_users` database table. It validates an 'initialization_code' provided via a POST request against an 'ADMIN_DEFAULT_PASSWORD' defined in the environment configuration. If the code matches and the user does not yet exist, it creates the admin record with BCRYPT-hashed credentials, effectively securing the initial access to the administrative system."
}
```

-------------------------------------------------
File #30
Path: /axialy-production-admin/var/www/html/axialy-admin/issues_admin.php

Referenced files:
  - /axialy-production-admin/var/www/html/axialy-admin/includes/admin_auth.php
  - /axialy-production-admin/var/www/html/axialy-admin/assets/css/styles.css
  - /axialy-production-admin/var/www/html/axialy-admin/index.php
  - /axialy-production-admin/var/www/html/axialy-admin/assets/js/issues_admin.js

Purpose:
This file serves as the administrative interface for managing user-reported issues. It enforces authentication via the 'admin_auth.php' include and provides a two-pane layout: the left pane displays a list of issues (dynamically populated via client-side script), and the right pane provides a detailed form for editing issue metadata (title, description, status) and sending direct emails to the relevant user. The logic for data fetching, form handling, and AJAX requests is delegated to the linked 'issues_admin.js' file.

Raw AI response:
{
  "referenced_files": [
    "/axialy-production-admin/var/www/html/axialy-admin/includes/admin_auth.php",
    "/axialy-production-admin/var/www/html/axialy-admin/assets/css/styles.css",
    "/axialy-production-admin/var/www/html/axialy-admin/index.php",
    "/axialy-production-admin/var/www/html/axialy-admin/assets/js/issues_admin.js"
  ],
  "purpose": "This file serves as the administrative interface for managing user-reported issues. It enforces authentication via the 'admin_auth.php' include and provides a two-pane layout: the left pane displays a list of issues (dynamically populated via client-side script), and the right pane provides a detailed form for editing issue metadata (title, description, status) and sending direct emails to the relevant user. The logic for data fetching, form handling, and AJAX requests is delegated to the linked 'issues_admin.js' file."
}

-------------------------------------------------
File #31
Path: /axialy-production-admin/var/www/html/axialy-admin/issues_ajax_actions.php

Referenced files:
  - /axialy-production-admin/var/www/html/axialy-admin/includes/admin_auth.php
  - /axialy-production-admin/var/www/html/axialy-admin/includes/ui_db_connection.php
  - /axialy-production-admin/var/www/html/axialy-admin/includes/AdminDBConfig.php

Purpose:
This file acts as a backend AJAX controller for managing support issues within the admin dashboard. It provides an interface to list, retrieve details for, update, and communicate (via email) regarding user-submitted issues. It relies on internal session-based authentication to verify administrative access and uses distinct database connections to handle data from both the user interface system (via $pdoUI) and the internal admin database (via AdminDBConfig) to facilitate ticket resolution workflows.

Raw AI response:
{
  "referenced_files": [
    "/axialy-production-admin/var/www/html/axialy-admin/includes/admin_auth.php",
    "/axialy-production-admin/var/www/html/axialy-admin/includes/ui_db_connection.php",
    "/axialy-production-admin/var/www/html/axialy-admin/includes/AdminDBConfig.php"
  ],
  "purpose": "This file acts as a backend AJAX controller for managing support issues within the admin dashboard. It provides an interface to list, retrieve details for, update, and communicate (via email) regarding user-submitted issues. It relies on internal session-based authentication to verify administrative access and uses distinct database connections to handle data from both the user interface system (via $pdoUI) and the internal admin database (via AdminDBConfig) to facilitate ticket resolution workflows."
}

-------------------------------------------------
File #32
Path: /axialy-production-admin/var/www/html/axialy-admin/logout.php

Referenced files:
  - /axialy-production-admin/var/www/html/axialy-admin/includes/AdminDBConfig.php

Purpose:
This file handles the administrative logout process for the application. It performs three main tasks: it retrieves the database connection via `AdminDBConfig` to invalidate the active session record in the `admin_user_sessions` database table, it clears the local PHP session state using `session_destroy()`, and it redirects the user to the login page (`/admin_login.php`) with a `logged_out` query parameter.

Raw AI response:
{
  "referenced_files": [
    "/axialy-production-admin/var/www/html/axialy-admin/includes/AdminDBConfig.php"
  ],
  "purpose": "This file handles the administrative logout process for the application. It performs three main tasks: it retrieves the database connection via `AdminDBConfig` to invalidate the active session record in the `admin_user_sessions` database table, it clears the local PHP session state using `session_destroy()`, and it redirects the user to the login page (`/admin_login.php`) with a `logged_out` query parameter."
}

-------------------------------------------------
File #33
Path: /axialy-production-admin/var/www/html/axialy-admin/promo_codes_admin.php

Referenced files:
  - /axialy-production-admin/var/www/html/axialy-admin/includes/admin_auth.php
  - /axialy-production-admin/var/www/html/axialy-admin/assets/css/styles.css
  - /axialy-production-admin/var/www/html/axialy-admin/index.php
  - /axialy-production-admin/var/www/html/axialy-admin/assets/js/promo_codes_admin.js

Purpose:
This file serves as the administrative interface for managing promotional codes within the Axialy system. It provides a UI for administrators to create, view, and edit promo codes, supporting different configurations such as unlimited access, time-limited access, and Stripe-integrated discounted pricing. It enforces authentication via a required include and manages the front-end state of forms for handling promo code metadata like usage limits, validity dates, and status.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-admin/var/www/html/axialy-admin/includes/admin_auth.php",
    "/axialy-production-admin/var/www/html/axialy-admin/assets/css/styles.css",
    "/axialy-production-admin/var/www/html/axialy-admin/index.php",
    "/axialy-production-admin/var/www/html/axialy-admin/assets/js/promo_codes_admin.js"
  ],
  "purpose": "This file serves as the administrative interface for managing promotional codes within the Axialy system. It provides a UI for administrators to create, view, and edit promo codes, supporting different configurations such as unlimited access, time-limited access, and Stripe-integrated discounted pricing. It enforces authentication via a required include and manages the front-end state of forms for handling promo code metadata like usage limits, validity dates, and status."
}
```

-------------------------------------------------
File #34
Path: /axialy-production-admin/var/www/html/axialy-admin/promo_codes_ajax_actions.php

Referenced files:
  - /axialy-production-admin/var/www/html/axialy-admin/includes/admin_auth.php
  - /axialy-production-admin/var/www/html/axialy-admin/includes/ui_db_connection.php

Purpose:
This file serves as a backend controller for managing promotional codes within the admin panel via AJAX. It provides a centralized interface for listing, retrieving, creating, and updating promo codes in the `promo_codes` database table. The script handles validation—specifically supporting different promo code types (unlimited, limited-duration, or discounted pricing)—and ensures that only authorized administrators can perform these operations by enforcing session-based authentication.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-admin/var/www/html/axialy-admin/includes/admin_auth.php",
    "/axialy-production-admin/var/www/html/axialy-admin/includes/ui_db_connection.php"
  ],
  "purpose": "This file serves as a backend controller for managing promotional codes within the admin panel via AJAX. It provides a centralized interface for listing, retrieving, creating, and updating promo codes in the `promo_codes` database table. The script handles validation—specifically supporting different promo code types (unlimited, limited-duration, or discounted pricing)—and ensures that only authorized administrators can perform these operations by enforcing session-based authentication."
}
```

-------------------------------------------------
File #35
Path: /axialy-production-admin/var/www/html/axialy-admin/README.md

Referenced files:
  - /axialy-production-admin/var/www/html/axialy-admin/admin_login.php
  - /axialy-production-admin/var/www/html/axialy-admin/admin_login.http.php
  - /axialy-production-admin/var/www/html/axialy-admin/create_minimal_docx.php
  - /axialy-production-admin/var/www/html/axialy-admin/db_viewer_admin.php
  - /axialy-production-admin/var/www/html/axialy-admin/db_viewer_ajax.php
  - /axialy-production-admin/var/www/html/axialy-admin/doc_ajax_actions.php
  - /axialy-production-admin/var/www/html/axialy-admin/docs_admin.php
  - /axialy-production-admin/var/www/html/axialy-admin/favicon.ico
  - /axialy-production-admin/var/www/html/axialy-admin/index.php
  - /axialy-production-admin/var/www/html/axialy-admin/init_user.php
  - /axialy-production-admin/var/www/html/axialy-admin/issues_admin.php
  - /axialy-production-admin/var/www/html/axialy-admin/issues_ajax_actions.php
  - /axialy-production-admin/var/www/html/axialy-admin/logout.php
  - /axialy-production-admin/var/www/html/axialy-admin/promo_codes_admin.php
  - /axialy-production-admin/var/www/html/axialy-admin/promo_codes_ajax_actions.php
  - /axialy-production-admin/var/www/html/axialy-admin/includes/

Purpose:
This file serves as the master documentation (README.md) for the Axialy Admin Product. It outlines the architectural, functional, and operational requirements of the administrative interface, which acts as the central control panel for managing the Axialy AI platform's databases, user sessions, documentation lifecycle, support tickets, and promotional marketing codes.

Raw AI response:
```json
{
  "referenced_files": [
    "/axialy-production-admin/var/www/html/axialy-admin/admin_login.php",
    "/axialy-production-admin/var/www/html/axialy-admin/admin_login.http.php",
    "/axialy-production-admin/var/www/html/axialy-admin/create_minimal_docx.php",
    "/axialy-production-admin/var/www/html/axialy-admin/db_viewer_admin.php",
    "/axialy-production-admin/var/www/html/axialy-admin/db_viewer_ajax.php",
    "/axialy-production-admin/var/www/html/axialy-admin/doc_ajax_actions.php",
    "/axialy-production-admin/var/www/html/axialy-admin/docs_admin.php",
    "/axialy-production-admin/var/www/html/axialy-admin/favicon.ico",
    "/axialy-production-admin/var/www/html/axialy-admin/index.php",
    "/axialy-production-admin/var/www/html/axialy-admin/init_user.php",
    "/axialy-production-admin/var/www/html/axialy-admin/issues_admin.php",
    "/axialy-production-admin/var/www/html/axialy-admin/issues_ajax_actions.php",
    "/axialy-production-admin/var/www/html/axialy-admin/logout.php",
    "/axialy-production-admin/var/www/html/axialy-admin/promo_codes_admin.php",
    "/axialy-production-admin/var/www/html/axialy-admin/promo_codes_ajax_actions.php",
    "/axialy-production-admin/var/www/html/axialy-admin/includes/"
  ],
  "purpose": "This file serves as the master documentation (README.md) for the Axialy Admin Product. It outlines the architectural, functional, and operational requirements of the administrative interface, which acts as the central control panel for managing the Axialy AI platform's databases, user sessions, documentation lifecycle, support tickets, and promotional marketing codes."
}
```

-------------------------------------------------
File #36
Path: /axialy-production-admin/var/www/html/archive-test.txt

Referenced files:
  (none)

Purpose:
This file is a plain text file containing only the string 'archive-test'. Based on its location in the '/var/www/html/' directory and its filename, it serves as a simple diagnostic or placeholder file likely used to verify web server accessibility or to test file system interactions within the production environment.

Raw AI response:
{
  "referenced_files": [],
  "purpose": "This file is a plain text file containing only the string 'archive-test'. Based on its location in the '/var/www/html/' directory and its filename, it serves as a simple diagnostic or placeholder file likely used to verify web server accessibility or to test file system interactions within the production environment."
}

-------------------------------------------------