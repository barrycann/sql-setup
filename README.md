# PostgreSQL Setup

## Heroku

Heroku is a service that offers simple web application hosting with many extra features. We'll use their hosted Postgres service to quickly create a database instance.

https://www.heroku.com

### Sign up

On the Heroku website, click the **Sign up for free** button. After submitting your details you'll be sent a confirmation email. Follow the link found in this email and set your password.

Sign Up Page           |  Email Confirmation
:-------------------------:|:-------------------------:
![Heroku Homepage](https://github.com/statianzo/sql-setup/raw/master/images/heroku_homepage.png)  |  ![Heroku Signup](https://github.com/statianzo/sql-setup/raw/master/images/heroku_signup.png)


### Create an App

On your first visit to the dashboard, click the **Create New App** button.
From there, specify a name (or leave blank and Heroku will generate a name). Click **Create App**

Create New App      |  Add a Name  
:-------------------------:|:-------------------------:
![Heroku Create App](https://github.com/statianzo/sql-setup/raw/master/images/heroku_dashboard.png)  |  ![Heroku Add Name](https://github.com/statianzo/sql-setup/raw/master/images/heroku_newapp.png)


### Provision the Heroku Postgres add-on

At this point, you're in the dashboard for the project you just created. Depending on the size of your browser window, you will see either a "Resources" tab or a set of seven icons near the top of the window. Select the resources tab if you see text options. If you see icons, select the icon with three horizontal lines.
On the next screen, type "postgres" in the "Add-ons" search field and select "Heroku Postgres" from the list.
Provision the Hobby Dev free tier database.

Select the "Resources" Tab | Or the Resources Icon | Select Heroku Postgres | Click Provision
:-------------------------:|:----------------------:|:----------------------:|:----------------------:
![Heroku Resources Tab](https://github.com/statianzo/sql-setup/raw/master/images/heroku_resources_tab.jpg)  |  ![Heroku Resources Icon](https://github.com/statianzo/sql-setup/raw/master/images/heroku_resources_icon.jpg) | ![Heroku Search For Addon](https://github.com/statianzo/sql-setup/raw/master/images/heroku_addon.png) | ![Heroku Povision Database](https://github.com/statianzo/sql-setup/raw/master/images/heroku_provision.png)


### View database credentials

Select the **Heroku Postgres :: Database** add-on from the list. On the database page, click the **View Credentials** button. You will be presented with the credentials necessary to connect to the Postgres instance.

![Heroku Go To Postgres](https://github.com/statianzo/sql-setup/raw/master/images/heroku_gotopg.png)

![Heroku Postgres Dashboard](https://github.com/statianzo/sql-setup/raw/master/images/heroku_pgdashboard.png)

![Heroku Postgres Credentials](https://github.com/statianzo/sql-setup/raw/master/images/heroku_credentials.png)

## SQL Tabs

SQL Tabs is a cross-platform database client that will allow you to execute SQL against your postgres server.

### Install

Download the version for your OS from http://www.sqltabs.com and install accordingly

- OS X: unzip the download and put it in your Applications
- Windows: unzip the download and place the folder somewhere easy to access, like your desktop. Run **sqltabs.exe**.
- Linux: gunzip the tarball and execute `./sqltabs`


![SQL Tabs Download](https://github.com/statianzo/sql-setup/raw/master/images/sqltabs_download.png)

### Connect to Postgres

Copy the **URI** from your Heroku Postgres credentials. Paste it into the connection string input at the top of SQL Tabs and **IMPORTANT: append `?ssl=true` to the end.**

![SQL Tabs URI](https://github.com/statianzo/sql-setup/raw/master/images/sqltabs_uri.png)

### Test

Run a `select 'Hello World'` query against the database to ensure you're connected. Execute the query using ⌘-R or Ctrl-R. If the database responds with Hello World, you're good to go.

![SQL Tabs Hello World](https://github.com/statianzo/sql-setup/raw/master/images/sqltabs_helloworld.png)
