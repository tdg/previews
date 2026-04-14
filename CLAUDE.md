# previews — Claude workflow

This repo hosts JSX component previews at **https://tdg.github.io/previews/**.

## Publishing a preview

1. Write the JSX component to a `.jsx` file (e.g. `/tmp/my-component.jsx`).
   - The top-level component **must be named `App`**.
   - No ES module `import` statements — React, ReactDOM, and Tailwind are pre-loaded.
   - React hooks are available via destructuring: `const { useState, useEffect } = React;`
     (the template does this automatically, so you can use hooks directly in the file).

2. Run:
   ```
   ~/bin/push-preview /tmp/my-component.jsx [optional-slug]
   ```

3. The script will:
   - Inject the JSX into the HTML template
   - Commit and push to `main`
   - Print the live URL

GitHub Pages deploys in ~30 seconds. The live URL pattern is:
`https://tdg.github.io/previews/<slug>.html`

## File layout

| File | Purpose |
|---|---|
| `template.html` | Blank starter template |
| `example.html` | Hello World counter demo |
| `CLAUDE.md` | This file |
| `README.md` | Human-readable docs |
