# Size düşen nedir?

Sırayla,

    ~$ git clone git@github.com:seyyah/rails3-devise-rspec-cucumber-sim.git
    ~$ cd rails3-devise-rspec-cucumber-sim/
    ~$ bundle
    ~$ rake db:migrate
    ~$ rake db:seed
    $ rails s --binding=192.168.140.214 --port=3005

Yerelde demo için: http://192.168.140.214:3005

Herokuda demo için: http://rails3-devise-rspec-cucumber.herokuapp.com/

Örnek:
    kullanıcı adı: "user@example.com"
    parola: "secret"

# Nasıl?

Template,

    $ rails new rails3-devise-rspec-cucumber -m
    https://raw.github.com/RailsApps/rails3-application-templates/master/rails3-devise-rspec-cucumber-template.rb
    -T

Kurulum sırasında soruları şöyle yanıtla,

    Would you like to use Haml instead of ERB? No.
    Would you like to use RSpec instead of TestUnit? Yes.
    Would you like to use factory_girl for test fixtures with RSpec? Yes.
    Would you like to use machinist for test fixtures with RSpec? No.
    Would you like to use Cucumber for your BDD? Yes.
    Would you like to use Guard to automate your workflow? No.
    Would you like the app to use a Gmail account to send email? Yes.
    Would you like to use Devise for authentication? Devise with default modules
    Which front-end framework would you like for HTML5 and CSS3? None
    Would you like to use rails-footnotes during development? No.
    Would you like to set a robots.txt file to ban spiders? Yes.

    $ cd myapp/
    $ git init
    $ git add .
    $ git commit -a -m ilk

    $ vim Gemfile
    açıklamalar silindi

    gem 'execjs'
    gem 'therubyracer'

    gem 'rspec-rails', :group => [:development, :test]
    group :test do
      gem 'database_cleaner'
      gem 'factory_girl_rails'
      gem 'email_spec'
    end

    $ bundle

    $ git add .
    $ git commit -a -m rspec:install

    $ rails generate rspec:install

    $ git add .
    $ git commit -a -m rspec:install

    $ vim spec/factories.rb
    ...
    $ mkdir spec/support
    $ vim spec/support/devise.rb
    ...
    $ vim spec/spec_helper.rb
    ...
    $ bundle exec rake db:migrate
    $ bundle exec rake db:test:prepare

    $ vim Gemfile
    ..
    $ bundle

    $ rails generate cucumber:install --capybara --rspec
    $ rails generate email_spec:steps
    $ bundle exec cucumber features/visitors/request_invitation.feature --require features
    $ vim config/cucumber.yml
    std_opts = "-r features/support/ -r features/step_definitions --format #{ENV['CUCUMBER_FORMAT'] || 'pretty'} --strict --tags ~@wip"
    $ cd features
    ...

    $ vim config/environments/development.rb
    # ActionMailer Config
    config.action_mailer.default_url_options = { :host => 'localhost:3000' }
    config.action_mailer.delivery_method = :smtp
    # change to false to prevent email from being sent during development
    config.action_mailer.perform_deliveries = true
    config.action_mailer.raise_delivery_errors = true
    config.action_mailer.default :charset => "utf-8"

    IP adresi güncellendi.

    ...

## Devise

    rails generate devise:install


