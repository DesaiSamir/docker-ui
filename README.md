# Docker UI

Docker UI is a web app for viewing and managing Docker images, containers, volumes, etc in a web browser.

This project is also meant to serve as a working example of how to build a web app using the following tech stack:

- NodeJS
- ExpressJS
- ReactJS
- FuseBox

## Usage

### Production (Docker)

Pull the image

```bash
docker pull otothea/docker-ui
```

Run it

```bash
docker run -d -p 9898:9898 -v /var/run/docker.sock:/var/run/docker.sock --name docker-ui otothea/docker-ui
```

### Production (Node)

Clone the repository

```bash
git clone https://github.com/otothea/docker-ui.git
```

Change to the repository directory

```bash
cd docker-ui
```

Install the production dependencies

```bash
npm install --prod
```

Copy the config (and adjust as needed in a text editor)

```bash
cp config.example.js config.js
```

Start the server

```bash
npm run prod
```

### Development

Clone the repository

```bash
git clone https://github.com/otothea/docker-ui.git
```

Change to the repository directory

```bash
cd docker-ui
```

Install the dependencies 

```bash
npm install
```

Copy the config (and adjust as needed in a text editor)

```bash
cp config.example.js config.js
```

Start the client

```bash
npm run watch
```

Start the server

```bash
npm start
```

## Environment Variables

DOCKER_UI_HOST     - override config.host (the hostname that the API listens on)
DOCKER_UI_PORT     - override config.port (the port the API listens on)
DOCKER_UI_DEBUGGER - override config.debugger (the port the debugger runs on)

## Testing

There are currently no tests.

## Contributing

Pull requests are welcome.