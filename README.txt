BROMPTON SITE — README
=======================

WHAT'S IN HERE
--------------
- index.html                          → landing page linking the 3 pages below
- brompton-storyboard.html            → in-store storyboard
- brompton-ownership-storyboard.html  → Andy's ownership journey
- brompton-tline-product-page.html    → T Line product page
- Brand/                              → put your font (and any logo) files here

These three pages already link to each other by filename (storyboard → ownership
journey → product page), so don't rename them or those links will break.


STEP 1 — ADD YOUR FONT FILES
-----------------------------
Two of the pages expect:
  Brand/BromptonSlab-Regular.woff
  Brand/BromptonSlab-Regular.otf

Drop your actual font files into the Brand/ folder using those exact names
(or update the @font-face src paths near the top of each HTML file's <style>
block if your filenames differ). If you also want a local copy of the
Brompton logo instead of relying on the hotlinked one from brompton.com,
add it to Brand/ too and update the relevant <img src="..."> tag in
brompton-tline-product-page.html.

Everything else (product photos, headshots, the brompton.com logo, etc.) is
loaded from external URLs already, so no action needed there — just know
that if any of those source sites ever take an image down, it'll break on
your site too.


STEP 2 — DEPLOY TO NETLIFY (free, no account needed to start)
----------------------------------------------------------------
1. Go to https://app.netlify.com/drop
2. Drag this whole "brompton-site" folder onto the page
3. Netlify gives you a live public URL in a few seconds (something like
   random-name-123.netlify.app)

That link works immediately, but is temporary (~24 hrs) unless you claim it
with a free account:

4. Sign up free at https://app.netlify.com (email or GitHub login)
5. Claim the site you just dropped — it gets a permanent URL
6. Optional: in Site settings → Domain management, you can rename the
   subdomain (e.g. brompton-project.netlify.app) at no cost. A fully custom
   domain (yourname.com) requires owning that domain separately.


STEP 3 — UPDATING THE SITE LATER
----------------------------------
After editing the HTML in Claude Desktop:
1. Log into https://app.netlify.com
2. Open your site → "Deploys" tab
3. Drag the updated brompton-site folder onto the deploy area
4. Netlify swaps in the new files instantly — same URL, no downtime,
   no editing happens on Netlify's end at all.

That's the entire update workflow going forward: edit locally, drag, done.


ALTERNATIVE: GITHUB PAGES
--------------------------
If you'd rather not use Netlify: create a free GitHub repo, upload this
folder's contents via the GitHub web UI (Add file → Upload files — no git
command line needed), enable Pages in repo Settings → Pages → Deploy from
branch → main → /(root). You get a URL like
yourusername.github.io/repo-name. Updating later means re-uploading changed
files through that same web UI screen.
