eliteedu
========
This is a fork of the open source School management system known as Fedena, few customization have been done to fix issues and to fit the need of the local institutions.
 Installation steps
1.Download eliteedu bundle patched source code from Download section. Extract the ZIP/TAR archive and save to a folder (say C:\Fedena).
2.Now goto the fedena source directory in the command window.
3.Run the command "gem install bundler --remote" to install Bundler gem.
4.Run the command "bundle install --local".
5.Update the MySQL database details in config/database.yml (under "development:")
6.Run the command "rake db:create". This will create the required database.
7.If your MySQL user does not have database creation privilages, just create the database from your Database manager and you may skip this step.
8.Run the command "rake fedena:plugins:install_all". This will populate the database with required tables.
9.Finally, run the command "mongrel_rails start".This would start the server and it will be accessible at http://localhost:3000
10.If you want to run Fedena in production mode, run the command "mongrel_rails start -e production". For this, Production database details should be given in config/database.yml
