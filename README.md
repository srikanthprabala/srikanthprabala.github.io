# srikanthprabala.github.io

Personal site. Currently a landing page plus the CV.

## Stable URL, do not break this

`https://srikanthprabala.github.io/cv.pdf` is handed out on reviewer applications, IEEE
forms, and to journal editors. It has to keep resolving regardless of how the site evolves.

## Updating the CV

```bash
cp /path/to/new/cv.pdf cv.pdf
git commit -am "Update CV"
git push
```

Same URL, so links already sitting in other people's records stay current. LaTeX source is
`cv.tex`, kept outside this repo.

## If this becomes a full site later

Any static setup works: Jekyll, Hugo, Astro, or plain HTML. One thing to preserve: keep
`cv.pdf` at the repo root. Static site generators pass unknown file types through
untouched, so this usually needs no configuration. If you add a Jekyll `_config.yml`, check
that `exclude` does not swallow `cv.pdf`.

A custom domain is fine too. Add a `CNAME` file and GitHub redirects
`srikanthprabala.github.io` to it, so existing links continue to resolve.

If you later host the job-hunting resume as well, name it `resume.pdf` so the two stay
distinct.
