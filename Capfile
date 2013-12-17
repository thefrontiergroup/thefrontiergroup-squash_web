require 'rubygems'
require 'bundler/setup'
require 'tfg_cap'

set :application,    'squash'
set :display_name,   'Squash'
set :repository,     'git@github.com:thefrontiergroup/thefrontiergroup-squash_web.git'
set :bundle_without, [:development, :test, :test_mac, :cucumber]
set :ruby_interpreter, 'ruby-1.9.3-p392'
set :ruby_gemset,    'squash'
set :release_regexp, /2013\d{4}/

has_linked_dirs 'private' => 'private'

set(:branch) { ask_for_release_branch }

stage :staging do
  server "inferno.thefrontiergroup.net.au", :app, :web, :db, :primary => true
  set    :domain, 'squash.tfgrails.com'
end
