# Jaskrit Singh

Personal academic website using the al-folio v1 starter and its versioned `al_folio_core` runtime. The custom domain is `jaskrit.com`.

## Editing

- `index.html`: biography and homepage settings.
- `_bibliography/papers.bib`: publications, links, and summaries; `selected = {true}` displays a paper on the homepage.
- `_projects/`: research, entrepreneurship, and service projects.
- `_pages/cv.md`: education, experience, skills, and awards.
- `_data/socials.yml`: contact links.
- `_config.yml`: site and theme settings.
- `res/`: existing images, animations, and project PDFs.


## Local preview

Use Ruby 3.3+, Bundler 4.0.6, and Node.js 22. Linux or WSL2 is convenient; Windows editing works with Linux builds in GitHub Actions.

```sh
gem install bundler -v 4.0.6
bundle install
bundle exec jekyll serve
```

Open `http://localhost:4000/`. The domain is served at the root, so `baseurl` stays empty.

The imported template folder and `.local-tools/` are ignored by Git and excluded from the generated site. A backup of the pre-migration working copy is kept locally at `.local-tools/original-index.html`.

See `LICENSE-al-folio` for the starter's MIT license.
