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

- bundle install

- MySQL
  - bundle exec rails new . -d mysql

- No Database, MongoDB, etc
  - bundle exec rails new . --skip-active-record

- vi Gemfile

```
source 'https://rubygems.org'
source 'https://rails-assets.org'

ruby '2.0.0'

gem 'rails', '4.0.0'

gem 'mysql2'

- - - - - - - -

# bootstrap
# https://github.com/anjlab/bootstrap-rails
gem 'anjlab-bootstrap-rails', :require => 'bootstrap-rails',
    :github => 'anjlab/bootstrap-rails'

# pagination
# https://github.com/amatsuda/kaminari
gem 'kaminari'

# count page views
# https://github.com/charlotte-ruby/impressionist
gem 'impressionist'

# Settings.hoge
# https://github.com/railsjedi/rails_config
gem 'rails_config'

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

group :production do
  # for heroku
  gem 'rails_12factor'
end
```

```
vi config/database.yml
```

```
development:
  adapter: mysql2
  encoding: utf8
  reconnect: false
  database: dbname_development
  pool: 5
  username: root
  password: root
  host: localhost
```

```
rake db:setup
bundle exec rails s
git init
git add -a
git commit
```

http://localhost:3000/


