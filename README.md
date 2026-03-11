# DKU Wiki Development Guide

The DKU Wiki uses Quarto, a _Pandoc Markdown_-based scientific publishing tool, repurposing it for easy Markdown-based website building. Users of RStudio may find it familiar.

[Quarto Guide & Documentation](https://quarto.org/)

## Install dependencies

You can [install Quarto](https://quarto.org/docs/get-started/) through a variety of package managers.

### For macOS:

```zsh
brew install quarto
```

### For Windows:

```powershell
winget install -e --id Posit.Quarto
```

## Get started

1. Clone this repo.
2. Open the project in your IDE or terminal of choice.
3. Run `quarto preview`, and your default browser should open a preview on port 4201.

The site should hot reload upon saving .qmd files.

## Directory Structure

**Root `./`** contains project configuration files and documentation.

`./articles/` contains every Quarto Markdown (.qmd) file, including `index.qmd`, which serves as the entry point for the website (as configured inside `./_quarto.yml`).

`./assets/` contains every image and video included in articles.

## Contributing

All contributions must be made through a GitHub **pull request** (PR). We recommend PRs focus on one issue or one article only.

Bug reports and issue submissions are welcome!
