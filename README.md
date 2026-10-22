# Eval Apply Consulting — landing page

A static page for GitHub Pages: `index.html`, the Eval Apply logo (`logo.png`, `favicon-32.png`, `apple-touch-icon.png`),
Hugging Face's logo for its link (`hf-logo.svg`), and `.nojekyll` so Pages serves the files as they are.

## Publishing

1. Push this folder to a GitHub repository (e.g. `eval-apply-labs/evalapply-consulting`).
2. Settings → Pages → Build and deployment: *Deploy from a branch*, `main`, `/ (root)`.
3. Your domain: in the same page, set *Custom domain* (GitHub adds a `CNAME` file to the repository), then at the DNS host:
   - the apex (`example.co.uk`): `A` records to `185.199.108.153`, `185.199.109.153`, `185.199.110.153`,
     `185.199.111.153` (and `AAAA` to `2606:50c0:8000::153`, `…8001::153`, `…8002::153`, `…8003::153`);
   - `www`: a `CNAME` to `eval-apply-labs.github.io`.
   Existing `MX` records (the mail) are not touched by either. Once the certificate is issued, tick *Enforce HTTPS*.

Serving the page on the domain itself (a custom domain) rather than a redirect to `github.io` keeps the company's
domain in the address bar, which is what a verifier such as Dun & Bradstreet looks for.

The footer is the company's record at Companies House:
<https://find-and-update.company-information.service.gov.uk/company/17370805>.
