# Gatsby + Forestry CMS Trial

A trial project exploring [Gatsby v2](https://www.gatsbyjs.com/) as a static site generator with [Forestry.io](https://forestry.io/) as a headless CMS admin interface.

## What It Does

This is a Gatsby starter site wired up with Forestry CMS for git-based content management. It includes:

- Static site generation with Gatsby v2
- Forestry CMS admin panel at `/admin`
- Image optimization via `gatsby-image` + `gatsby-plugin-sharp`
- SEO component with Open Graph and Twitter Card meta tags
- TypeScript page example
- PWA manifest support
- Prettier code formatting

## Project Structure

```
├── .forestry/          # Forestry CMS configuration
├── src/
│   ├── components/     # Layout, Header, SEO, Image components
│   ├── images/         # Static image assets
│   └── pages/          # Site pages (index, 404, page-2, TypeScript demo)
├── static/admin/       # Forestry admin panel entry point
├── gatsby-config.js    # Gatsby plugins and site metadata
├── gatsby-node.js      # Gatsby Node APIs (unused)
├── gatsby-browser.js   # Gatsby Browser APIs (unused)
└── gatsby-ssr.js       # Gatsby SSR APIs (unused)
```

## 🛠 Tech Stack

| Tool | Purpose |
|------|---------|
| ⚛️ React 16 | UI framework |
| 🟣 Gatsby v2 | Static site generator |
| 🌲 Forestry CMS | Git-based content management |
| 🖼 gatsby-image | Optimized image loading |
| 🔍 react-helmet | Document head management / SEO |
| 🎨 Prettier | Code formatting |

## Getting Started

```bash
# Install dependencies
npm install

# Start development server
npm run develop
# → http://localhost:8000
# → http://localhost:8000/___graphql (GraphQL explorer)

# Build for production
npm run build

# Serve production build locally
npm run serve
```

## ⚠️ Known Issues

- **Forestry.io has been sunset.** Forestry was discontinued and replaced by [TinaCMS](https://tina.io/). The admin panel at `/admin` loads scripts from `app.forestry.io` which is no longer available. To restore CMS functionality, migrate to TinaCMS or another headless CMS.
- **Gatsby v2 is end-of-life.** The project depends on Gatsby v2.25.3. Gatsby v5 is the current major version with significant performance and API improvements. An upgrade would require migrating from `gatsby-image` to `gatsby-plugin-image` and updating Node.js requirements.
- **Forestry Docker image uses Node 12 (EOL).** The `.forestry/settings.yml` references `forestryio/node:12` which is no longer supported.

## License

0BSD — see [LICENSE](LICENSE).
