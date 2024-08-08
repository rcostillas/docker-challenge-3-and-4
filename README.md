Romeo Costillas

Challenge 3

• The initial step was to clone the provided repository and make it private.

• First, we need to set up the database by creating a .env file with the necessary details such as the database name, user, password, and host. I used HeidiSQL for this project to display and process the data, following the instructions provided in the project documentation.

• Using the provided init.sql file, I created a new schema in the database to set up a table called books. Simply run the code provided in the init.sql file.

• Using the terminal, I navigated to the challenge3 folder and executed “npm install” to install all necessary dependencies. Additionally, I ran “npm install dotenv” to manage environment variables securely, ensuring proper configuration for the project.

• To start the server, I ran node .\server.js, which initialized the application and allowed me to confirm that the server was set up and functioning as expected.

• The screenshot provided demonstrates that everything is configured properly. To verify that the setup is functioning correctly, we need to test the connection to localhost > api > books. This ensures that the server is correctly interfacing with the API endpoint and operating as expected.

• The docker-compose.yml file was created to define and configure the services required for the project. This file outlines the necessary Docker containers, including their images, networks, and volumes, to ensure a consistent and reproducible development and deployment environment. By specifying these components, the docker-compose.yml streamlines the setup process and enhances the efficiency of managing the project’s infrastructure.

• I ran docker-compose up in the main Docker folder to ensure that all specified services and containers were properly initialized and running. This command, executed in the terminal, started the containers as defined in the docker-compose.yml file, allowing for verification that the environment was correctly set up and all dependencies were functioning as expected.

• Next, proceed to Docker Desktop to manage and run the images and containers.

• To confirm that everything is functioning correctly, we can open a browser and check if the records are being displayed as expected.

Challenge 4
• To verify the functionality of the application, we need to make a GET request to the appropriate endpoint using a browser or REST client. For instance, using the URL http://localhost:8080/api/stats, where 8080 is the port number on which the application is running and api/stats is the specific route to test. This request should return the expected data or response, confirming that the server is handling requests correctly and the application is functioning as intended.

• Run the command docker-compose up --scale node-service=3 -d to start the Docker containers with the node-service scaled to three instances, operating in the background. This setup ensures that multiple instances of the node-service are running simultaneously, which can improve load handling and redundancy while allowing the terminal to remain free for other tasks.

• Returning to Docker Desktop, you can verify that there are three instances of the container running. This confirmation ensures that the node-service has been successfully scaled to the specified number of instances.

• The response contains a unique hostname value each time a GET request is made to the endpoint. This behavior indicates that the requests are being routed to different instances of the node-service container, reflecting the scaling of the service. Each instance provides a distinct hostname, demonstrating that the load is distributed across multiple containers and confirming that the scaling configuration is functioning as intended.

• Execute the command docker-compose ps to list the running containers and their current status. This command provides a summary of the containers defined in the docker-compose.yml file, including details such as container IDs, service names, and their respective states, which helps in verifying that all services are running as expected.

Resources
https://www.youtube.com/watch?v=1je3VxDF67o
https://docs.docker.com/compose/environment-variables/
https://docs.docker.com/reference/cli/docker/compose/up/
https://www.appsdeveloperblog.com/scaling-with-docker-compose-a-beginners-guide/
https://hub.docker.com/_/mariadb
