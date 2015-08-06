Disclaimer: This documentation is a WIP.
What is Evercam?
TODO:

Developer Guide
---------------

Setting up Evercam locally for development
------------------------------------------
Evercam is tested to work under either Ubuntu 14.04 and Mac OSX 10.10. It should also work under most linux distro out there but we haven't tested them.

* System Requirements [*]
  - Ubuntu 14.04 or Mac OSX 10.10
  - Ruby 2.2.2
  - Elixir 1.04
  - Erlang 17.05
  - Redis 2.8
  - Memcached 1.4
  - Postgres 9.4
  [*] - This guide is written for developers assuming that all of the Evercam components (see below) are running from a single machine. However, this may not the case when you use docker or VMs to run individual components on a separate containers. In those cases, you should install the system requirements for the running components in those containers.


For the impatient
-----------------
If you are impatient and want to run Evercam locally without into much details, make sure you all the above dependencies installed on your computer and run the following command:

```
wget -qO- https://raw.githubusercontent.com/evercam/evercam-devops/master/setup_evercam | sh
```

The above command will clone multiple git repos into `evercam-devops` directory. The script will take sometime to download the repos and to download the dependencies.

Once done, use the following command to run Evercam locally.

```
foreman start
```

Visit http://localhost:3000

There are two user accounts available for you to test:
username: admin
password: admin

username: user
password: user


Installing the system requirements
---------------------------------
TODO: link to good resources on the internet for installing the dependecies. Do not spend time writing something that's already available elsewhere.


Components of Evercam
---------------------
  - evercam-dashboard
  - evercam-api
  - evercam-media

Evercam Dashboard (evercam-dashboard)
-------------------------------------
TODO:

Evercam API (evercam-api)
-------------------------
TODO:

Evercam Media (evercam-media)
-----------------------------
TODO:
