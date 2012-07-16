# Ruby on Rails Splunk App

This is a "fork" of the [Ruby on Rails splunk app](http://splunk-base.splunk.com/apps/22351/ruby-on-rails) on SplunkBase.

(There appears to be no repo on Github for this project, so we're adding it for sharing)

## Features/Improvements

It has all the same features as the above link, supporting Rails 3.x better by:

* Concatenates multi-line logging at Splunk (no need to play with Rails' logger)
* Breaks log entries on "Started" (introduced in Rails 3)
* Supports small RegExp changes for extracting Controller and Action from a log entry

It's also recommended that you configure your Rails logs to not use ANSI coloring like this:

```ruby
# e.g., in config/environments/staging.rb
  config.colorize_logging = false
```