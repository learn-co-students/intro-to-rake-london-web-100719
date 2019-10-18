require 'pry'

task :environment do 
  require_relative './config/environment'
end 

namespace :greeting do 
  desc 'outputs hello'
  task :hello do 
    puts "hello from Rake!"
  end 
  desc 'outputs hola'
  task :hola do 
    puts "hola de Rake!"
  end 
end 

namespace :db do 
  desc 'migrates changes to database'
  task migrate: :environment do 
    Student.create_table 
  end 
  desc 'seed database with dummy data'
  task seed: :environment do 
    require_relative './db/seeds.rb'
  end 
end 

desc 'Start pry'
task console: :environment do 
  Pry.start
end 