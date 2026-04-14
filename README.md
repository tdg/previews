# previews

Shareable JSX component previews, served via GitHub Pages.

Each `.html` file is a self-contained page that runs React 18 + Tailwind CSS entirely in the browser — no build step required.

**Live URL pattern:** `https://tdg.github.io/previews/<filename>.html`

---

## How to add a new preview

1. **Copy `template.html`** and give it a descriptive name, e.g. `my-component.html`.

2. **Paste your JSX** into the clearly marked section:

   ```html
   <!-- ============================================================
        PASTE YOUR JSX COMPONENT BELOW
        ...
        ============================================================ -->
   <script type="text/babel">

     function App() {
       // your component here
     }
   ```

3. **Update the `<title>`** tag at the top to match your component name.

4. **Commit and push** to `main`:

   ```bash
   git add my-component.html
   git commit -m "Add my-component preview"
   git push
   ```

5. GitHub Pages will deploy within ~30 seconds. Your preview is live at:
   `https://tdg.github.io/previews/my-component.html`

---

## What's included in each page

| Library | Version | Purpose |
|---|---|---|
| React | 18 | Component rendering |
| ReactDOM | 18 | DOM mounting |
| Babel Standalone | latest | In-browser JSX transpilation |
| Tailwind CSS | latest | Utility-first styling |

All loaded from CDN — no `npm install`, no bundler.

---

## Files

| File | Description |
|---|---|
| `template.html` | Blank starter — copy this for new previews |
| `example.html` | Hello World counter component |
