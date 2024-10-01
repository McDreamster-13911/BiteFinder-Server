# FoodFire Server

A BiteFinder Server (Node.js web server) that fetches data from a third-party (Swiggy) API (Fix the CORS Issue) and exposes it to a client (https://bitefinder.netlify.app/) App.


## Clone this Repository

You need to write the following commands on the terminal screen(in vscode) so that you can run this project locally.

```bash
  git clone "https://github.com/McDreamster-13911/BiteFinder-Server.git"
```

Go to the project directory

```bash
  cd BiteFinder-Server
```

Install dependencies

```bash
  npm install
```

Start the server

```bash
  npm run start
```

This application should now be running on `localhost`. If you want to Fork repository and want to run locally, follow this guidelines [Fork and Clone Github Repository](https://docs.github.com/en/get-started/quickstart/fork-a-repo)

Test the BiteFinder Server Locally in your React App then use this domain name (`http://localhost:3000/`) if the Server is running on a `3000` Port:
```javascript
const response =  await fetch(`http://localhost:3000/api/restaurants?lat=12.9351929&lng=77.62448069999999&page_type=DESKTOP_WEB_LISTING`)

const data = await response.json();
```


## Deploy the server
Once you have tested the BiteFinder server locally, you can deploy it to a production environment by following these steps.

1. Create an account on [Render](https://render.com/) if you haven't already.
2. Click on the `New +` button and select `Web Service` from the dropdown menu.
3. `Connect` to your own GitHub repository (node server that you have created your own) which you want to deploy.
4. In the `Settings` tab, scroll down to the `Environment Variables` section and add `PORT` environment variables to `3000`.
5. Wait for the deployment to finish. Once it's done, you should see a success message and a link to our server URL. For Instance: `http://YourOwnServerName.onrender.com`
6. Click on the link URL to test our server.

Note: Now that our server is deployed on [Render](https://render.com/) you can change the API URL in react app to the domain in which the server is deployed. For instance: if your server is hosted in `http://YourOwnServerName.onrender.com`, in the react app while sending a request to API, use this domain name : 

```javascript
const response =  await fetch(`http://YourOwnServerName.onrender.com/api/restaurants?lat=12.9351929&lng=77.62448069999999&page_type=DESKTOP_WEB_LISTING`)
```

