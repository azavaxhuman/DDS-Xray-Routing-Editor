# DDS-Xray-Routing-Editor

# DDS Routing Rules Editor

![Version](https://img.shields.io/badge/version-1.0-blue.svg)

A sleek, web-based tool to **create, sort, and export Xray routing rules** in JSON—right from your browser. Built with **Vue 3** and **Tailwind CSS** (via CDN), there’s no build step or backend. Just open the page and get to work. The UI is tuned for both English and Persian (RTL) content and includes a sponsor area and donation section out of the box. :contentReference[oaicite:0]{index=0}

> This README was rewritten using your previous README as a template while aligning terminology and features with the current `index.html`. The earlier README described an “Inbound Generator”; this project is specifically a **Routing Rules Editor**. :contentReference[oaicite:1]{index=1}:contentReference[oaicite:2]{index=2}

---

## Features

- **Rule management UI**: Add, edit, duplicate, delete, and drag-drop re-order rules in a data-grid with grouped headers. :contentReference[oaicite:3]{index=3}
- **Import & Export**:
  - Export current rules as a JSON file (`⬇️ Export JSON`).
  - Import from a JSON file (`⬆️ Import JSON (File)`) or directly from your clipboard (`📋 Import from Clipboard`).
  - Copy current output to clipboard (`✅ Copy Output`). :contentReference[oaicite:4]{index=4}
- **Helpful presets**: Load an example ruleset with one click (`🧪 Example`) or clear everything (`🗑️ Clear All`). :contentReference[oaicite:5]{index=5}
- **Live output**: The right panel shows **Final Output (`routing.rules`)**—always in sync with your edits. You can select and copy it directly. :contentReference[oaicite:6]{index=6}
- **Sponsor box (RTL-friendly)**: A sidebar “Sponsored Content” card where you can place Persian content, links, and even an image. :contentReference[oaicite:7]{index=7}
- **Donation widget**: Copy-friendly wallet inputs with a one-click copy button. :contentReference[oaicite:8]{index=8}

---

## Quick Start

1. **Download** this repository (or clone it).
2. **Open** `index.html` in a modern browser — that’s it. No server is required because the app is fully client-side. :contentReference[oaicite:9]{index=9}

> The app loads Vue and Tailwind from CDNs referenced in `index.html`. :contentReference[oaicite:10]{index=10}

---

## Using the Editor

### Toolbar

- **➕ Add Rule** – Opens the modal to define a new rule.
- **⬇️ Export JSON** – Downloads the rules as a JSON file.
- **⬆️ Import JSON (File)** – Import rules from a local JSON file.
- **📋 Import from Clipboard** – Paste JSON from your clipboard.
- **✅ Copy Output** – Copies the formatted output.
- **🧪 Example** – Loads sample rules.
- **🗑️ Clear All** – Removes all rules. :contentReference[oaicite:11]{index=11}

### Table & Reordering

- Drag the **⋮⋮** handle to rearrange rules.
- The table groups fields by **Source**, **Network**, **Destination**, **Inbound**, and shows **Outbound**/**Balancer** plus **Actions** (Edit / Duplicate / Delete). :contentReference[oaicite:12]{index=12}

### Modal Form (Rule Fields)

The “Add/Edit Rule” dialog contains all supported fields:

- **domainMatcher**: `"" | "hybrid" | "linear"`
- **source** (IPs), **sourcePort**
- **network** (L4), **protocol**
- **attrs** (custom attributes—add/remove rows)
- **ip** (destination IPs), **domain** (destinations), **port**
- **inboundTag**, **user** (client email)
- **outboundTag** _(required)_, **balancerTag**  
  These correspond to the grid columns and are reflected in the final output. :contentReference[oaicite:13]{index=13}

### Output Panel

- The **Final Output (routing.rules)** area mirrors your rules.
- Click **Copy Output** to copy the text or **Export JSON** to download. :contentReference[oaicite:14]{index=14}

---

## JSON Import/Export Format

You can import **either** of the following:

- An **array** of rules: `[{ ... }, { ... }]`
- An **object** containing `routing.rules`: `{ routing: { rules: [...] } }` :contentReference[oaicite:15]{index=15}

> Tip: Use commas to separate multiple values in list-type inputs (e.g., `tcp,udp` or multiple IPs/domains). :contentReference[oaicite:16]{index=16}

---

## Donations

A “Support Us with a Donation” panel includes wallet inputs and a **copy** button for each wallet. You can customize wallet names and addresses in the app’s data section. :contentReference[oaicite:19]{index=19}

If you prefer a table in the README, you can add one like your previous project style. :contentReference[oaicite:20]{index=20}

---

## Tech Stack

- **Vue 3** (via CDN) for reactive UI.
- **Tailwind CSS** (via CDN) for styling.
- Vanilla HTML/CSS/JS—no build tooling required. :contentReference[oaicite:21]{index=21}

---

## Contributing

Issues and PRs are welcome—especially for UX polish, keyboard accessibility, shortcuts, and schema validations.

---

## License

GPL-3.0

---

## Credits

Developed by **Daily Digital Skills**. Sidebar links to the Telegram channel and YouTube are included in the header. :contentReference[oaicite:22]{index=22}
