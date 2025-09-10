# Apps Repository

This repo contains simple, deployable apps that solve specific problems quickly using AI coding assistants, like Augment.


## App Architecture

Each application follows these principles:
- **Self-contained**: All CSS and JavaScript inline or from CDN
- **Single HTML file**: No external dependencies within the repo
- **Responsive**: Works on mobile and desktop
- **Complete**: Standalone functionality with no navigation dependencies


## Available Apps

- [Top Text LLMs - Arena Score vs Voting Score - Discover non-proprietary models in Ollama](https://kimnewzealand.github.io/apps/models-app.html) 

I wanted to find a quick way to chose the best free to use Ollama model to download and experiment with. This app visualises the model capabilities (the Arena score) and public opinion (number of votes) based on the [LLMArena leaderboard](https://lmarena.ai/leaderboard), breaks down proprietary and open source text models and whether they are available for download from Ollama, and which ones are 7B or smaller given my 8GB installed RAM.

As per [Ollama's docs:](https://github.com/ollama/ollama?tab=readme-ov-file)
> You should have at least 8 GB of RAM available to run the 7B models, 16 GB to run the 13B models, and 32 GB to run the 33B models.


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