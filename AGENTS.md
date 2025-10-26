# Repository Guidelines

## Project Structure & Module Organization
This repository is an example Ruby MD SSG site. Human-authored content lives in `docs/`, shared assets in `assets/`, and layout overrides in `templates/`. Generated output is written to `build/` (ignored by git). The site depends on the sibling `ruby_static` gem via the `Gemfile`; run commands from this directory so bundler can find that local dependency.

## Build, Test, and Development Commands
Run `bundle install` after changing the Gemfile or pulling updates to the `ruby-md-ssg` gem. Use `./bin/build` (or `bundle exec ruby_md_ssg build`) to regenerate the site—this also emits `build/sitemap.xml`. `./bin/serve` hosts the site locally with automatic rebuilds, and `./bin/generate_menu` refreshes `docs/menu.yml` manually if needed. The lightweight `./bin/test` command simply runs a build to ensure the project still compiles; CI does the same in `.github/workflows/test.yml`. GitHub Pages deployment lives in `.github/workflows/deploy.yml` and publishes the `build/` directory on pushes to `main`.

Set `RUBY_MD_SSG_BASE_URL` (or pass `--base-url`) to control the absolute URLs that appear in `sitemap.xml`.

## Content & Styling Guidelines
Each markdown file should start with YAML front matter (`title`, optional `description`) so the template can render metadata correctly. Keep navigation-friendly filenames (mirroring folder structure) and store additional styles/scripts under `assets/`—the gem will copy them into `build/assets/` during compilation.

## Working With The Gem
The sibling `ruby_static` project contains the CLI and scaffold template. When updating the gem, run its test suite (`bundle exec ruby bin/test` inside that project) before bumping the path dependency here. After changes, rerun `./bin/build` in this example repo to confirm everything still works.

## Context Logging
Use `CONTEXT_LOG.md` to summarize noteworthy actions so the example remains understandable when history is trimmed.
