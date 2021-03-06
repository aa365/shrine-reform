# Shrine::Plugins::Reform

Provides [Reform] integration for [Shrine].

## Installation

```ruby
gem "shrine-reform"
gem "shrine", github: "janko-m/shrine"
```

## Usage

The reform plugin can be loaded globally alongside activerecord plugin.

```rb
Shrine.plugin :activerecord
Shrine.plugin :reform
```
```rb
class Post < ActiveRecord::Base
  include ImageUploader[:image]
end
```
```rb
class PostForm < Reform::Form
  include ImageUploader[:image]
end
```

## Contributing

You can run tests with the Rake task:

```
$ bundle exec rake test
```

## License

[MIT](LICENSE.txt)

[Reform]: https://github.com/apotonick/reform
[Shrine]: https://github.com/janko-m/shrine
