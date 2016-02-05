# Screencap

A screenshot gem you can use from your ruby application. Uses Phantom.js under the hood.

## Installation

Add this line to your application's Gemfile:

    gem 'screencap', github: 'beevelop/screencap'

And then execute:

    bundle

Or install it yourself as:

    gem install screencap

## Usage

```ruby
require 'screencap'

f = Screencap::Fetcher.new('http://google.com')
screenshot = f.fetch
```

it also currently supports a couple of options

```ruby
f = Screencap::Fetcher.new('http://google.com')
screenshot = f.fetch(
  :output => '~/my_directory.png', # don't forget the extension!
  # optional:
  :div => '.header', # selector for a specific element to take screenshot of
  :width => 1024,
  :height => 768,
  :top => 0, :left => 0 # dimensions for a specific area
)
```
