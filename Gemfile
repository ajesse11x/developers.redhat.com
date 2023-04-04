# Gemfile
source "http://rubygems.org"
#source "http://rubygems.org" # Try this without ssl for now

# Platform helpers
def windows_only(require_as)
  RbConfig::CONFIG['host_os'] =~ /mingw|mswin/i ? require_as : false
end

def linux_only(require_as)
  RbConfig::CONFIG['host_os'] =~ /linux/ ? require_as : false
end

def darwin_only(require_as)
  RbConfig::CONFIG['host_os'] =~ /darwin/ ? require_as : false
end

# GEMS
#gem 'awestruct', '0.5.7'
gem 'awestruct', git: 'https://github.com/lightguard/awestruct', branch: 'feature/perf-testing-large-site'
#gem 'awestruct', path: '~/projects/ruby/awestruct'
gem 'slim', '~> 3.0'
gem 'kramdown', '~> 2.3.0'
gem 'asciidoctor', '~> 1.5.8'
gem 'uglifier', '~> 2.7.2'
gem 'htmlcompressor', '~> 0.0.6'
gem 'curb', '~> 0.8.5'
gem 'oauth', '~> 0.5.5'
gem 'git', '~> 1.13.0'
gem 'oily_png', '~> 1.1.1'
gem 'nokogiri', '~> 1.13', '>= 1.13.9'
gem 'therubyracer', platforms: :ruby, require: linux_only('therubyracer')
gem 'parallel', '~> 1.1'
gem 'mime-types', '2.1'
gem 'google-api-client', '~> 0.9'
gem 'signet', '~> 0.7', '>= 0.7.3'
gem 'gpgme', '~> 2.0'
gem 'ruby-duration', '~> 3.2', '>= 3.2.3'
gem 'daybreak'
gem 'sass', '~> 3.4', '< 3.4.6'
gem 'activesupport', '~> 6.1', '>= 6.1.7.3' # Used in aweplug by ruby-duration
gem 'compass', '~> 1.0', '>= 1.0.3'
gem 'rake', '~> 12.3', '>= 12.3.3'
gem "octokit", "~> 4.6", ">= 4.6.0"
gem 'docker-api', :require => 'docker'
gem 'uuid'
gem 'listen', '3.0.8'
gem 'akamai-edgegrid', '1.0.6'
# To use Aweplug code from a different location:
#
# From a specific GitHub branch. Ommit the 'branch' parameter for 'master'
#    gem 'aweplug', github: '<github_id>/aweplug', :branch => '<branch_name>'
#
# From a location on your disk:
#
gem 'aweplug', git: 'https://github.com/awestruct/aweplug'

group :test do
  gem 'climate_control'
  gem 'guard'
  gem 'guard-minitest'
  gem 'launchy', '~> 2.4', '>= 2.4.3'
  gem 'rubocop', '~> 0.49.0'
  gem 'minitest-reporters'
  gem 'rspec', '~>3.3'
  gem 'parallel_tests', '~> 1.9.0'
  gem 'require_all', '~> 1.3.2'
  gem 'mocha'
  gem 'faker', '~> 1.6', '>= 1.6.6'
  gem 'report_builder', '~> 0.1.3'
  gem 'webmock', '~> 2.1', '>= 2.1.0'
end

group :development do
  gem 'rb-inotify', require: false
  gem 'rb-fsevent', require: false
  gem 'rb-fchange', require: false
  gem 'pry', require: false
  gem 'pry-byebug', require: false
end

# group :vdiff do
#   gem 'wraith', '~> 1.3.0'
# end

# group :health do
#   gem 'blinkr', '~> 0.3'
# end