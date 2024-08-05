# frozen_string_literal: true
source "https://rubygems.org"
gemspec

if Gem.ruby_version < Gem::Version.new("1.9.3")
  gem "rake", "< 11"
else
  gem "rake"
end

group :development, :test do
  gem "rspec"

  gem "sinatra", '~> 2.0'
  gem "rack", '< 3'

  if Gem.ruby_version < Gem::Version.new("2.0.0")
    gem "json", "< 2"
  else
    gem "json"
  end

  if Gem.ruby_version >= Gem::Version.new("2.0.0")
    gem "mime-types", "~> 1.18"
  end

  if Gem.ruby_version >= Gem::Version.new("2.2.0")
    gem "mustermann"
  elsif Gem.ruby_version >= Gem::Version.new("2.1.0")
    gem "mustermann", "0.4.0"
  elsif Gem.ruby_version >= Gem::Version.new("2.0.0")
    gem "mustermann", "0.3.1"
  end

  if Gem.ruby_version >= Gem::Version.new("3.0.0")
    gem "base64"
    gem "webrick"
  end
end

group :perf do
  gem "benchmark-ips"
  gem "patron"
  gem "curb"
end
