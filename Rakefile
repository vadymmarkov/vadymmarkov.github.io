# frozen_string_literal: true

GITHUB_REPONAME = 'vadymmarkov.github.io'

desc 'Generate blog files'
task :generate do
  system 'bundle exec jekyll build'
end

desc 'Generate and publish blog to gh-pages'
task :publish => [:generate] do
  
end
