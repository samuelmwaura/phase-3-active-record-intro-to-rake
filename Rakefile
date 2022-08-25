namespace :greeting do
  desc "outputs hello to the terminal"
  task :hello do
    puts "hello from Rake!"
  end

  task :hola do
    puts "hola de Rake!"
  end

end

task :environment do
  require_relative "./config/environment"
end

#migration in ruby means that you change your db from a current version to another 1 either by changing schema or the data inside 
namespace :db do
  desc "migrate changes to your database"
  task migrate: :environment do
    Student.create_table
  end
  
  #seed the database with some dummy data
  desc "seed the db with some dummy data"
  task seed: :environment do
   require_relative './db/seeds'
  end
end

#open up a pry session - meant to interact with our class or db without having to run an entire program
desc "drop into the pry console"
task console: :environment do
  pry.start
end


#Used to speed up the development process by automating some of the setup and testing tasks.