# Rails API Boilerplate

A template of Rails API only app. You can use this template as base template for any Rails API only app.

## Table of Contents

- [Setup](#setup)
- [Versions](#versions)
- [GemList](#gemlist)
- [Scaffolding](#scaffolding)
- [Documentation](#documentation)
- [SampleCURL](#samplecurl)

## Setup

- [Install Ruby](https://www.ruby-lang.org/en/documentation/installation)
- [Install Ruby on Rails](https://guides.rubyonrails.org/v5.0/getting_started.html#installing-rails)
- [Clone this template](https://docs.github.com/en/github/creating-cloning-and-archiving-repositories/cloning-a-repository)
- [Run it locally](https://guides.rubyonrails.org/v5.0/getting_started.html#starting-up-the-web-server)

## Versions

- Ruby - 3.0.0
- Ruby on Rails - 6.1.1

## GemList

Recommended Gems
- devise
- jwt
- versionist
- active_model_serializers
- redis-rails
- apitome
- bullet
- brakeman
- rubocop

## Scaffolding

- Controllers

```text
app/controllers
├── application_controller.rb
├── concerns
├── v1
│   ├── base_controller.rb
│   └── users_controller.rb
└── v2
    └── users_controller.rb
```

- Serializers

```text
app/serializers/
├── v1
│   ├── expense_serializer.rb
│   └── user_serializer.rb
└── v2
    └── user_serializer.rb
```

## Documentation

- Ganerate documentation
  ```ruby
  $ rake docs:generate
  ```

- Documentation route
  ```ruby
  http://localhost:3000/api/docs
  ```

## SampleCURL

```sh
curl --location --request GET 'localhost:3000/users' \
--header 'Accept: application/vnd.boilerplate-rails.com; version=1' \
--header 'X-Api-Key: eyJhbGciOiJIUzI1NiJ9.eyJleHAiOjE2MTc5MzgxMjYsInVzZXJfaWQiOiIxIn0.Lc52z1w_9FvsIHTvrRx0ezhpl4BOljwRC0-A_thIIVM'
```