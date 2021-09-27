# Create a Dockerfile

Recall that to start working on this project, you had to install a fair amount of software.

Chances are that you ran into some difficulty along the way and had to troubleshoot those problems before completing the first todo item.

How long did it take you to overcome those problems? An hour, three, or perhaps a day?

That's a lot of time to spend chasing hunches on the Web, and generally doing things that take time away from your real goal, i.e. completing todo items and being able to run the app to verify the results. Programmers are expensive resources, so it's important that they are efficient and productive.

There are many tools that can help programmers set up their projects more quickly, and Docker is one of them.

You will need to have [docker installed](https://docs.docker.com/engine/install/) and running in the background to complete this todo item.

After completing the docker installation steps for your operating system, you can check that docker is indeed installed and running using the following commands.

View the version of docker you just installed
```
docker --version
```

You should see something like this, but don't expect it to be exact.
```
Docker version 20.10.6, build 370c289
```

Try running the test container called hello-world.
```
docker run hello-world
```

You should see something like this, but don't expect it to be exact.
```
Unable to find image 'hello-world:latest' locally
latest: Pulling from library/hello-world
2db29710123e: Pull complete
Digest: sha256:393b81f0ea5a98a7335d7ad44be96fe76ca8eb2eaa76950eb8c989ebf2b78ec0
Status: Downloaded newer image for hello-world:latest

Hello from Docker!
This message shows that your installation appears to be working correctly.

To generate this message, Docker took the following steps:
 1. The Docker client contacted the Docker daemon.
 2. The Docker daemon pulled the "hello-world" image from the Docker Hub.
    (amd64)
 3. The Docker daemon created a new container from that image which runs the
    executable that produces the output you are currently reading.
 4. The Docker daemon streamed that output to the Docker client, which sent it
    to your terminal.

To try something more ambitious, you can run an Ubuntu container with:
 $ docker run -it ubuntu bash

Share images, automate workflows, and more with a free Docker ID:
 https://hub.docker.com/

For more examples and ideas, visit:
 https://docs.docker.com/get-started/
```
