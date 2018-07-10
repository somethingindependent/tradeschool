require 'html-proofer'

task :test do
  sh "bundle exec jekyll build"
  options = { assume_extension: true, verbose: true, only_4xx: true }
  HTMLProofer.check_directory("./_site", options).run
end

task default: :test
