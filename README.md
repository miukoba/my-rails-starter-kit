# my rails starter kit

## Setup

- gem update bundler

- mkdir /path/to/project

- cd /path/to/project

- bundle init

- vi Gemfile

```
source 'https://rubygems.org'
gem 'rails', '4.0.0'
```

- bundle install --path vendor/bundle

- MySQL, SQLite, etc
  - bundle exec rails new .

- No Database, MongoDB, etc
  - bundle exec rails new . --skip-active-record

- vi Gemfile

```
source 'https://rubygems.org'
source 'https://rails-assets.org'

gem 'rails', '4.0.0'
ruby '2.0.0'

- - - - - - - -

# Rails Assets
# https://rails-assets.org/
gem 'rails-assets-bootstrap'
gem 'rails-assets-bootstrap-datepicker'
gem 'rails-assets-select2'

# pagination
# https://github.com/amatsuda/kaminari
gem 'kaminari'

# count page views
# https://github.com/charlotte-ruby/impressionist
gem 'impressionist'

# Settings.hoge
# https://github.com/railsjedi/rails_config
rails_config

# tagging
# https://github.com/mbleigh/acts-as-taggable-on
gem 'acts-as-taggable-on'

# admin
# https://github.com/plataformatec/devise
gem 'devise'
# https://github.com/sferik/rails_admin
gem 'rails_admin'

# deploy
# https://github.com/capistrano/capistrano
# gem 'capistrano'
gem 'capistrano-rbenv'

# monitoring
# https://devcenter.heroku.com/articles/newrelic
gem 'newrelic_rpm'

# cron
# https://github.com/javan/whenever
gem 'whenever', :require => false

# SEO
# http://morizyun.github.io/blog/meta-tags-sitemap-generator-rails-seo/
gem 'meta-tags', :require => 'meta_tags'
gem 'sitemap_generator'

group :development, :test do
  # preloader
  gem 'spring'
end

group :test do
  # Rspec
  gem 'rspec-rails'
end

group :production
  # for heroku
  gem 'rails_12factor'
end

```
