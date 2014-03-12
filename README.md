# AttrDefaultable

Easily add attributes with default values to your classes.

## Installation

Add this line to your application's Gemfile:

    gem 'attr_defaultable'

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install attr_defaultable

## Usage

```ruby
class Example
  extend AttrDefaultable
  attr_defaultable :foo, -> { 'bar' }
end
```

This will create a getter/setter pair for your variable `foo`. If the setter is not used before the getter
the proc given will be called and it's result used to set the value of `foo`.

Very useful for creating dependency definitions with protected default values that are evaluated just in time.

## Contributing

1. Fork it ( http://github.com/<my-github-username>/attr_defaultable/fork )
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request
