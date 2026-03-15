# The Queen Remains – Band website

Static site for the band. Run it locally or deploy to Netlify.

## Run locally

**With Node (recommended)**  
Install dependencies once, then use the scripts:

```bash
npm install
npm run dev      # Development: live-server with auto-reload on port 8080
npm run start    # Production-style: simple static server on port 3000
```

- **`npm run dev`** – Uses [live-server](https://www.npmjs.com/package/live-server): opens the site in your browser and reloads when you edit files.
- **`npm run start`** – Uses [serve](https://www.npmjs.com/package/serve): runs a minimal static server (no live reload), similar to how it will run on Netlify.

**Without Node**  
- Double‑click `index.html` to open in your browser, or  
- **Python 3:** `python3 -m http.server 8000` then open http://localhost:8000

## What to edit

- **Band bios & photos:** `band.html` – replace placeholder text and swap the placeholder divs for `<img src="assets/your-photo.jpg" alt="Name">`.
- **Gallery:** `gallery.html` – replace the placeholder divs with `<img>` tags pointing to files in `assets/` (e.g. `assets/gallery1.jpg`).
- **Gigs:** `gigs.html` – follow the comment at the top of the gigs list: copy a gig block, fill in date/venue/city, add a ticket link if you have one.
- **Videos:** `videos.html` – when you have a YouTube channel, use Share → Embed on each video and paste the iframe code where the placeholders are.
- **Merch:** `merch.html` – when Printful is set up, replace the placeholder with the store embed or a link to the store.
- **Contact:** `contact.html` – create a Google Form (Name + Message), get the embed code (Send → `</>`), and paste the iframe where the instructions say.

## Deploy to Netlify

This site is static (HTML, CSS, images). No build step is required. Netlify will serve the files as-is using the settings in `netlify.toml`.

### Option A: Deploy with Git (recommended)

1. **Push your code to GitHub**  
   Create a new repo on GitHub, then in this folder run:
   ```bash
   git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO.git
   git push -u origin main
   ```

2. **Connect to Netlify**  
   - Go to [netlify.com](https://www.netlify.com) and sign in (or sign up with GitHub).  
   - Click **Add new site** → **Import an existing project**.  
   - Choose **GitHub** and authorize Netlify.  
   - Select the repo you pushed.  

3. **Configure the build**  
   Netlify should pick up `netlify.toml` automatically. If not, set:
   - **Build command:** leave empty, or `echo 'Static site – no build'`  
   - **Publish directory:** `.` (the root)  

4. **Deploy**  
   Click **Deploy site**. Netlify will build and give you a URL like `random-name-123.netlify.app`.  
   Every push to `main` will trigger a new deploy.

### Option B: Drag-and-drop deploy

1. Go to [app.netlify.com](https://app.netlify.com) and sign in.  
2. Drag this project **folder** (the one containing `index.html`, `band.html`, `assets/`, etc.) onto the “Deploy manually” drop zone.  
3. Netlify will upload and publish. You’ll get a live URL right away.  
   - **Note:** Drag-and-drop doesn’t connect to Git, so you’ll need to drag the folder again whenever you want to update the site.

### After deploy

- **Custom domain:** In the Netlify dashboard, go to **Domain settings** → **Add custom domain** and follow the steps.  
- **HTTPS:** Netlify provides a free SSL certificate; it’s enabled by default on `*.netlify.app` and for custom domains.
