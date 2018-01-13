require 'html-proofer'

task :test do
  sh "bundle exec jekyll build"
  options = { assume_extension: true, verbose: true, typhoeus: { ssl_verifyhost: 0 } }
  HTMLProofer.check_directory("./_site", options).run
end

task default: :test
