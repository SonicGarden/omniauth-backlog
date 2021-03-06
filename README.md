# Omniauth::Backlog

This is omniauth strategy for authenticating to your Backlog service used OAuth 2.0 style.

Backlog is project management tools served by [Nulab Inc](https://nulab-inc.com).


## Installation

Add this line to your application's Gemfile:

```ruby
gem 'omniauth-backlog'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install omniauth-backlog

## Usage

Backlog is managed by space-id, used backlog url (ex. https://xxxx.backlog.jp).
Backlog's oauth endpoint uses space url. so it need to configure space-id.


```ruby
use OmniAuth::Builder do
    provider :backlog, ENV['CLIENT_ID'], ENV['CLIENT_SERCRET'],
      :space_id => 'yourspaceid'
end
```

It can set site-url directly.

```ruby
use OmniAuth::Builder do
  provider :backlog, ENV['CLIENT_ID'], ENV['CLIENT_SERCRET'],
    :client_options => {
      :site => 'https://yourspaceid.backlog.jp'
    }
end
```

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/attakei/omniauth-backlog.

0. Fork it
0. Create your feature branch (git checkout -b my-new-feature)
0. Commit your changes (git commit -am 'Add some feature')
0. Push to the branch (git push origin my-new-feature)
0. Create new Pull Request

## License

The gem is available as open source under the terms of the [MIT License](http://opensource.org/licenses/MIT).

