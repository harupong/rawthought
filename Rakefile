JEKYLL_DIR = "_site"
directory JEKYLL_DIR
desc 'Build jekyll site and publish to GitHub Pages'
task :publish => JEKYLL_DIR do
  sh "rm -rf #{JEKYLL_DIR}/"
  sh "jekyll build"
  sh "git commit -a -m \"Add new post\""
  sh "git push origin jekyll-source"

  cd "#{JEKYLL_DIR}" do
    sh "git commit -a -m \"Publish new post\""
    sh "git push origin gh-pages"
  end

end
