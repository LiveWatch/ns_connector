require 'rubygems'
require 'bundler'
begin
	Bundler.setup(:default, :development)
rescue Bundler::BundlerError => e
	warn e.message
	warn "Run `bundle install` to install missing gems"
	exit e.status_code
end

require 'rdoc/task'
require 'jeweler'
require 'rspec/core/rake_task'

Jeweler::Tasks.new do |gem|
	gem.name = "ns_connector"
	gem.homepage = ""
	gem.summary = "An interface to NetSuite records via RESTlets."
	gem.description = "This library provides an interface to NetSuite via"\
		"'RESTlets'. This appears to be a quicker and more reliable"\
		"way of interfacing with NetSuite records than the SOAP API."
	gem.authors = ["Christian Marie <christian@ru>"]
	gem.license = 'MIT'
end
Jeweler::RubygemsDotOrgTasks.new

task :default => :test
RSpec::Core::RakeTask.new :test 

Rake::RDocTask.new do |rd|
	rd.main = "README.rdoc"
	rd.title = 'NSConnector documentation'
	rd.rdoc_files.include("README.rdoc", "lib/**/*.rb")
end
