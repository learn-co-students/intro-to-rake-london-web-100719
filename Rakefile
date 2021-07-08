desc 'outputs hello to the terminal'
namespace :greeting do
  task :hello do
    puts "hello from Rake!"
  end

  task :hola do
    puts "hola de Rake!"
  end
end

desc 'require ./config/environment.rb'
task :environment do
  require_relative './config/environment.rb'
end

desc 'drop into the Pry console'
task :console => :environment do
  Pry.start
end

namespace :db do
  desc 'create the students table in the database'
  task :migrate => :environment do
    Student.create_table
  end

  desc 'seed the database with dummy data'
  task :seed do
    require_relative './db/seeds.rb'
  end
end