# EL Education (El Edu)

> A Vue 3 web application for EL Education — balancing knowledge, empowering learners.

This site is for informing purposes. Elsa Lamprecht is an Accounting tutor with experience of more than 40 years. 
She lives in George.

She assists high school learners from various schools in George with Accounting. She is passionate about teaching and accounting.

// Note to self: should check if she has space for more learners

Email: eleducation2021@gmail.com

<p align="center">
  <img src="src/assets/logo.png" alt="EL Education Logo" width="140" />
</p>

---

## Color Palette

| Token | Hex | Usage |
|---|---|---|
| `--color-primary` | `#E8453C` | Brand red — backgrounds, buttons, accents |
| `--color-primary-dark` | `#C0392B` | Hover states, active elements |
| `--color-on-primary` | `#FFFFFF` | Text/icons on red surfaces |
| `--color-surface` | `#1A1A1A` | Dark sections, footer |
| `--color-background` | `#FFFFFF` | Page background |
| `--color-text` | `#1A1A1A` | Body text |

---

## Tech Stack

- **Framework:** [Vue 3](https://vuejs.org/) (Composition API)
- **Build tool:** [Vite](https://vitejs.dev/)
- **Hosting:** [GitHub Pages](https://pages.github.com/) (`/docs` folder)
- **Package manager:** npm

---

## Project Structure

```
eledu-website/
├── docs/               # Built output served by GitHub Pages
├── public/             # Static assets copied as-is
├── src/
│   ├── assets/
│   │   ├── logo.png    # EL Education logo
│   │   └── styles/
│   │       └── main.css
│   ├── components/
│   │   ├── NavBar.vue
│   │   ├── HeroSection.vue
│   │   └── FooterSection.vue
│   ├── views/
│   │   └── HomeView.vue
│   ├── App.vue
│   └── main.js
├── index.html
├── vite.config.js
├── package.json
└── README.md
```

---

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) v18 or later
- npm v9 or later

### Install dependencies

```bash
npm install
```

### Run development server

```bash
npm run dev
```

Open [http://localhost:5173](http://localhost:5173) in your browser.

### Build for production

```bash
npm run build
```

The compiled output is written to the `docs/` folder, ready for GitHub Pages.

### Preview the production build locally

```bash
npm run preview
```

---

## Deploying to GitHub Pages

1. Build the project:
   ```bash
   npm run build
   ```
2. Commit and push the `docs/` folder to your repository:
   ```bash
   git add docs/
   git commit -m "chore: build for GitHub Pages"
   git push
   ```
3. In your GitHub repository go to **Settings → Pages**.
4. Under **Build and deployment → Source**, select **Deploy from a branch**.
5. Choose the branch (e.g. `main`) and set the folder to **`/docs`**.
6. Click **Save**. Your site will be live at `https://<username>.github.io/<repo-name>/`.

> **Note:** If your repository is not at the root (e.g. `https://<username>.github.io/<repo-name>/`), make sure the `base` option in `vite.config.js` matches your repository name:
> ```js
> base: '/<repo-name>/',
> ```

---

## Scripts

| Command | Description |
|---|---|
| `npm run dev` | Start Vite dev server with HMR |
| `npm run build` | Build to `docs/` for GitHub Pages |
| `npm run preview` | Preview production build locally |
| `npm run lint` | Lint source files |

---

## License

© 2026 EL Education. All rights reserved.
