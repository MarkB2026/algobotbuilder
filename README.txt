BUILDTRADINGBOTS PRIVATE BETA PAGES

1. Upload basic.html to the ROOT of the public website repository, replacing the existing file.
2. Upload premium_public_landing_index.html as /premium/index.html in the public website repository. If your public premium page is /premium.html, also use this landing HTML to replace /premium.html (rename to premium.html).
3. Place the supplied premium.html inside a private, unlinked directory only AFTER configuring actual access restrictions (e.g., Cloudflare Access and server-side Worker authorization). A random directory name alone does not protect it.
4. Keep the private URL out of public navigation, sitemaps, and README files. A static GitHub Pages site cannot itself enforce authenticated access; Cloudflare Access requires routing the domain through Cloudflare and protecting the path.
5. The Worker must reject unauthorized Premium-schema build requests independently of the HTML page. This package does NOT change or deploy the Worker, and does NOT implement access control. Do not distribute the private URL until that is configured.
6. Existing website build JavaScript, payment and condition serialization were left intact. Test a Basic PAPER build and Premium PAPER build before inviting testers.
7. GitHub Actions run #129 was successful according to the supplied screenshot, but the screenshot does not prove which schema or entry conditions were packaged; inspect its plan and artifact before release.
