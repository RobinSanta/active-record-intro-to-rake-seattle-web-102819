desc 'outputs hello to the terminal'
task :hello do
  puts "hello from Rake!"
end

namespace :greeting do
  task :hello do
    puts "hello from Rake!"
  end
  task :hola do
    puts "hola de Rake!"
  end
end

task :console do
  exit
end

task :environment do
  require_relative './config/environment'
end

namespace :db do
  task :migrate => :environment do
    # Pry.start
    Student.create_table
  end
  task :seed do
    require_relative './db/seeds.rb'
  end
end