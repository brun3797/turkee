require 'rubygems'
require 'rake'
require 'bundler'
Bundler::GemHelper.install_tasks

$:.push File.expand_path("../lib", __FILE__)

task :default do
  sh "rspec spec/"
end

begin
  INSTALL_MESSAGE = %q{
  ========================================================================
  Turkee Installation Complete.
  ------------------------------------------------------------------------
  If you're upgrading Turkee (1.1.1 and prior) or installing for the first time, run:

    rails g turkee --skip

  For full instructions on gem usage, visit:
    http://github.com/aantix/turkee#readme

  ** If you like the Turkee gem, please click the "watch" button on the
  Github project page.  You'll make me smile and feel appreciated. :)
    http://github.com/aantix/turkee

  ========================================================================
  }

  Gem::Specification.new do |gem|
    gem.name = "turkee"
    gem.summary = "Turkee makes dealing with Amazon's Mechnical Turk a breeze."
    gem.description = "Turkee will help you to create your Rails forms, post the HITs, and retrieve the user entered values from Mechanical Turk."
    gem.email = "jjones@aantix.com"
    gem.homepage = "http://github.com/aantix/turkee"
    gem.authors = ["Jim Jones"]
    gem.add_dependency(%q<rails>, [">= 3.0.7"])
    gem.add_dependency(%q<rturk>, [">= 2.3.0"])
    gem.add_dependency(%q<lockfile>, [">= 1.4.3"])

    gem.post_install_message = INSTALL_MESSAGE
    gem.require_path = 'lib'
    gem.files = %w(MIT-LICENSE README.textile Gemfile Rakefile init.rb) + Dir.glob("{lib,spec}/**/*")

  end
end
