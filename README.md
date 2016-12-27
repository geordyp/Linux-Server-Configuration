# Linux_Server_Configuration
For this project, I configured a linux server to deploy my Item_Catalog web
application. The server was an Amazon EC2 instance provided by Udacity. The URL
can be found below. I first updated all the installed packages and configured
the local timezone to UTC (United States, central). Then I secured the server
by configuring the Uncomplicated Firewall. After that, I set up a new user,
grader, with sudo permissions and ensured grader would be able to log in with
an ssh key before continuing. I wanted to get those configurations done early
to avoid losing a lot of work in the event that I was locked out of the server.

Then I began to set up my web application. I first installed Apache and
configured it with mod_wsgi to serve the application. I then installed
PostgreSQL which held the data for the application. Once those were set up,
I installed git to clone my Item_Catalog project onto the server. I had to
re-work some of the code to work with PostgreSQL, but the app is now live and
fully functional.

# Project Information
- IP address: 35.166.218.220
- SSH port: 2200
- URL: http://ec2-35-166-218-220.us-west-2.compute.amazonaws.com
- Username: grader
- Password: see "Notes to Reviewer"

# Software Installed
- finger: user information lookup program
- Apache: web server to handle HTTP requests
- mod_wsgi: Apache was configured to hand-off certain requests to this
  application handler
- PostgreSQL: database server used to serve the data in the web application
- git: version control system, used to pull down my Item_Catalog project

# Third-Party Resources
https://discussions.udacity.com/t/markedly-underwhelming-and-potentially-wrong-resource-list-for-p5/8587
https://help.ubuntu.com/community/UbuntuTime#Using_the_Command_Line_.28terminal.29
https://www.digitalocean.com/community/tutorials/how-to-set-up-ssh-keys--2
https://www.digitalocean.com/community/tutorials/how-to-deploy-a-flask-application-on-an-ubuntu-vps
https://www.tutorialspoint.com/postgresql/postgresql_create_database.htm
http://killtheyak.com/use-postgresql-with-django-flask/
http://docs.sqlalchemy.org/en/latest/core/engines.html
