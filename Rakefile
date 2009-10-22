require 'rubygems'
require 'rake'
require 'pathname'

begin
  require 'jeweler'
  Jeweler::Tasks.new do |gem|
    gem.name = "riot-js"
    gem.summary = %Q{JS version of the Riot testing framework}
    gem.description = %Q{JS version of the Riot testing framework}
    gem.email = "gabriel.gironda@gmail.com"
    gem.homepage = "http://github.com/gabrielg/riot-js"
    gem.authors = ["ggironda"]
    
    gem.add_dependency "xpcomcore-rubygem"
    gem.add_development_dependency "jsdoc-toolkit"
  end
  Jeweler::GemcutterTasks.new
rescue LoadError
  puts "Jeweler (or a dependency) not available. Install it with: sudo gem install jeweler"
end



gem 'jsdoc-toolkit'
require 'jsdoc-toolkit/doc_task'
desc "Builds the docs."
JsDocToolkit::DocTask.new(:doc) do |doc|
  doc.jsdoc_dir = 'xpcomcore/doc'
  doc.jsdoc_files << 'xpcomcore/lib'
end

task :test => :check_dependencies
task :default => :test