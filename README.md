![stremio-mixer](/public/logo_readme.png)

---

_[Stremio](https://www.stremio.com/) add-on with live broadcasts from Microsoft's innovative streaming platform, [Mixer](https://mixer.com/)_

---

The add-on is a node.js app written in TypeScript that retrieves stream URLs from Mixer using its REST API and provides them to Stremio. Supports in-memory caching and different levels of logging. Can be configured using environment variables and run in Docker.

> Starting May 21 Mixer [will require](https://aka.ms/MixerDevIdentification) developers to register and pass an API token with each request. This isn't supported in their official node client yet, and, therefore, this add-on. Once it is implemented in the client, the add-on will be updated.


## Installation

```
git clone https://github.com/ax-schneider/stremio-mixer
cd stremio-mixer
npm install
```


## Usage

Set any environment variables before running the app.

Command              | Action
---------------------| -----------------------
`npm start`          | Start the add-on
`docker-compose up`  | Run the add-on in Docker
`npm run build`      | Build the add-on
`npm test`           | Test the add-on


## Environment Variables

Boolean variables are defined as "true"/"false" strings.

Variable                | Default Value     | Description
------------------------| ------------------| ---------------
STREMIO_MIXER_ADDRESS   | http://localhost  | Public address this add-on is going to be accessible on
STREMIO_MIXER_PORT      | 80                | Port to listen to
STREMIO_MIXER_EMAIL     |                   | Contact email
STREMIO_MIXER_CACHE     | true              | Toggle caching
STREMIO_MIXER_ANNOUNCE  | false             | Toggle announcing the add-on to Stremio
STREMIO_MIXER_LOG       | 1                 | 0 to turn logging off, 1 to print errors, 2 to also print requests to Stremio methods, 3 to print all HTTP requests


## License

[ISC](LICENSE)


## Screenshots

![Screenshot](/public/screenshot.jpg)
