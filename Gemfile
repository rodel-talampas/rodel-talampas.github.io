source "https://rubygems.org"

ruby file: ".ruby-version"

gem "jekyll", "4.4.1"
gem "minima", "~> 2.5"

group :jekyll_plugins do
  gem "jekyll-feed", "~> 0.17"
end

platforms :windows, :jruby do
  gem "tzinfo", "~> 2.0"
  gem "tzinfo-data"
end

gem "wdm", "~> 0.1.1", platforms: [:windows]
