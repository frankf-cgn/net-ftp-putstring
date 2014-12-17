require 'rubygems'
require 'rake'

begin
  require 'jeweler'
  Jeweler::Tasks.new do |gem|
    gem.name = "net-ftp-putstring"
    gem.summary = %Q{Allow to upload string to a FTP server}
    gem.description = %Q{Allow to upload a string to a FTP server}
    gem.email = "youre-email@youre-domain.io"
    gem.homepage = "http://github.com/frankf-cgn/net-ftp-putstring"
    gem.authors = ["Dan Williams", "ciastek"]
    gem.add_development_dependency "rspec"
  end
  Jeweler::GemcutterTasks.new
rescue LoadError
  puts "Jeweler (or a dependency) not available. Install it with: sudo gem install jeweler"
end

require 'rspec/core/rake_task'
RSpec::Core::RakeTask.new do |t|
  t.rspec_opts = ["-c", "-f progress", "-r ./spec/spec_helper.rb"]
  t.pattern = 'spec/**/*_spec.rb'
end

task :spec => :check_dependencies

task :default => :spec

require 'rdoc/task'
RDoc::Task.new do |rdoc|
  if File.exist?('VERSION')
    version = File.read('VERSION')
  else
    version = ""
  end

  rdoc.rdoc_dir = 'rdoc'
  rdoc.title = "deleteme #{version}"
  rdoc.rdoc_files.include('README*')
  rdoc.rdoc_files.include('lib/**/*.rb')
end
