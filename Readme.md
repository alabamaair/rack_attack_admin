# Rack::Attack Admin Dashboard  [![Gem Version](https://badge.fury.io/rb/rack_attack_admin.svg)](https://badge.fury.io/rb/rack_attack_admin)

Lets you see the current state of all throttles and bans. Delete existing keys/bans. Manually add bans.

Inspired by: https://www.backerkit.com/blog/building-a-rackattack-dashboard/

(screenshot)

## Installation

Add this line to your application's `Gemfile`:

```ruby
gem 'rack_attack_admin'
```

And then execute:

    $ bundle


Add this line to your application's `config/routes.rb`:

```ruby
mount RackAttackAdmin::Engine, at: '/admin/rack_attack'
```

## Usage

Go to '/admin/rack_attack' in your browser!

## Flags

## Fail2Ban/Allow2Ban

In order to allow your Fail2Ban/Allow2Ban rules to be introspected by this app, you must define them
slightly differently than the upstream Rack::Attack suggest:

...

## Compatibility

This has mostly been tested with `Rack::Attack.cache.store` set to an instance
of `Redis::Store` from the fantastic
[redis-store](https://github.com/redis-store/redis-store) gem. (Which is used by the
`ActiveSupport::Cache::RedisStore` (from redis-activesupport/redis-rails gems))

Now that Rails 5.2+ provides its own built-in `ActiveSupport::Cache::RedisCacheStore`, you may set
`Rack::Attack.cache.store` to an instance of that store instead.
```ruby
```

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/TylerRick/rack_attack_admin.
