# Personal Site Starter (Academic Pages)

This repository is a cleaned version of the Academic Pages Jekyll theme. All template content that described someone else has been removed so you can focus on adding your own details.

## Quick Start
1. Install Ruby and Bundler (see instructions in `CONTRIBUTING.md` or the Academic Pages docs if needed).
2. Install dependencies: `bundle install`.
3. Run locally: `bundle exec jekyll serve -l -H localhost` and open http://localhost:4000.
4. Edit the files listed below to publish your own information, then push to GitHub (or any static host that supports Jekyll).

## Files You Should Update First
- `_config.yml`: site title, description, sidebar profile, social links, analytics, etc.
- `_data/navigation.yml`: top navigation items; remove sections you do not use.
- `images/profile.png`: replace with a square headshot. Update other icons in `images/` as desired.
- `_pages/about.md`: landing page copy. Fill in your introduction, current work, and contact details.
- `_pages/cv.md`: long-form résumé in Markdown. Replace every `待补充` item with your history.
- `_data/cv.json`: machine-readable CV. Fill this if you want `/cv-json/` or automated exports.

## Optional Content Areas
Add Markdown/HTML files to these folders to enable each section:
- `_posts/`: blog posts (filename format `YYYY-MM-DD-title.md`).
- `_publications/`: scholarly outputs; each file becomes an entry on `/publications/` and the CV page.
- `_talks/`: talks and presentations. After adding content, regenerate the map (`talkmap.ipynb` or `talkmap.py`).
- `_teaching/`: teaching experience list used on `/teaching/` and within the CV.
- `_portfolio/`: portfolio/project highlights surfaced on `/portfolio/`.
- `_projects/`: long-form project write-ups if you enable a projects page.
- `files/`: supporting PDFs (CV, slides, papers) referenced from your pages.

All of these directories are currently empty so that no third-party details appear on the site. When a directory has no items, its corresponding page still builds but will show only headings—hide the link from `_data/navigation.yml` if you prefer.

## Styling and Layout
- `_sass/` and `assets/css/main.scss`: customize colors, typography, and layout.
- `_includes/` and `_layouts/`: advanced edits to shared components (nav, sidebar, page templates).

## Data Sources & Automation
- `markdown_generator/`: optional notebooks and scripts that transform TSV/CSV data into Markdown files for publications and talks.
- `talkmap/`: generated assets for the talk location map. The default `org-locations.js` is empty; populate it by running `talkmap.py` (requires API access for geocoding).

## Housekeeping
- Delete pages in `_pages/` that you do not plan to use (e.g., `markdown.md`, archive templates) and remove their entries from `_data/navigation.yml`.
- Update `LICENSE` or add attribution if you change theme licensing.
- Consider using `scripts/update_cv_json.sh` to convert `_pages/cv.md` to the JSON format when you make significant updates.

With these edits, your site will be free of placeholder data and ready to publish your own profile.
