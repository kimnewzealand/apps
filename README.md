# Apps Repository

Collection of simple standalone web applications hosted on GitHub Pages.

The goal of this repo is to develop simple deployable apps to solve specific use cases as a practice to focus on solving problems quickly.

## Available Apps

- [LLMArena Text Area Scores](https://kimnewzealand.github.io/apps/models-app.html) - Interactive visualization of large language model scores with bar charts to visualise the difference between proprietary and open source models, which is not visually available in the [LLMArena leaderboard](https://lmarena.ai/leaderboard).

## About

This repository hosts multiple standalone web applications, each designed to run independently without shared dependencies. Each app is a single HTML file that includes all necessary CSS and JavaScript inline or loads dependencies from CDNs.

## App Architecture

Each application follows these principles:
- **Self-contained**: All CSS and JavaScript inline or from CDN
- **Single HTML file**: No external dependencies within the repo
- **Responsive**: Works on mobile and desktop
- **Complete**: Standalone functionality with no navigation dependencies

## Adding New Apps

1. Create a new HTML file following the naming pattern: `[app-name]-app.html`
2. Make it completely self-contained (all CSS/JS inline or from CDN)
3. Include proper meta tags for title, description, and viewport
4. Test locally using a simple HTTP server: `python -m http.server 8000`
5. Commit and push - GitHub Actions will deploy automatically

## Local Development

To test apps locally:

```bash
# Start a local HTTP server
python -m http.server 8000

# Open in browser
http://localhost:8000/models-app.html
```

## Deployment

This repository uses GitHub Actions for automatic deployment to GitHub Pages. Any HTML file pushed to the main branch will be automatically available at:

`https://kimnewzealand.github.io/apps/[filename].html`