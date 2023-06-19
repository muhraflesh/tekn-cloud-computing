### Section #1 - Networking Basics
#### Step 1: The Docker Network Command
![01](img/img1.png)
#### Step 2: List networks
![02](img/img2.png)
#### Step 3: Inspect a network
![03](img/img3.png)
#### Step 4: List network driver plugins
![04](img/img4.png)

### Section #2 - Bridge Networking
#### Step 1: The Basics
1. Every clean installation of Docker comes with a pre-built network called bridge. Verify this with the docker network ls.
![05](img/img5.png)
2. Install the brctl command and use it to list the Linux bridges
![06](img/img6.png)
3. Then, list the bridges on your Docker host
![07](img/img7.png)
4. You can also use the ip a command to view details
![08](img/img8.png)

#### Step 2: Connect a container
1. Create a new container
![09](img/img9.png)
2. Verify our example container is up
![10](img/img10.png)
3. Run the brctl show
![11](img/img11.png)
4. Inspect the bridge network
![12](img/img12.png)

#### Step 3: Test network connectivity
1. Ping the IP address of the container from the shell prompt of your Docker host
![13](img/img13.png)
2. Run docker ps to get ID container
![14](img/img14.png)
3. Run a shell inside that ubuntu container, by running docker exec -it CONTAINER_ID /bin/bash.
![15](img/img15.png)
4. Run apt-get update && apt-get install -y iputils-ping
![16](img/img16.png)
5. Ping www.github.com
![17](img/img17.png)
6. Disconnect our shell from the container
![18](img/img18.png)
7. Stop this container so we clean things up from this test, by running docker stop CONTAINER_ID.
![19](img/img19.png)

#### Step 4: Configure NAT for external connectivity
1. Start a new container based off the official NGINX image
![20](img/img20.png)
2. Review the container status and port mappings
![21](img/img21.png)
3. Connect from your Docker host
![22](img/img22.png)

### Task 3: Modify a running website
#### Step 1: The Basics
#### Step 2: Create an overlay network
#### Step 3: Create a service
#### Step 4: Test the network
#### Step 5: Test service discovery

### Cleaning Up