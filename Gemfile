source "https://rubygems.org"

# The site is built and deployed with GitHub Actions (see
# .github/workflows/pages.yml), so we are free to use a current Jekyll rather
# than the version pinned by the `github-pages` gem.
gem "jekyll", "~> 4.4"

group :jekyll_plugins do
  gem "jekyll-sitemap", "~> 1.4"
end

# kramdown 2.x ships GFM parsing as a separate gem.
gem "kramdown-parser-gfm", "~> 1.1"

# Windows and JRuby do not include zoneinfo files, so bundle the tzinfo-data gem
# and associated library.
platforms :mingw, :x64_mingw, :mswin, :jruby do
  gem "tzinfo", ">= 1", "< 3"
  gem "tzinfo-data"
end

# Performance-booster for watching directories on Windows.
gem "wdm", "~> 0.2.0", :platforms => [:mingw, :x64_mingw, :mswin]

# Lock `http_parser.rb` gem to v0.6.x on JRuby builds.
gem "http_parser.rb", "~> 0.6.0", :platforms => [:jruby]
