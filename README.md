The hackAD NYU Vote server
==========================

The entrypoint for the hackAD NYU Vote server

### To Install:

```
# Start submodules
git submodule init
git submodule update

# Follow setup instructions inside the git submodules
...

# install docker
curl https://raw.githubusercontent.com/lingz/Scripts/master/install/docker.sh | bash

# install fig
curl https://raw.githubusercontent.com/lingz/Scripts/master/install/fig.sh | bash

```

### To rebuild after changing files:


```
fig build
```

### To start:
```
fig up
```
