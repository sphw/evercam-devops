## Evercam Development Environment Setup

#### Install Host dependencies 

* [Virtualbox](https://www.virtualbox.org/wiki/Downloads)
* [Vagrant](http://www.vagrantup.com/downloads.html)
* [Python](https://www.python.org/downloads/)
* [Git](http://git-scm.com/downloads)

#### Clone this repository and it's submodules

```
git clone git@github.com:evercam/devops.git && cd devops
git pull && git submodule init && git submodule update && git submodule status
git submodule foreach --recursive git checkout master
```

#### Install Ansible dependencies

```
sudo pip install ansible
sudo ansible-galaxy install -r ansible/requirements.yml --force
```

#### Create a `private_vars_devops.yml` file and fill it in with your information

```
heroku_login: "heroku_login"
heroku_apikey: "heroku_apikey"
aws_access_key: "aws_access_key"
aws_secret_key: "aws_secret_key"
```

#### Run Vagrant

```
vagrant up
```

Grap a cup of your favorite beverage, this is going to take some time...

If you encounter any errors run `vagrant provision`, which will continue provisioning process.

#### Start Dashboard server

```
vagrant ssh

cd /vagrant/evercam_dashboard
bundle exec rails s -b 0.0.0.0
```

You're done!

Open [http://localhost:3000/](http://localhost:3000/) in a browser and you'll see the dashboard of the Next Big Thing&trade;
