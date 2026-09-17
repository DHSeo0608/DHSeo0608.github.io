# Donghee Seo — personal website

Website: <https://dhseo0608.github.io>

Built with [al-folio](https://github.com/alshedivat/al-folio), Jekyll, and GitHub Pages.

**수정 방법은 [EDITING_GUIDE.md](EDITING_GUIDE.md)를 확인하세요.**

## Content

- `_config.yml`: name, description, site settings
- `_pages/about.md`: home page and biography
- `_data/socials.yml`: social links
- `_bibliography/papers.bib`: publications
- `_projects/`: project pages
- `_data/cv.yml`: CV
- `assets/img/` and `assets/pdf/`: photos and documents

The original test page is preserved in `backup/index-test.html` and Git history
(commit `1984caa`). Backups and templates are excluded from the published site.

## Deployment

GitHub Pages source: **GitHub Actions**. Every push to `main` builds and deploys
the site using `.github/workflows/deploy.yml`. Only the generated `_site` artifact
is published. Pull requests build and validate without deploying.

## Template provenance

al-folio starter commit: `8ec1f3608d997491e0206c4e7a9368547a5ef255`.
Gem versions are recorded in `Gemfile` and `Gemfile.lock`. Original MIT license retained.
No theme runtime overrides.
