# MongoMapper ORM for Devise

## Installation

This version is for Devise >= 2.1.0.

Add mongo_mapper and devise-mongo_mapper to your Gemfile

    gem 'mongo_mapper'
    gem 'devise-mongo_mapper',
      :git    => 'git://github.com/polar/devise-mongo_mapper

Comment out the current ORM in config/initializers/devise.rb, and add:

    require 'devise/orm/mongo_mapper'

Configure your model:

    class User
      include MongoMapper::Document
      devise :registerable, :database_authenticatable, :recoverable
    end
