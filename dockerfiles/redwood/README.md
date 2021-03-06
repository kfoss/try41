To get the environment for Redwood on top of Docker you can either Pull it from the public docker index, or you can build it from source.

Pull from Docker index:
=======================
```
sudo docker pull lab41/redwood

sudo docker tag lab41/redwood redwood
```

Build from source:
==================
```
git clone https://github.com/Lab41/try41.git

cd try41/dockerfiles/redwood

sudo docker build -t redwood .
```

Once the image has been built you can either run it as a contained webapp as it's used in Try41, or you can run in a shell.

Run as a webapp:
================
```
sudo docker run -d -P redwood
```

Run in a shell:
===============
```
sudo docker run -i -t -P redwood /bin/bash
```

NOTE: when running in a shell, you can also execute /src/startup.sh and access the webapp from the exposed port

Find port that was exposed:
===========================
```
sudo docker ps
```
