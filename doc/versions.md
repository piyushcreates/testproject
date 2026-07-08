# Version History

All notable changes to the **Social Masla** project will be documented in this file. This project adheres to Semantic Versioning (`MAJOR.MINOR.PATCH`).

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
