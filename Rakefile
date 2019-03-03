

# 1. define tasks and namespace them
namespace :greeting do

  desc 'outputs hello to the terminal'
  task :hello do
    puts "hello from Rake!"
  end

  desc 'outputs hello to the terminal'
  task :hola do
    puts "hola de Rake!"
  end
end

#rake greeting:hello    
#hello from Rake!             rake hello
 
#rake greeting:hola
#hola de Rake!                rake hola


# 2.Giving access to db
task :environment do
  require_relative './config/environment'
end

# 3. Migrate
namespace :db do
  desc 'migrate changes to your database'   # rake db:migrate  call in termminal
  task :migrate => :environment do
    Student.create_table
  end

# 4. seed some examples under the same db namespace
  desc 'seed the database with some dummy data'
  task :seed do
    require_relative './db/seeds.rb'
  end
end
# 5. interact with class and da without running the program by using console
  desc 'drop into the Pry console'
  task :console => :environment do  # We'll make this task dependent on our environment task so that the Student class and the database connection load first.
    Pry.start
  end

