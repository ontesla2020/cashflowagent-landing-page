# cashflowagent.ai website

Static site. No build step. Files:

- index.html: the whole page
- assets/: screenshots, photo, QR code, demo call audio
- CNAME: tells GitHub Pages the custom domain (www.cashflowagent.ai)

## Publish on GitHub Pages

1. Create a new GitHub repo (for example cashflowagent-site) and upload everything in this folder, keeping the assets folder.
2. In the repo go to Settings, then Pages. Under Build and deployment choose Deploy from a branch, branch main, folder / (root). Save.
3. Under Custom domain enter www.cashflowagent.ai and save. Tick Enforce HTTPS once it becomes available.

## Point the domain (at your domain registrar)

- CNAME record: host www, value YOUR-GITHUB-USERNAME.github.io
- For the bare domain cashflowagent.ai add four A records (host @) to GitHub Pages: 185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153. Also set the registrar to forward the bare domain to www if it offers that.
- DNS can take from a few minutes to a day. Check the current values in GitHub's docs, "Managing a custom domain for your GitHub Pages site".

## Before going live

- Contact form: sign up at formspree.io, create a form, and replace REPLACE_WITH_YOUR_FORM_ID in the form action in index.html.
- FAQ: confirm the answer about how invoice data connects (search for CONFIRM).
- Demo link: the Live demo links go to /demo, which redirects to https://cashflowagent.onrender.com/ (change the address in demo/index.html if the app moves). Warm the app up before showing it.
- Add Privacy, Terms and Contact pages or links in the footer.
