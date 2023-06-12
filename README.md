Create a new github repository (if you don’t have one). 
Create a react application (if you don’t have one).
2.1. “npx create-react-app . “ - create react app template (OPTION 1)
2.2. “npm create vite@latest . -- --template react” - vite react app (OPTION 2)
Create a static web server using the express library.
	3.1. “npm i express” - install library
	3.2. Create a new file called “server.js” in the root folder of your app.
3.3. Paste below code into it. Check comments for certain version


import express from "express"; // For Vite app
// const express = require("express"); // For create-react-app


const app = express();


app.use(express.static("dist")); // "build" for create-react-app


app.listen(5000, () => {
  console.log("server serves static files");
});

Push to github.
Deploy using render.
5.1. Go to render and click on the “New +” blue button at the top of the render dashboard webpage. 
5.2. Click on “Web Service” in the pop-up. 
5.3. Connect your github (just once)
5.4. Choose your github repository. 
5.5. Put name for your project (it is just for you)
5.6. Choose “Node” runtime
5.7. Put “npm install && npm run build” as your build command
5.8. Put “node server.js” as your start command.
5.9. Click on “create web service” at the bottom.

Done! ✨
