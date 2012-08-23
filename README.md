# therubythino-issue-25

A sample (J)Ruby on Rails app that fails to start b/c of an error being raised by therubyrhino (2.0.0).

See <a href="https://github.com/cowboyd/therubyrhino/issues/25">issue 25</a> at the therubyrhino repo for details or to follow along.

## How to reproduce

1. clone this project
2. `cd` into the project directory
3. accept the rvm security thing, if it doesn't prompt you then do `source .rvmrc`
4. bundle
5. rails s

You'll end up with:


```
Rhino::JSError: [ruby LoadError]
     call at /Users/mindscratch/.rvm/gems/jruby-1.6.7@therubyrhino-issue-25/gems/therubyrhino-2.0.0/lib/rhino/rhino_ext.rb:170
  require at /Users/mindscratch/.rvm/gems/jruby-1.6.7@therubyrhino-issue-25/gems/commonjs-0.2.6/lib/commonjs/environment.rb:18
  require at /Users/mindscratch/.rvm/gems/jruby-1.6.7@therubyrhino-issue-25/gems/less-2.2.1/lib/less/loader.rb:22
     Less at /Users/mindscratch/.rvm/gems/jruby-1.6.7@therubyrhino-issue-25/gems/less-2.2.1/lib/less.rb:15
   (root) at /Users/mindscratch/.rvm/gems/jruby-1.6.7@therubyrhino-issue-25/gems/less-2.2.1/lib/less.rb:9
  require at org/jruby/RubyKernel.java:1042
   (root) at /Users/mindscratch/.rvm/gems/jruby-1.6.7@therubyrhino-issue-25/gems/less-2.2.1/lib/less.rb:6
  require at org/jruby/RubyKernel.java:1042
   (root) at /Users/mindscratch/.rvm/gems/jruby-1.6.7@therubyrhino-issue-25/gems/less-rails-2.2.3/lib/less/rails.rb:1
  require at org/jruby/RubyKernel.java:1042
   (root) at /Users/mindscratch/.rvm/gems/jruby-1.6.7@therubyrhino-issue-25/gems/less-rails-2.2.3/lib/less-rails.rb:8
  require at org/jruby/RubyKernel.java:1042
  require at /Users/mindscratch/.rvm/gems/jruby-1.6.7@therubyrhino-issue-25/gems/less-rails-bootstrap-2.1.0/lib/less-rails-bootstrap.rb:68
     each at org/jruby/RubyArray.java:1615
  require at /Users/mindscratch/.rvm/gems/jruby-1.6.7@global/gems/bundler-1.1.3/lib/bundler/runtime.rb:66
     each at org/jruby/RubyArray.java:1615
  require at /Users/mindscratch/.rvm/gems/jruby-1.6.7@global/gems/bundler-1.1.3/lib/bundler/runtime.rb:55
  require at /Users/mindscratch/.rvm/gems/jruby-1.6.7@global/gems/bundler-1.1.3/lib/bundler.rb:119
   (root) at /Users/mindscratch/code/projects/rubyrhino/config/application.rb:7
  require at org/jruby/RubyKernel.java:1042
   (root) at /Users/mindscratch/code/projects/rubyrhino/config/application.rb:53
      tap at org/jruby/RubyKernel.java:1787
   (root) at /Users/mindscratch/.rvm/gems/jruby-1.6.7@therubyrhino-issue-25/gems/railties-3.2.8/lib/rails/commands.rb:50
  require at org/jruby/RubyKernel.java:1042
   (root) at script/rails:6
```

Here's my gem env:

```

RubyGems Environment:
  - RUBYGEMS VERSION: 1.8.15
  - RUBY VERSION: 1.9.2 (2012-02-22 patchlevel 312) [java]
  - INSTALLATION DIRECTORY: /Users/mindscratch/.rvm/gems/jruby-1.6.7@therubyrhino-issue-25
  - RUBY EXECUTABLE: /Users/mindscratch/.rvm/rubies/jruby-1.6.7/bin/jruby
  - EXECUTABLE DIRECTORY: /Users/mindscratch/.rvm/gems/jruby-1.6.7@therubyrhino-issue-25/bin
  - RUBYGEMS PLATFORMS:
    - ruby
    - universal-java-1.7
  - GEM PATHS:
     - /Users/mindscratch/.rvm/gems/jruby-1.6.7@therubyrhino-issue-25
     - /Users/mindscratch/.rvm/gems/jruby-1.6.7@global
  - GEM CONFIGURATION:
     - :update_sources => true
     - :verbose => true
     - :benchmark => false
     - :backtrace => false
     - :bulk_threshold => 1000
     - "install" => "--no-rdoc --no-ri"
     - "update" => "--no-rdoc --no-ri"
     - "gem" => "--no-ri --no-rdoc"
     - :sources => ["http://gems.rubyforge.org", "http://gems.github.com"]
  - REMOTE SOURCES:
     - http://gems.rubyforge.org
     - http://gems.github.com
```
