desc 'outputs hello to the terminal'
namespace :greeting do
    
    task :hello do

        puts "hello from Rake!"
        
    end
    
    task :hola do

        puts "hola de Rake!"
        
    end
    
end

task :console do

    Pry.start
    
end

namespace :db do

    task :migrate => :environment do


        
    end

    task :environment do

        require_relative 'config/environment'
        
    end

    task :seed do

        require_relative 'db/seeds'
        
    end
    
end