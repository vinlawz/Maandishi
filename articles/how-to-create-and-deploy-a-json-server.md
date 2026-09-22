---
title: "How To Create and Deploy a json-server"
datePublished: Tue Oct 18 2022 16:00:14 GMT+0000 (Coordinated Universal Time)
cuid: cl9ee64pf000h09mh2jq71gna
slug: how-to-create-and-deploy-a-json-server
cover: https://cdn.hashnode.com/res/hashnode/image/unsplash/ot5kWZkH97s/upload/v1666103604086/9aL54Mk0o.jpeg
tags: javascript, json, server

---

`json-server` is a tool for creating mock REST API fast! To get started, ensure you have the following requirements:

1. NodeJS (npm)

>Let's get started!

On an empty folder, initiate a nodejs application by running the following on your terminal/CMD:

```shell
npm init -y
```

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1666104260278/mP6C7CN2d.png align="left")

Once that is complete, you install the following packages:

- `json-server`
- `cors`
- `nodemon` (as a dev dependency)

```shell
npm install json-server cors
```

```shell
npm install -D nodemon
```

After the installation, create a new file: `index.js`. This is the entry point for the json-server setup. Add the following inside the file:

```js
const jsonServer = require('json-server')
const cors = require('cors')
const path = require('path')

const server = jsonServer.create()
const router = jsonServer.router(path.join(__dirname, 'db.json'))
const middlewares = jsonServer.defaults()

server.use(cors())
server.use(jsonServer.bodyParser)
server.use(middlewares)
server.use(router)

const PORT = 8000

server.listen(PORT, () => {
  console.log(`JSON Server is running on http://localhost:${PORT}`)
})
```

In the code above, a server has been created that will be fetching and updating data from a json file, `db.json`

In the project root, create a new file: `db.json` and add the following:

```JSON
{
    "feedback": [
        {
            "id": 1,
            "rating": 10,
            "user_name": "Tony Stark",
            "text": "You are the ironman of this world"
        },
        {
            "id": 2,
            "rating": 9,
            "user_name": "Bruce Wayne",
            "text": "You are the batman of this world"
        },
        {
            "id": 3,
            "rating": 8,
            "user_name": "Peter Parker",
            "text": "You are the spiderman of this world"
        }
    ]
}
```

The mock server is ready to run, but let's add some scripts in `package.json`:

Update the `"scripts"` to:

```JSON
  "scripts": {
    "start": "node index.js",
    "dev": "nodemon index.js"
  },
```

To run the server, use either of the scripts:

```shell
npm run start
```

The server runs on port 8000:

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1666106933814/ZcGrHylgC.png align="left")

http://localhost:8000/:

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1666107072195/FDu1-KBvd.png align="left")

The API endpoint is: `http://localhost:8000/feedback`

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1666107202771/xNcnZubfw.png align="left")

The following images show the GET and POST methods:

#### GET

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1666107404425/kQSKiaybw.png align="left")

#### POST

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1666107433130/h11ahTN0d.png align="left")

After POST.ing new data, the `db.json` files update the latest entry.

## Deployment Note

The original article used Cyclic for deployment, but that platform is no longer available for app hosting. If you want to publish the mock server today, push the repository to GitHub and deploy it on a currently supported Node.js platform such as Render, Railway, or Fly.io, then follow that provider's steps for running a `json-server` process.

Once the deployment is complete, your simple mock API will be ready for use.
