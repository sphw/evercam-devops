## Evercam Development Environment Setup

#### Install Host dependencies

* [Virtualbox](https://www.virtualbox.org/wiki/Downloads)
* [Vagrant](http://www.vagrantup.com/downloads.html)
* [Git](http://git-scm.com/downloads)

#### Clone this repository and it's submodules

```
git clone https://github.com/evercam/evercam-devops.git && cd evercam-devops
git pull && git submodule init && git submodule update && git submodule status
git submodule foreach --recursive git checkout master
git submodule foreach --recursive git pull
```

#### Copy example `.env` file into required directories

```
cp .env evercam-api/
cp .env evercam-dashboard/
cp .env evercam-models/
```

#### Run Vagrant and ssh into the VM

```
vagrant up && vagrant ssh
```

Grab a cup of your favorite beverage, this is going to take some time...

#### Type the password in console 

```
vagrant
```

#### Test that everything is working

```
cd /vagrant/evercam-api
bundle install
bundle exec rspec
cd /vagrant/evercam-dashboard
bundle install
bundle exec rspec --pattern 'c*/*_spec.rb,h*/*_spec.rb'
```

#### You're done!

Now start the API server:

```
cd /vagrant/evercam-api
bundle exec rackup
```

And in another terminal tab/window start the Dashboard server:

```
cd /vagrant/evercam-dashboard
EVERCAM_LOCAL=true bundle exec rails server -b 0.0.0.0
```

Open [http://localhost:3000/](http://localhost:3000/) in a browser and you'll see the dashboard of the Next Big Thing&trade;
