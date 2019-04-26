Click [here](https://todoster-zoe-kramer.herokuapp.com/) to visit ToDo.

# ToDo

### Overview

A web application, built with Ruby on Rails, that allows users to enter in a task and cross it out upon completion. This app utlizes jQuery to display the tasks and cross them off without needing to refresh the page. 

### Code Structure

**Models**:

*Task Model* - [`app\models\task.rb`](https://github.com/ZoeBKramer/todo/blob/master/app/models/task.rb)

This model has no validations. 

**Views**:

*Static Pages Index View* - [`app\views\static_pages\index.html.erb`](https://github.com/ZoeBKramer/todo/blob/master/app/views/static_pages/index.html.erb)

![Static Pages Index View Page Image](https://raw.githubusercontent.com/ZoeBKramer/todo/master/app/assets/images/todoster.png)

*Tasks Javascript* - [`app\assets\javascripts\tasks.js`](https://github.com/ZoeBKramer/todo/blob/master/app/assets/javascripts/tasks.js)

*Header* - [`app\views\layouts\application.html.erb`](https://github.com/ZoeBKramer/todo/blob/master/app/views/layouts/application.html.erb)

Controls what is displayed in the header of the application.

**Controllers**:

*Tasks Controller* - [`app\controllers\tasks_controller.rb`](https://github.com/ZoeBKramer/todo/blob/master/app/controllers/tasks_controller.rb)

* Index Method: Displays all the tasks on the page in the order of their ID and renders the task in JSON format.  

* Update Method: Finds the task by ID and then updates the task if the data entered is valid and renders the task in JSON format. 

* Create Method: Creates a task if the data entered is valid and renders the task in JSON format.

**Gemfiles**:

[jquery-rails gem](https://github.com/rails/jquery-rails) - jQuery is a fast, small, and feature-rich JavaScript library. It makes things like HTML document traversal and manipulation, event handling, animation, and Ajax much simpler with an easy-to-use API that works across a multitude of browsers.

# Set Up Vagrant

Click [here](https://github.com/university-bootcamp/coding-environment/blob/master/windows-vagrant.md) to find the instructions for setting up Vagrant.

### Vagrant

Between each of the coding sessions you do, especially if you restart your machine, you will need to run the following command to start your vagrant environment prior to connecting:

`vagrant up`

When this command completes, run the vagrant ssh command to log in to Vagrant.

After this completes, you will be taken to a coding environment inside your virtual machine, and your terminal should contain the green [ENV].

Running the `killall ruby` command in your terminal should quit all running Rails servers.

**To ensure that your server is not running** -— If you visit the URL [http://localhost:3030](http://localhost:3030) in your browser, you should not see a web page load. You should ensure that your server is not running before starting new server windows.

**If you want to preview the application that is running within your coding environment**—Visiting the [http://localhost:3030](http://localhost:3030) from your web browser will allow you to do this.

All the files within this folder inside the Vagrant environment will be automatically synced outside the Vagrant environment to folder inside the `coding-environment/src` folder that is located outside the virtual machine, usually on your Desktop.

# Set Up ToDo

### Checking Out the Repo

Check this repository out into your `coding-environment/src` folder. 

### Create the Initial Database

Connect to your Vagrant instance, change the directory `cd /vagrant/src/todo`

Run `rake db:create`

### Starting Up Your Server

In a separate terminal, change the directory `cd /vagrant/src/todo`

Start your server by running `rails server -b 0.0.0.0 -p 3000`
