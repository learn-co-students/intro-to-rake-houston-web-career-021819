task :environment do
  require_relative './config/environment'
end

namespace :greeting do
  
  desc 'outputs hello to the terminal'
  task :hello do
    puts "hello from Rake!"
  end

  desc 'outputs hola to the terminal'
  task :hola do
    puts "hola de Rake!"
  end

end

namespace :db do
  
  desc 'migrate changes to your database'
  task :migrate => :environment do
    Student.create_table
    puts "creating table in the db..."
  end

  desc 'seeds the database with dummy data'
  task :seed do 
    require_relative './db/seeds.rb'
    puts "adding seed data to the db..."
  end 

end

desc 'drop into the Pry console'
task :console => :environment do
  Pry.start
end 