This assignment has a *Backend code* in nodejs, a *Frontend code* in React and it stores data in a *Database with MongoDB*

*Tasks to do*

1. Rund MongoDB container with the following run command
- *docker run -d -p 27017:27017 --name mongodb --rm mongo*
- Don't bother about environment variables because the connection has been made in the application already

2. Install depencies(node_modules) needed by the backend 
- Change directory to backend folder
- Run this command *npm install*
- After installing the node_mudules, start the server with *node app.js*
- It will get connected to mongoDB automatically

3. Install depencies(node_modules) needed by the frontend
- Change directory to frontend folder
- Run this command *npm install*
- After installing the node_mudules, start the frontend React app with *npm start*
- The app will automatically run in your browser on port 3000
- Add a goal and refresh the page, the you will notice that data is persisting

4. Docker-compose
- Shut down mongodb and delete the image
- Terminate the frontend and the backend from running
- Build a *docker-compose* file for this setup so as to ease the deployment of the application, then run the docker-compose file and make sure the application runs as intended.