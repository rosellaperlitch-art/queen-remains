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

1. Push this folder to a GitHub repo (or use Netlify’s drag‑and‑drop).
2. In Netlify: **Add new site** → **Import from Git** (or drag the folder).
3. Build settings: leave **Build command** empty, set **Publish directory** to `.` (root).
4. Deploy. Your site will be at `something.netlify.app`. You can add a custom domain later.

No backend or build step is required; the site is plain HTML, CSS, and assets.
