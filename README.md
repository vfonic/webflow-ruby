# Webflow [![Build Status](https://github.com/vfonic/webflow-rb/workflows/build/badge.svg)](https://github.com/vfonic/webflow-rb/actions)

## Note

This is an active fork of the great [webflow-ruby](https://github.com/penseo/webflow-ruby) gem. [webflow-ruby](https://github.com/penseo/webflow-ruby) gem still works for Webflow API v1. If you're looking for a similar gem API (method names) but for Webflow API v2, try webflow-rb [api-v2](https://github.com/vfonic/webflow-rb/tree/api-v2) branch.

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'webflow-rb'
```

And then execute:

```bash
bundle
```

Or install it yourself as:

```bash
gem install webflow-rb
```

## Usage

Check out [lib/webflow/client.rb](lib/webflow/client.rb).

Check the official Webflow API v2 documentation at: https://developers.webflow.com/reference/list-collection-items

Basic usage:

```ruby
client = Webflow::Client.new(ENV.fetch('WEBFLOW_API_TOKEN'))
sites = client.sites
```

Here are method signatures:

```ruby
def sites
def site(site_id)
def publish(site_id)
def collections(site_id)
def collection(collection_id)
def list_items(collection_id, limit: 100, offset: 0)
def list_all_items(collection_id)
def get_item(collection_id, item_id)
def create_item(collection_id, data)
def update_item(collection_id, item_id, data)
def delete_item(collection_id, item_id)
```

## Contributing

Bug reports and pull requests are welcome!
If you're missing certain functionality, please open an issue or create a pull request.

## Plugins

- [webflow_sync](https://github.com/vfonic/webflow_sync) - Keep Rails models in sync with WebFlow collections.

## Thanks and Credits

This gem wouldn't be possible without the amazing work of [webflow-ruby](https://github.com/penseo/webflow-ruby) gem. Thank you, [@phoet](https://github.com/phoet) and [@sega](https://github.com/sega)!

## License

The gem is available as open source under the terms of the [MIT License](http://opensource.org/licenses/MIT).
