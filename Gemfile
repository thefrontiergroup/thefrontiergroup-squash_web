source 'https://rubygems.org'

# Load all files under the Gemfile.d directory.

Dir.glob(File.join(File.dirname(__FILE__), 'Gemfile.d', '*.rb')).sort.each do |file|
  eval File.read(file), binding, file
end

group :development do
  gem "tfg_cap", :require => nil, :git => 'git@github.com:thefrontiergroup/tfg-cap.git'
  gem "rvm",     :require => nil
end
