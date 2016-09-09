# COLANTOTTE
Framgia x COLANTOTTE

## Requirements
- Ruby 2.3.x (2.3.1)
- Rails 4.2.x (4.2.6)
- Mysql 5.x (5.6)

## Configure Options

#### Database config 
```cmd
cp database.yml.example database.yml
```

#### Secrets config

```cmd
cp secrets.yml.example secrets.yml

```
#### .env file

Need .env file with production or staging enviroment
```cmd
sudo nano .env
```
Update Key follow description

Properties        | Description |
---                       |  ---|
RAILS_SERVE_STATIC_FILES | This will allow a new Rails 4.2+ app to serve static assets by default as a result of this pull request to Rails |
RUBYCOLANTOTTE_USER_NAME | Define user access database Mysql |
RUBYCOLANTOTTE_DATABASE_PASSWORD | Password for user |
SECRET_KEY_BASE | Run `rake secret` |
DOMAIN_HOST | Domain name of system |
MAIL_PORT | Port send mail (587, 495, 2525) |
MAIL_USERNAME | User name login to mail server |
MAIL_PASSWORD | Password login to mail server |
MAIL_HOST | Mail host (smtp.gmail.com ...) |
MAIL_DOMAIN_HOST | Domain host (gmail.com ...) |
MAIL_SENDER | COLANTOTTE |
MAIL_FROM | collantotte@framgia.com |

## Installation

##### Install all package

```ruby
bundle install
```

##### Database

```ruby
rake db:create
rake db:migrate
rake db:seed
```

If production:

```ruby
rake db:create RAILS_ENV=production
rake db:migrate RAILS_ENV=production
rake db:seed RAILS_ENV=production
```

#### Build i18njs

```ruby
rake i18n:js:export
```

##### Precompile assets

```ruby
rake assets:precompile RAILS_ENV=production
```

## Run

```ruby
rails s
```

Or

```ruby
rails s -e production
```
