

## Quick Start in [Docker](https://www.docker.com/)

> Get the code

```bash
$ cd react-berry-dashboard
```

> Start the app in Docker

```bash
$ docker-compose pull  # download dependencies 
$ docker-compose build # local set up
$ docker-compose up    # start the app 
```

The React UI starts on port `3000` and expects an API server on port `5000` (saved in configuration).

<br />

![React Nodejs Berry - Open-source full-stack seed project crafted by CodedThemes and AppSeed.](https://github.com/senior-developer1019/admin-dashboard-react/blob/master/public/screenshot.gif)


## How to use it

To use the product Node JS (>= 12.x) is required and GIT to clone/download the project from the public repository.

**Step 1** - Clone the project

```bash
$ git clone https://github.com/senior-developer1019/admin-dashboard-react.git
$ cd admin-dashboard-react
```

<br >

**Step 2** - Install dependencies via NPM or yarn

```bash
$ npm i
// OR
$ yarn
```

<br />

**Step 3** - Start in development mode

```bash
$ npm run start 
// OR
$ yarn start
```

<br />

## Configure the backend server

The product comes with a usable JWT Authentication flow that provides only the basic requests: login/logout/register. 

**API Server URL** - `src/config/constant.js` 

```javascript
const config = {
    ...
    API_SERVER: 'http://localhost:5000/api/'  // <-- The magic line
};
```

<br />

**API Server Descriptor** - POSTMAN Collection

The API Server signature is provided by the [Unified API Definition](https://docs.appseed.us/boilerplate-code/api-unified-definition)


<br />

## Node JS API Server

The product is also open-source and is already configured to work with Berry Dashboard Template - product features:

- Typescript / `NodeJS` / `Express` Server
- JWT authentication (`passport-jwt` strategy)
- Persistence: `SQLite` / `TypeORM`

<br />

### Compile the API Server

**Step 1** - Clone the project

```bash
$ cd api-server-nodejs
```

**Step #2** - Install dependencies via NPM or Yarn

```bash
$ npm i
// OR
$ yarn
```

**Step 3** - Run the SQLite migration via TypeORM

```
$ npm run typeorm migration:run
// OR 
$ yarn typeorm migration:run
```

**Step 4** - Start the API server (development mode)

```bash
$ npm run dev
// OR
$ yarn dev
```

The API server will start using the `PORT` specified in `.env` file (default 5000).
