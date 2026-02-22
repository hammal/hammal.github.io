# Hampus Malmberg — Academic Website

Personal academic website of [Hampus Malmberg](https://hammal.github.io), postdoctoral researcher at the [Signal and Information Processing Laboratory (ISI)](https://isi.ee.ethz.ch), ETH Zürich, and guest researcher at [NTNU Trondheim](https://www.ntnu.edu).

Built with [Jekyll](https://jekyllrb.com) using the [al-folio](https://github.com/alshedivat/al-folio) theme.

---

## Research

- Control-bounded analog-to-digital and digital-to-analog converters
- Factor graphs and Gaussian message passing
- Model-based signal processing and sparse recovery

---

## Running Locally

**Prerequisites:** Ruby, Bundler, ImageMagick

```bash
bundle install
bundle exec jekyll serve
```

The site will be available at `http://localhost:4000`.

---

## Structure

| Path | Contents |
|---|---|
| `_pages/` | Static pages (about, publications, CV, projects, talks) |
| `_bibliography/papers.bib` | Publications (rendered via jekyll-scholar) |
| `_news/` | News and announcements |
| `_projects/` | Research project pages |
| `_data/cv.yml` | CV content |
| `_data/coauthors.yml` | Coauthor name → profile URL mapping |
| `_data/supervision.yml` | Student supervision records |
| `_data/talks.yml` | Talks and presentations |
| `assets/img/` | Images |
| `_config.yml` | Site configuration |

---

## Keeping Up with al-folio

This site tracks the upstream [al-folio](https://github.com/alshedivat/al-folio) template. To update the template infrastructure while preserving personal content:

```bash
git remote add upstream https://github.com/alshedivat/al-folio.git
git fetch upstream

# Take upstream template files (adjust paths as needed)
git checkout upstream/master -- _includes/ _layouts/ _sass/ _plugins/
git checkout upstream/master -- assets/js/ assets/css/ assets/fonts/ assets/webfonts/
git checkout upstream/master -- Gemfile bin/ package.json requirements.txt

# Manually merge _config.yml to preserve personal settings
```

Personal content (`_pages/`, `_news/`, `_projects/`, `_bibliography/`, `_data/`, `assets/img/`) is never taken from upstream.

---

## License

The al-folio theme is available under the [MIT License](https://opensource.org/licenses/MIT).
Site content (text, images, publications) is copyright Hampus Malmberg.
