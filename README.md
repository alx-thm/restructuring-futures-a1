# ReStructuring Futures (RSF) 

A public notebook for Restructuring Futures, an experimental collaboration between Hypha Worker Co-op, [UKAI Projects](https://www.ukai.ca/) and the [Laboratory for Artistic Intelligence](https://artisticintelligence.com/) supported by a grant from the [2020-2021 Digital Strategies Fund](https://canadacouncil.ca/funding/strategic-funds/digital-strategy-fund) at Canada Council for the Arts. 

"Restructuring Futures is ostensibly about building infrastructure to support creative and cultural collaboration that is resilient to volatile conditions." More on the latest phase of the project [here](https://localdisturbances.substack.com/p/the-arts-has-a-fever?r=f3tud). 

The prototype from Phase 1 [lives here](https://github.com/hyphacoop/crispy-couscous).

### Running the app locally

If you want to run the [svelte app](https://github.com/hyphacoop/restructuring-futures/tree/main/svelte-app) locally, you can run the following commands in your terminal after downloading [node](https://nodejs.org/en/) and cloning this github repository.

1. download [Node.js](https://nodejs.org/en)
2. clone this [repository](https://github.com/hyphacoop/restructuring-futures)
3. run the following commands:

```
cd svelte-app
npm install
npm run dev
```

### Hosting a server

The [server folder](https://github.com/hyphacoop/restructuring-futures/tree/main/server) contains instructions on how to run an earthstar server in order to host the shared database.

### Pointing the web app to the server

The server address can be manually added by users through the UI by clicking the top right button and then selecting the *Show Server Settings* button. Users can then input the server's ip address in the text input field.

Alternatively, an admin can input the server address in the .env file in the svelte-app folder. You simply need to copy and rename the .env.example file found in the svelte-app folder and insert the server's address.

### Deploying the application

With gh-pages, it is possible to quickly build and deploy with the following commands:
```
npm run build
npm run deploy
```

## Building with Earthstar

We use github pages to host prototypes found in the [web folder](https://hyphacoop.github.io/restructuring-futures/web/).
The active prototype can be found at [hyphacoop.github.io/restructuring-futures](https://hyphacoop.github.io/restructuring-futures/)

## Code of Conduct

This project has a [Code of Conduct](https://docs.google.com/document/d/1KlvsinjNGPpF25aKxWJpG8jv8aHk7uLguIbmciX16xo/edit?usp=sharing). The Restructuring Futures project team is dedicated to providing a harassment-free environment for everyone, regardless of gender, gender identity and expression, sexual orientation, disability, physical appearance, body size, race, age, religion or technical skill level.

In order to try and remove obstacles to participation, we have adopted an explicitly-documented code to communicate our expectations for conduct within the community. We expect all people engaging with the project to have read the code. If you have any questions please email [project.rsfutures@hypha.coop](mailto:project.rsfutures@hypha.coop) or to report a violation please email Udit directly: [udit@hypha.coop](mailto:udit@hypha.coop).


## Curious? Want to know more?

You can email [project.rsfutures@hypha.coop](mailto:project.rsfutures@hypha.coop) to get ahold of all of us at Hypha!

## License

<span xmlns:dct="http://purl.org/dc/terms/" property="dct:title">Restructuring Futures Public Notebook</span> content is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License</a>, the text of which is included in the repository [here](https://github.com/hyphacoop/restructuring-futures/blob/main/LICENSE).

All code at <a xmlns:cc="http://creativecommons.org/ns#" href="https://github.com/hyphacoop/restructuring-futures/" property="cc:attributionName" rel="cc:attributionURL">github.com/hyphacoop/restructuring-futures/</a> is licensed under a <a rel="license" href="https://www.gnu.org/licenses/gpl.html">GNU General Public License v3.0</a>.
