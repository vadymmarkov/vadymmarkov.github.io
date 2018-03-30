# frozen_string_literal: true

GITHUB_REPONAME = 'vadymmarkov.github.io'

desc 'Generate blog files'
task :generate do
  system 'JEKYLL_ENV=production bundle exec jekyll build'
end

desc 'Publish website to gh-pages'
task :publish => [:generate] do
  system 'git checkout master'
  system 'rm -rf assets *.html'
  system 'cp -a _site/. .'
  system 'rm -rf _site'
  commit
  system 'git push origin master'

  system 'git checkout sources'
  commit
  system 'git push origin sources'
end

def commit
  system 'git add .'
  message = "Site updated at #{Time.now.utc}"
  system "git commit -m #{message.inspect}"
end
