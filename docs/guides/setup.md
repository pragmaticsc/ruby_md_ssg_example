# Getting Started

1. Install Ruby 3.2 or newer.
2. Run `bundle install` inside the repository.
3. Execute `bundle exec ruby exe/ruby_md_ssg build` to generate the static site (or `bundle exec ruby_md_ssg build` once the gem is installed). This command also writes `build/sitemap.xml`; set `RUBY_MD_SSG_BASE_URL` (or pass `--base-url`) if you need canonical URLs.

You can now open the files in the `build/` directory or run the server command to preview locally.
