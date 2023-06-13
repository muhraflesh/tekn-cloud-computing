### Task 1: Run some simple Docker containers
#### Run a single task in an Alpine Linux container
1. Run the following command in your Linux console.
![01](./img/img1.png)
2. Docker keeps a container running as long as the process it started inside the container is still running. In this case the hostname process exits as soon as the output is written. This means the container stops. However, Docker doesn’t delete resources by default, so the container still exists in the Exited state.
List all containers.
![02](./img/img2.png)

#### Run an interactive Ubuntu container
1. Run a Docker container and access its shell.
![03](./img/img3.png)
2. Run the following commands in the container.
![04](./img/img4.png)
![05](./img/img5.png)
![06](./img/img6.png)
3. Type exit to leave the shell session. This will terminate the bash process, causing the container to exit.
![07](./img/img7.png)
4. For fun, let’s check the version of our host VM.
![08](./img/img8.png)

#### Run a background MySQL container
1. Run a new MySQL container with the following command.
![09](./img/img9.png)
2. List the running containers.
![10](./img/img10.png)
3. You can check what’s happening in your containers by using a couple of built-in Docker commands: docker container logs and docker container top.
![11](./img/img11.png)
Let’s look at the processes running inside the container.
![12](./img/img12.png)
4. List the MySQL version using docker container exec.
![13](./img/img13.png)
5. You can also use docker container exec to connect to a new shell process inside an already-running container. Executing the command below will give you an interactive shell (sh) inside your MySQL container.
![14](./img/img14.png)
6. Let’s check the version number by running the same command again, only this time from within the new shell session in the container.
![15](./img/img15.png)
7. Type exit to leave the interactive shell session.
![16](./img/img16.png)

### Task 2: Package and run a custom app using Docker
#### Build a simple website image
1. Make sure you’re in the linux_tweet_app directory.
![17](./img/img17.png)
2. Display the contents of the Dockerfile.
![18](./img/img18.png)
3. Echo the value of the variable back to the terminal to ensure it was stored correctly
![19](./img/img19.png)
4. Use the docker image build command to create a new Docker image using the instructions in the Dockerfile.
![20](./img/img20.png)
5. Use the docker container run command to start a new container from the image you created.
![21](./img/img21.png)
7. result
![22](./img/hasil.png)
6. Once you've accessed your website, shut it down and remove it.
![23](./img/img22.png)

### Task 3: Modify a running website
1. Let's start the web app and mount the current directory into the container.

![24](./img/task3-1.png)

2. Go to the running website and refresh the page. Notice that the site has changed.

![25](./img/task3-2.png)

3. Copy a new index.html into the container.

![26](./img/task3-3.png)

4. website

![27](./img/task3-4.png)

5. stop and rerun without bind

![28](./img/task3-5.png)

6. build new image

![29](./img/task3-6.png)

7. docker image ls

![30](./img/task3-7.png)

8. rerun new container

![31](./img/task3-9.png)

9. running 2 container

![32](./img/task3-10.png)

10. website

![33](./img/task3-12.png)
