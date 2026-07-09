# Version History

All notable changes to the **Social Masla** project will be documented in this file. This project adheres to Semantic Versioning (`MAJOR.MINOR.PATCH`).

## [1.5.0] - 2026-07-09

### Removed
- Removed FormSubmit.co AJAX endpoint integration from both Home (`index.html`) and Contact (`contact.html`) pages.
- Removed automated email notifications to `hello@socialmasla.com` from form submissions.

### Changed
- Refactored form submission handlers to mock form submission client-side (with a simulated network delay) to prevent receiving emails from the project.
- Updated project documentation (`README.md`) to reflect the removal of external form submission endpoints.

## [1.4.0] - 2026-07-08

### Removed
- Removed Meta (Facebook) Pixel base scripts and PageView tracking from all pages.
- Removed custom Lead event tracking from the Home and Contact form submission handlers.

## [1.3.0] - 2026-07-08

### Added
- Standard robots meta tags (`noindex, nofollow, noarchive`) added to all pages to prevent search engines and AI crawlers from indexing or tracking the website.
- Updated `robots.txt` to explicitly disallow all user agents from crawling any directories.

## [1.2.0] - 2026-07-08

### Added
- Meta (Facebook) Pixel integration with ID `418549630012363` added across all static pages (`index.html`, `about.html`, `consultation.html`, `contact.html`).
- Standard `PageView` event tracked on every page load.
- Custom `Lead` event tracked on successful contact form submission on both the Home page (`index.html`) and Contact page (`contact.html`).

## [1.1.1] - 2026-07-08

### Changed
- Updated the primary hero tagline from "Less noise. More growth." to "Premium growth marketing consultancy" on the home (`index.html`) and about (`about.html`) pages.

## [1.1.0] - 2026-07-08

### Added
- JSON-LD structured data (schema markup) for Search Engines and AIs on all pages (`index.html`, `about.html`, `consultation.html`, `contact.html`).
- Canonical link tags and Open Graph / Twitter Card social metadata headers.
- Root crawler configurations: `robots.txt` and `sitemap.xml`.
- Web-optimized WebP asset `assets/piyush-sachdeva.webp` (~35KB), replacing the original raw PNG image (~5.6MB).

### Changed
- Improved page loading performance and visual stability by enforcing explicit dimensions (`width` and `height`) and resource prioritization attributes (`fetchpriority="high"`, `loading="eager"`, and `loading="lazy"`) on logo and founder image elements.
- Cleaned up remote repository by removing the heavy raw PNG founder photo.

## [1.0.0] - 2026-07-08

### Added
- Initial import of the static website code.
- Pages: `index.html`, `about.html`, `consultation.html`, `contact.html`.
- Asset files including logos, favicons, and founder photos.
- Initial `.gitignore` to exclude `.DS_Store` and `.claude/` directories.
- AI Agent Instructions (`doc/ai_agent_instructions.md`) and Version History (`doc/versions.md`).
