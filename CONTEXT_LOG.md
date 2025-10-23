## 2024-10-08
- Split the original static-ruby repository into two projects: this example site (`ruby_static_example`) and the reusable gem in `../ruby_static`.
- Updated Gemfile to depend on the sibling gem, refreshed bin scripts and GitHub workflows to call `static_ruby` via bundler, and added a simple Rakefile/build script for the example site.
