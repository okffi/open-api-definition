# Config based on the documentation from:
# http://jekyllrb.com/docs/github-pages/

source 'https://rubygems.org'

require 'json'
require 'open-uri'
versions = JSON.parse(open('https://pages.github.com/versions.json').read)

gem 'github-pages', versions['github-pages']
gem 'jekyll-paginate', versions['jekyll-paginate']

gem 'html-proofer'
