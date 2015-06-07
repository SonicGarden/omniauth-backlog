# Omniauth::Backlog

Welcome to your new gem! In this directory, you'll find the files you need to be able to package up your Ruby library into a gem. Put your Ruby code in the file `lib/omniauth/backlog`. To experiment with that code, run `bin/console` for an interactive prompt.

TODO: Delete this and the text above, and describe your gem

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

Backlog is managed by space-id, used backlog url. (ex. https://xxxx.backlog.jp)
Backlog's oauth endpoint uses space url. so it need to configure site in client_options.

```ruby
use OmniAuth::Builder do
 provider :backlog, ENV['CLIENT_ID'], ENV['CLIENT_SERCRET'], :client_options => { :site => 'https://yourspaceid.backlog.jp' }
end
```

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/[USERNAME]/omniauth-backlog. This project is intended to be a safe, welcoming space for collaboration, and contributors are expected to adhere to the [Contributor Covenant](contributor-covenant.org) code of conduct.


## License

The gem is available as open source under the terms of the [MIT License](http://opensource.org/licenses/MIT).

