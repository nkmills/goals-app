### The Project MERN Stack

This Repo has a Backend code in Node.js, a Frontend code in React, and it stores data in a Database with MongoDB.

#### Tasks to do

1. **Run MongoDB container:**
   - Use the following command to start a MongoDB container:
     ```
     docker run -d -p 27017:27017 --name mongodb --rm mongo
     ```
   - This command will:
     - Run a MongoDB container in detached mode (`-d`).
     - Map port 27017 of your host to port 27017 of the container (`-p 27017:27017`).
     - Name the container `mongodb` (`--name mongodb`).
     - Automatically remove the container when it stops (`--rm`).

   - Don't worry about setting environment variables because the application is pre-configured to connect to MongoDB.

2. **Install backend dependencies:**
   - Change directory to the backend folder:
     ```
     cd backend
     ```
   - Install the necessary dependencies by running:
     ```
     npm install
     ```
   - This command will install all the packages listed in the `package.json` file.

   - After installing the dependencies, start the backend server with:
     ```
     node app.js
     ```
   - The server will automatically connect to MongoDB.

3. **Install frontend dependencies:**
   - Change directory to the frontend folder:
     ```
     cd ../frontend
     ```
   - Install the necessary dependencies by running:
     ```
     npm install
     ```
   - This command will install all the packages listed in the `package.json` file.

   - After installing the dependencies, start the React frontend app with:
     ```
     npm start
     ```
   - The app will automatically open in your default web browser on port 3000.

4. **Add and verify data persistence:**
   - Add a goal through the frontend application.
   - Refresh the page to verify that the data persists in MongoDB.

## Docker-compose

1. **Shut down MongoDB and delete the image:**
   - Stop the running MongoDB container:
     ```
     docker stop mongodb
     ```
   - Remove the MongoDB container:
     ```
     docker rm mongodb
     ```

2. **Terminate the frontend and backend:**
   - Stop the backend server by pressing `Ctrl+C` in the terminal where it's running.
   - Stop the frontend app by pressing `Ctrl+C` in the terminal where it's running.

3. **Build a Docker Compose file:**
   - Create a `docker-compose.yml` file to define and run multi-container Docker applications.
   - Ensure that it includes services for both the backend and frontend applications, and MongoDB.

4. **Run Docker Compose:**
   - Use the following command to start all services defined in the `docker-compose.yml` file:
     ```
     docker-compose up
     ```
   - Ensure that the entire application runs as intended with all components connected and working together.

### Hints:
- Make sure Docker and Docker Compose are installed on your system.
- Use `docker-compose down` to stop and remove all the containers if you need to start fresh.
- Check the logs with `docker-compose logs` if something goes wrong to troubleshoot issues.
