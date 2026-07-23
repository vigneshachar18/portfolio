# Your Name — Portfolio

A playful, animated, single-page portfolio built with plain HTML, CSS, and
JavaScript. No build tools, no frameworks, no npm install — just upload and go.

## What's inside

```
portfolio/
├── index.html          ← all the content lives here
├── css/
│   └── style.css       ← colors, fonts, layout, animations
├── js/
│   └── script.js       ← typewriter, scroll reveals, confetti, form, etc.
├── assets/
│   └── profile-placeholder.svg   ← swap this for your real photo
└── README.md
```

## 1. Personalize it before you publish

Search the files for `<!-- EDIT ME -->` comments and the following
placeholders, and replace them with your real info:

- **Name & title** — top of `index.html` (`<title>`, hero heading, footer)
- **Bio** — the About section
- **Photo** — replace `assets/profile-placeholder.svg` with a real image
  (e.g. `assets/profile.jpg`) and update the `src` in the About section
- **Skills** — the pill tags in the Skills section
- **Projects** — titles, descriptions, tech tags, and the `href="#"` links
  (point them at your real GitHub repos / live demos)
- **Timeline** — your education and milestones
- **Contact links** — email, GitHub, LinkedIn, Twitter/X in the Contact
  section
- **Resume** — the "grab my resume" button links to `/resume.pdf`; drop your
  actual resume PDF into the project root with that filename (or update the
  link)
- **Contact form** — right now the form only shows a "sent! 🎉" animation
  locally; it doesn't actually send anywhere yet. Easiest fix: sign up at
  [Formspree](https://formspree.io) (free tier works fine), grab your form
  endpoint, and in `index.html` change:
  ```html
  <form class="contact-form" id="contactForm">
  ```
  to:
  ```html
  <form class="contact-form" id="contactForm" action="https://formspree.io/f/yourFormId" method="POST">
  ```
  and remove the `e.preventDefault()` line in `script.js` (or follow
  Formspree's fetch-based example if you want to keep the confetti + inline
  "sent" message).

## 2. Preview it locally

Just double-click `index.html` — it'll open in your browser. That's it,
no server required (Google Fonts still needs an internet connection to load).

## 3. Push it to GitHub

```bash
cd portfolio
git init
git add .
git commit -m "Initial portfolio"
git branch -M main
git remote add origin https://github.com/<your-username>/<repo-name>.git
git push -u origin main
```

If you'd rather not use the command line, you can also just drag-and-drop
the whole `portfolio` folder's contents into a new repo on github.com
("Add file → Upload files").

## 4. Host it for free — GitHub Pages (recommended, easiest)

1. Push the project to a GitHub repo (see above). For a personal site at
   `https://<username>.github.io`, name the repo exactly
   `<your-username>.github.io`. Any other name works too, it'll just live at
   `https://<username>.github.io/<repo-name>/`.
2. On GitHub, open the repo → **Settings** → **Pages** (left sidebar).
3. Under "Build and deployment", set **Source** to **Deploy from a branch**.
4. Set **Branch** to `main` and folder to `/ (root)`, then **Save**.
5. Wait 1–2 minutes, then refresh — GitHub shows you the live URL at the
   top of that same Pages settings page.

Every time you `git push` after that, your live site updates automatically.

## 5. Other free hosting options

- **Netlify** — go to [app.netlify.com](https://app.netlify.com), drag the
  `portfolio` folder straight onto the dashboard, done. Or connect your
  GitHub repo for auto-deploys on every push.
- **Vercel** — [vercel.com/new](https://vercel.com/new), import the GitHub
  repo, leave all settings default (no framework/build step needed), deploy.
- **Cloudflare Pages** — similar flow: connect the repo, no build command,
  output directory `/`.

All of these are free for a personal portfolio and give you HTTPS
automatically. GitHub Pages is the simplest if you just want one URL tied
directly to your GitHub profile.

## 6. Custom domain (optional)

Bought a domain (Namecheap, Google Domains, etc.)? Every host above has a
"Custom domain" setting where you add your domain and point its DNS
(usually a CNAME record) at the host — each platform's docs walk through
the exact records to add.

---

Built with HTML, CSS, and vanilla JavaScript — no dependencies, no build
step, no framework lock-in. Fully responsive and respects
`prefers-reduced-motion` for accessibility.
