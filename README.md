# Influence Genogram

A single-page web tool for building **influence genograms** — visual maps of the people, institutions, and cultural forces that shaped your sexuality and worldview across your life, and how those influences changed over time.

**Live site:** https://dylwar27.github.io/genogram/

Built for a school assignment; free for anyone to use.

---

## Quick start

1. Open the live site in any modern browser (Chrome, Firefox, Safari, Edge).
2. Use the left sidebar to **Add Influence** — give it a name, a type (family / friend / partner / institution / media / self-realization), a life period (childhood / teens / college / adulthood), and a short note about how it influenced you.
3. Scroll down to **Add Connection** — pick two influences, a nature (supportive, restrictive, mixed, challenging, transformative), and optionally a short label (e.g. "taught openness").
4. Click any node or connection in the diagram to edit it. Click empty canvas to deselect.
5. Use the toolbar to save, export, or generate the graph from a narrative.

---

## AI features (optional)

Two buttons call Claude via your own Anthropic API key:

- **✨ Generate from Text** — paste a narrative or transcript; Claude extracts the influences and relationships and builds the graph for you.
- **📝 Written Statement** — Claude reads your current graph and writes a 3–5 paragraph reflective essay explaining the structure and patterns.

### Getting an API key

1. Go to [console.anthropic.com/settings/keys](https://console.anthropic.com/settings/keys).
2. Sign up (requires a small balance; a few cents covers dozens of generations).
3. Create a key starting with `sk-ant-...`.
4. Paste it into the **Generate from Text** dialog once — it's stored only in your browser's `localStorage` and sent only directly to Anthropic.

---

## Profiles & passwords

Click **👤 Profiles** to create a password-protected profile. This is useful when:

- Multiple classmates share a computer.
- You want to save your work and come back to it on the same browser later.

Profiles are stored **locally in your browser only**, encrypted with AES-GCM using a key derived from your password (PBKDF2, 200k iterations, SHA-256). No one — not me, not GitHub, not Anthropic — has access to your data or your password.

**Warning:** if you forget the password, the profile cannot be recovered. For important work, also use **Export JSON** for an unencrypted backup (or keep it in a password manager).

Profiles do not sync between devices or browsers. If you want to move a profile, use **Export JSON** on one device and **Import JSON** on the other.

---

## Accessibility

- Full keyboard support: Tab through all controls, Enter/Space to activate, Escape to deselect or close modals, Delete to remove a selected node/connection.
- Semantic landmarks, ARIA labels, and a hidden screen-reader-friendly table view of all nodes and connections.
- **Palette** toolbar button toggles an Okabe-Ito color-blind-safe palette.
- **A** / **A+** / **A++** toolbar button cycles text size.
- Connection lines are distinguished by **line style + arrow shape**, not just color.

---

## Exports

- **Save PNG** — 3× resolution, includes a small footer with the profile name and date.
- **Save SVG** — vector export; scales perfectly for handouts or slides.
- **Print** — landscape, no chrome, fits to page.
- **Export JSON / Import JSON** — raw unencrypted data for backups or sharing snapshots.
- **Present** — fullscreen mode with mouse drag to pan and scroll wheel to zoom.

---

## Privacy

This site is a **static HTML page**. No data leaves your browser except:

- Direct calls to Anthropic's API (only when you click ✨ or 📝), authenticated with your own key, containing only the narrative or graph you explicitly pass in.
- GitHub Pages serves the HTML file over HTTPS; no analytics, no tracking.

Your profiles, API key, and preferences live in your browser's `localStorage` and never leave your device.

---

## Source code

[github.com/dylwar27/genogram](https://github.com/dylwar27/genogram)

MIT-licensed; single `index.html` with embedded CSS and JavaScript. No build step, no dependencies.

---

*This is a student tool for a school assignment. It is not a clinical or therapeutic instrument. For concerns about your mental health, please reach out to a qualified professional.*
