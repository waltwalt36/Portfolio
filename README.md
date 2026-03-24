# Walter Briones — Portfolio

Personal portfolio site built with Node.js + Express + EJS.

## Local Development

```bash
npm install
npm run dev        # uses nodemon for hot reload
# or
npm start          # production
```

Open http://localhost:3000

---

## Adding Your Photo

1. Add your photo file to `public/images/` (e.g. `photo.jpg`)
2. Open `views/index.ejs`
3. Find this comment block in the hero section:
   ```html
   <!-- Replace the div below with: <img src="/images/photo.jpg" alt="Walter Briones" /> -->
   <div class="placeholder-photo">...</div>
   ```
4. Replace the entire `<div class="placeholder-photo">` block with:
   ```html
   <img src="/images/photo.jpg" alt="Walter Briones" />
   ```

---

## Adding Your Resume

Drop your resume PDF as `public/resume.pdf` — the Resume links in the nav and contact section will automatically point to it.

---

## Update Lux & Shine URL

In `views/index.ejs`, find the Lux & Shine project card and replace `href="#"` with the real URL.

---

## Deploy to Railway

Railway hosts Node.js apps with zero config.

1. Push your code to a GitHub repo:
   ```bash
   git init
   git add .
   git commit -m "init portfolio"
   git remote add origin https://github.com/YOUR_USERNAME/portfolio.git
   git push -u origin main
   ```

2. Go to https://railway.app and sign in with GitHub

3. Click **"New Project"** → **"Deploy from GitHub repo"**

4. Select your portfolio repo

5. Railway auto-detects Node.js and runs `npm start` (from your `package.json`)

6. Once deployed, click **"Settings"** → **"Domains"** → **"Generate Domain"** for a free `.railway.app` URL

7. Optional: Add a custom domain under Settings → Domains

That's it — Railway redeploys automatically on every `git push`.

---

## Deploy to Vercel

Vercel also supports Node.js via the included `vercel.json`.

1. Make sure your code is pushed to GitHub (see Railway step 1 above)

2. Go to https://vercel.com and sign in with GitHub

3. Click **"Add New Project"** → import your portfolio repo

4. Vercel will detect the `vercel.json` config automatically

5. Click **"Deploy"**

6. You'll get a free `yourname.vercel.app` URL instantly

7. Optional: Add a custom domain under Project Settings → Domains

Vercel also redeploys on every `git push`.

---

## Recommendation

Use **Vercel** for fastest deploys and the best free custom domain experience.
Use **Railway** if you later add a database or backend services.

---

## Tech Stack

- Node.js + Express
- EJS templating
- Vanilla CSS (custom properties, animations)
- Vanilla JS (IntersectionObserver, custom cursor)
