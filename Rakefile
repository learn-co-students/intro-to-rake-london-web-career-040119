task :environment do
  require_relative './config/environment.rb'
end

namespace :greeting do
  desc 'outputs hello to the terminal'
  task :hello do
    puts 'hello from Rake!'
  end
  desc 'outputs hello to the terminal'
  task :hola do
    puts 'hola de Rake!'
  end
end

desc 'pry console'
task console: :environment do
  Pry.start
end

namespace :db do
  desc 'migrate changes to your database'
  task migrate: :environment do
    Student.create_table
  end

  desc 'seed the database'
  task seed: :environment do
    Student.create(name: 'Melissa', grade: '10th')
    Student.create(name: 'April', grade: '10th')
    Student.create(name: 'Luke', grade: '9th')
    Student.create(name: 'Devon', grade: '11th')
    Student.create(name: 'Sarah', grade: '10th')
  end
end
