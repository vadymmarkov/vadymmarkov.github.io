# frozen_string_literal: true

GITHUB_REPONAME = 'vadymmarkov.github.io'

desc 'Generate blog files'
task :generate do
  system 'JEKYLL_ENV=production bundle exec jekyll build'
end

desc 'Publish website to gh-pages'
task :publish => [:generate] do
  system 'git checkout master'
  system 'cp -a _site/. .'
  system 'rm -rf _site'
end
