# DevsincBlogApp

database\_rewinder is a minimalist's tiny and ultra-fast database cleaner.

## Features

* Cleans up tables via DELETE SQL. No other strategies are implemented ATM
* Supports multiple databases
* Runs extremely fast :dash:

## Why is it fast?

database\_rewinder memorizes every table name into which `INSERT` SQL was performed during each test case.
Then it executes `DELETE` SQL only against these tables when cleaning.
So, the more number of tables you have in your database, the more benefit you will get.
Also, database\_rewinder joins all `DELETE` SQL statements and casts it in one DB server call.

### Credit

This strategy was originally devised and implemented by Shingo Morita (@eudoxa) at COOKPAD Inc.

## Supported versions

* Ruby 2.6.6

* Rails 5.2.6

* PostgreSQL 14.1

## Installation

Add this line to your Gemfile's `:test` group:

    gem 'database_rewinder'

And then execute:

    $ bundle

## Usage

