source "https://rubygems.org"

# Modern Jekyll — works with current Ruby versions.
gem "jekyll", "~> 4.3"

# Plugins used by the site.
group :jekyll_plugins do
  gem "jekyll-feed"
  gem "jekyll-paginate"
  gem "jekyll-seo-tag"
end

# Needed to run `jekyll serve` on Ruby 3.0+ (no longer bundled by default).
gem "webrick"

# Standard-library gems that newer Ruby versions no longer bundle by default.
gem "csv"
gem "base64"
gem "bigdecimal"
gem "logger"

# Windows / JRuby timezone support (harmless on Linux/macOS).
platforms :windows, :jruby do
  gem "tzinfo", ">= 1", "< 3"
  gem "tzinfo-data"
end
