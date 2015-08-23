The hackAD NYU Vote server
==========================

The entrypoint for the hackAD NYU Vote server

NYU Vote Code
=============

The repo for the actual NYU Vote code can be found here:
https://github.com/hackAD/nyu-vote

NYU Vote User Documentation
===========================

The NYU Vote users documentation can be found here:
https://docs.google.com/document/d/18qsoORoz7B6R_f45JJMU8bvnA1ux5EhjHrnW2LpV8sQ/edit?usp=sharing

## To Install

#### Start submodules

```
git submodule init
git submodule update
```

#### Install Docker and Fig

```
curl curl -sSL https://get.docker.com/ | sh
curl https://raw.githubusercontent.com/lingz/Scripts/master/install/fig.sh | bash
```

#### Follow setup instructions inside the git submodules

See submodule repos

## To Configure

First you need to make sure the reverse proxy is correctly configured. Checkout the README at this link for instructions:

[docker-nyu-vote-nginx](https://github.com/hackAD/docker-nyu-vote-nginx)

You also need a Google Apps token. Be sure your redirect URLs are correctly set. Here is an example:

![Example](http://i.imgur.com/jagLdyG.png)

Copy the fig yml file and fill in the environment variables.
You need to specify a Google API ID and Key (for o-auth logins), as well as optionally
a MONGO URI if you want to use an external databse.

```
cp fig.yml.example fig.yml
nano fig.yml
```

## To update after sub-projects have changed

```
git submodule foreach git pull
```

## To rebuild after changing files

```
fig build
```

##To start

```
fig up
```
