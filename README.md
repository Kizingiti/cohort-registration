Cohort Registration Site

A single self-contained page (index.html) for Kingdom Stewardship Experience registrations. No backend, no build step. It's the same page currently live at the claude.ai artifact link, moved here so it can be hosted under kizingiti.com instead.

Why this is its own thing

Deliberately kept separate from the Lovable-connected customer app repo (kizingiticapital-web/budget-buddy-hub-21), which is under a controlled publish process and has nothing to do with event registration, and from the Kizingiti Management Platform (kmp-phase1a, on Render), a live Node/Postgres business system with no reason to carry unrelated static marketing content. This folder is just a static file. It can be redeployed independently, as often as needed, with zero risk to either of those.

Reusing for future cohorts

Copy index.html to cohort6.html (etc.), update the date/venue/fee text and the WA_NUMBER constant if it ever changes, and redeploy. Each cohort can get its own path, or you can just overwrite index.html each time if you only ever need the current cohort live.

Deploy notes (Render Static Site, reusing the account already used for KMP)

Connect this repo to a new Render Static Site with no build command and the publish directory set to the repo root. Once it deploys, add a custom domain such as register.kizingiti.com in Render and point a CNAME record at Render's target from wherever kizingiti.com's DNS is managed. Once that resolves, swap the WhatsApp and poster link and QR code over to the new domain.
