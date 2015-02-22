[![Gem Version](https://badge.fury.io/rb/tuning.svg)](http://badge.fury.io/rb/tuning) [![Code Climate](https://codeclimate.com/github/museways/tuning/badges/gpa.svg)](https://codeclimate.com/github/museways/tuning) [![Build Status](https://travis-ci.org/museways/tuning.svg?branch=0.2.3)](https://travis-ci.org/museways/tuning) [![Dependency Status](https://gemnasium.com/museways/tuning.svg)](https://gemnasium.com/museways/tuning)

# Tuning

Common tools used in rails extracted into a gem.

## Install

Put this line in your Gemfile:
```ruby
gem 'tuning'
```

Then bundle:
```
$ bundle
```

## Controllers

Use error method to respond with status 500 and show 500.html (if format it's html):
```ruby
error
```

Use not_found to respond with status 404 and show 404.html (if format it's html):
```ruby
not_found
```

Use unauthorized to respond with status 401 and show 422.html (if format it's html):
```ruby
unauthorized
```

Use forbidden to respond with status 403 and show 422.html (if format it's html):
```ruby
forbidden
```

Use unprocessable_entity to respond with status 422 and show 422.html (if format it's html):
```ruby
unprocessable_entity
```

## Views

Use content_tag_if if you want wrap content into some tag if certain condition it's true:
```erb
<%= content_tag_if request.path == home_path, :h1 do %>
  <%= link_to 'Home', home_path, id: 'logo' %>
<% end %>
```

Use active_trail? if you want to check if some path is on active trail:
```erb
<li class="<%= 'active' if active_trail? some_path %>"></li>
```

## Credits

This gem is maintained and funded by [museways](http://museways.com).

## License

It is free software, and may be redistributed under the terms specified in the MIT-LICENSE file.
