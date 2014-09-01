The hackAD NYU Vote server
==========================

The entrypoint for the hackAD NYU Vote server

To Install
==========

```
# Start submodules
git submodule init
git submodule update

# install docker
curl https://raw.githubusercontent.com/lingz/Scripts/master/install/docker.sh | bash

# install fig
curl https://raw.githubusercontent.com/lingz/Scripts/master/install/fig.sh | bash

# Follow setup instructions inside the git submodules
...
```

To Configure
===========

Copy the fig yml file and fill in the environment variables.
You need to specify a Google API ID and Key (for o-auth logins), as well as optionally
a MONGO URI if you want to use an external databse.

```
cp fig.yml.example fig.yml
nano fig.yml
```

To update after sub-projects have changed
==============================

```
git submodule foreach git pull
```

To rebuild after changing files
==============================

```
fig build
```

To start
=======
```
fig up
```
