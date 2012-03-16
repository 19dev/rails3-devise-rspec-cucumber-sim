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
$ rails generate rspec:install



