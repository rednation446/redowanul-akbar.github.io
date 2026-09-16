# Portfolio site

Plain HTML/CSS/JS, no build step. Structure:

```
index.html
style.css
script.js
images/headshot.jpg
cv/Redowan_CV.pdf
```

## Before you publish — read this

`cv/Redowan_CV.pdf` is the exact file you sent me, and it still has your
**phone number**, **home address**, and the **phone numbers of your three
references**. That's normal for a CV you submit privately to an application
portal, but this repo will be public on the open internet and gets crawled
by search engines. Before pushing, swap in a version that:

- drops the phone number (or keep it if you're fine with that being public
  — your call, just make it a decision, not an accident)
- drops the home address
- changes "Phone: ..." under References to something like
  "Contact information available on request"

Everything else on the site (email, research, teaching, honors) is fine to
be public as written.

Also fill in your real links before publishing — search `index.html` for
the commented-out LinkedIn / Google Scholar / GitHub lines in the Contact
section and uncomment + edit the ones you have.

## Deploying to GitHub Pages

1. Create a new repository on GitHub. If you want it at
   `https://<your-username>.github.io`, name the repo exactly
   `<your-username>.github.io`. Otherwise any name works and it'll be served
   at `https://<your-username>.github.io/<repo-name>/`.

2. From this folder:
   ```bash
   git init
   git add .
   git commit -m "Initial portfolio site"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<repo-name>.git
   git push -u origin main
   ```

3. On GitHub: go to the repo's **Settings → Pages**. Under "Build and
   deployment", set Source to **Deploy from a branch**, branch **main**,
   folder **/(root)**. Save.

4. Wait a minute or two, then visit the URL GitHub shows you on that same
   Pages settings screen.

## Custom domain (optional)

If you get a domain later (many .edu-adjacent options, or a cheap
`.me`/`.dev`), add a `CNAME` file in this folder containing just your
domain name, and point your domain's DNS at GitHub Pages per
[GitHub's custom domain docs](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site).

## Updating later

Edit the HTML/CSS directly, commit, and push — GitHub Pages redeploys
automatically within a minute or two of every push to `main`.
