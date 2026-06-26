# HydeJekyll LLC — site

## Files
- `index.html` — main landing page
- `laboratory.html` — coming-soon page for unreleased ventures
- `style.css` — shared styles
- `assets/` — drop your hero photo here (see below)

## Adding the real hero photo
Right now the hero uses a CSS gradient as a stand-in for the photo (dusk sky,
warm horizon glow, dark barn-door framing on either side). To swap in a real
photo:

1. Save your photo as `assets/hero-stable-dusk.jpg`
2. Open `style.css`, find the `.hero-sky` rule, and uncomment this line:
   `/* background-image: url("assets/hero-stable-dusk.jpg"); */`

Look for something shot low and centered, like you're standing just inside
a stable doorway with the doors swung open, looking out at open country at
dusk — warm sky, dark silhouette framing top/sides. Unsplash and Pexels (free,
no attribution required) are good places to search "barn door sunset" or
"stable doorway countryside."

## Editing company blurbs
SoFlo Supply Co. and ReviewJester.ai currently have placeholder one-liners
in `index.html` (marked `<!-- EDIT ME -->`). Swap those out for real copy
whenever you're ready — everything else on the page will keep working as-is.

## Deploying

### 1. Push to GitHub
```
cd hydejekyll-llc
git init
git add .
git commit -m "Initial HydeJekyll LLC site"
git branch -M main
git remote add origin https://github.com/<your-username>/hydejekyll-llc.git
git push -u origin main
```

### 2. Connect Netlify
1. Log in to Netlify → **Add new site** → **Import an existing project**
2. Choose **GitHub**, authorize if needed, select the `hydejekyll-llc` repo
3. Build settings: leave **Build command** blank, set **Publish directory** to `/` (root)
4. Click **Deploy site** — Netlify gives you a temporary `*.netlify.app` URL

### 3. Point your domain at it
1. In the Netlify site dashboard: **Domain settings** → **Add a domain** → enter your domain
2. Netlify will show you DNS records to add (usually a `CNAME` for `www` and an `A` record, or you can delegate to Netlify DNS for it to handle automatically)
3. Add those records wherever your domain is registered — propagation usually takes anywhere from a few minutes to a few hours

From then on, every `git push` to `main` auto-deploys.
