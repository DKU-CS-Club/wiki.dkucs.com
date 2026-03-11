# DKU Wiki Development Guide

The DKU Wiki uses Quarto, a _Pandoc Markdown_-based scientific publishing tool, repurposing it for easy Markdown-based website building. Users of RStudio may find it familiar.

[Quarto Guide & Documentation](https://quarto.org/)

## Install Dependencies

You can [install Quarto](https://quarto.org/docs/get-started/) through a variety of package managers.

### For macOS:

```zsh
brew install quarto
```

### For Windows:

```powershell
winget install -e --id Posit.Quarto
```

## Get Started

1. Clone this repo.
2. Open the project in your IDE or terminal of choice.
3. Run `quarto preview`, and your default browser should open a preview on port 4201.

The site should hot reload upon saving .qmd files.

## Directory Structure

**Root `./`** contains project configuration files and documentation.

`./articles/` contains every Quarto Markdown (.qmd) file except `index.qmd`, which serves as the entry point for the website (as configured inside `./_quarto.yml`).

`./assets/` contains every image and video included in articles.

## Contributing

All contributions must be made through a GitHub **pull request** (PR). We recommend PRs focus on one issue or one article only. All activity must follow our community [CODE_OF_CONDUCT](./CODE_OF_CONDUCT.md)

Bug reports and issue submissions are welcome!

## Deploying 

> This section is only relevant to maintainers. 

This website uses Vercel to host all rendered files. 

Anar already set this up so that any commit to main that changes the `./render/` directory will auto-update the Vercel deployment, so all you need to do is run `quarto render`, and rename (`mv`) the `_site` directory to `render`.
