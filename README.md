# Apps Repository

Collection of simple standalone web applications hosted on GitHub Pages.

The goal of this repo is to develop simple deployable apps to solve specific use cases as a practice to focus on solving problems quickly with AI coding assistants like Augment.


## Available Apps

- [Top Text LLMs - Arena Score vs Voting Score - Discover non-proprietary models in Ollama](https://kimnewzealand.github.io/apps/models-app.html) 

This app visualises the model capabilities (the Arena score) and public opinion (number of votes) differences between proprietary and open source text models and whether they are available for download from Ollama, which is not visually available in the [LLMArena leaderboard](https://lmarena.ai/leaderboard). 

What is Arena Score:
- Battle-Based Evaluation
- Head-to-head battles: Two models compete by generating responses to the same prompt
- Human judges: Real users vote on which response is better
- Elo-style rating: Similar to chess ratings, models gain/lose points based on wins/losses
- Composite metric: Reflects overall model performance across diverse tasks


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