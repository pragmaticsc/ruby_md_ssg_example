# Recommended Workflow

- Write new content in `docs/` using markdown headings to outline the story.
- Regenerate the menu with `bundle exec ruby exe/ruby_md_ssg menu` so the navigation picks up new pages.
- Rebuild the site with `bundle exec ruby exe/ruby_md_ssg build` and review the output before opening a pull request.

Keep each page focused on a single topic and prefer relative links when referencing peer documents.
