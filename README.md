# Profiles REST API

Creating a REST API in Python to manage users Profiles. Application is deployed over AWS.

deploy/setup.sh --> To setup the application on server
deploy/update.sh --> To update the application with the latest updates
path of app on server -- /usr/local/apps/profiles-rest-api

--------------------------------------------------------------------------------

## Project setup commands

### Git

Use the below Git commands in the Windows Command Prompt or macOS Terminal.

Configure default email and name

Note: This only needs to be done the first time you use Git on your machine

git config --global user.email "your@email.com"
git config --global user.name "Your Name"
Initialise a new Git repository

git init
Commit changes to Git

git add .
git commit -am "Commit message"
Set Git remote

Note: This only needs to be done once, the details are provided by GitHub after creating a new project

git remote add origin <URL TO PROJECT>
git push -u origin master
Push changes to GitHub

git push origin


### SSH Key Management

The below commands are used to manage SSH keys on your local development machine.

Checking for existing SSH key

ls ~/.ssh/
Print contents of public key

cat ~/.ssh/id_rsa.pub
Generate new SSH key on your local machine

ssh-keygen -t rsa -b 4096 -C "EMAIL ADDRESS"


### Virtual Environments

The below commands are used for managing Virtual Environments using Python3-env. Use these commands when connected to your Vagrant server.

Create new environment

python -m venv ~/env
Activate virtual environment

source ~/env/bin/activate
De-activate virtual environment

deactivate
Install requirements from requirements.txt

Note: Virtual environment must be activated

pip install -r requirements.txt


### Django Management Commands

Create new Django project

django-admin.py startproject profiles_project  .
Create new Django app

python manage.py startapp profiles_api
Start Django development server

python manage.py runserver 0.0.0.0:8000
Create database migrations file

python manage.py makemigrations
Run migrations

python manage.py migrate
Create new superuser

python manage.py createsuperuser

### Vagrant


These commands are used for managing Vagrant using the GitBash or Terminal windows.

Initialise Vagrant on project
vagrant init ubuntu/bionic64
Start Vagrant box

vagrant up
Connect to Vagrant box

vagrant ssh
Disconnect from Vagrant box

Note: This command is a standard linux command for ending an SSH session

exit
Stop Vagrant box

vagrant halt
Remove Vagrant box

vagrant destroy
Update Vagrant box image

Note: you must rebuild the image after updating

vagrant box update

### Terminal / GitBash Commands

Change directory

cd /directory_name
Change to parent directory

cd ..


### AWS server
connect to AWS server -> ssh ubuntu@[Public IPv4 DNS]

setup.sh on the AWS server -> curl -sL [raw path of setup.sh in github] | sudo bash -

Run django on server -> sudo env/bin/python manage.py createsuperuser




--------------------------------------------------------------------------------


## Functions of the API:

### 1. Create new profiles
    -> Handle registration of new users
    -> Validate profile Database

### 2. Listing existing profiles
    -> Search for profiles
    -> Email and name

### 3. View specific profiles
    -> Profile ID

### 4. Update profile of logged in user
    -> Change name, email and password

### 5. Delete Profile



## URLs of the API:

### 1. /api/profile/
    -> List all profiles when HTTP GET method is called
    -> Create new profile when HTTP POST method is called

### 2. /api/profile/<profile_id>/
    -> View specific profile details by using HTTP GET
    -> Update object using HTTP PUT / PATCH
    -> Remove it completely using HTTP DELETE



--------------------------------------------------------------------------------


## Functions of Feed API:

    -> Creating new feed items -- Logged in users only
    -> Update feed items -- Logged in users only
    -> Deleting profile feed items -- Logged in users only
    -> Viewing other profile status updates -- All users




## URLs of the Feed API:

### 1. /api/feed/
    -> list all feed items
    -> GET (list feed items)
    -> POST (create feed item for logged in user)

### 2. /api/feed/<feed_item_id>/
    -> manage specific feed items
    -> GET (get the feed item)
    -> PUT/PATCH (update feed item)
    -> DELETE (delete feed item)



--------------------------------------------------------------------------------

admin id -- gauty22@gmail.com
admin password -- 12345
ssh passcode -- 123456
profile password -- password@123

AWS admin ID -- testuser@django.com
AWS password -- 123456
