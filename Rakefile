namespace :greeting do
  desc 'outputs hello to the terminal'
  # We run 'rake -T' in the terminal to view a list of available Rake tasks and their descriptions.
    task :hello do
      puts "hello from Rake!"
  end
 # We define tasks with task + name of task as a symbol + a block that contains the code we want to execute

  desc 'outputs hola to the terminal'
    task :hola do
      puts "hola de Rake!"
  end
end

namespace :db do
  desc 'migrate changes to your database'
  task migrate: :environment do
    Student.create_table
  end

  task :environment do
    require_relative './config/environment'
  end

  desc 'seed the database with some dummy data'
  task seed: :environment do
    require_relative './db/seeds'
  end

end

desc 'drop into the Pry console'
task console: :environment do
  Pry.start
end

task :environment do
  require_relative "./config/environment"
end



