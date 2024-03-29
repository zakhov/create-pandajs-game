# create-pandajs-game
Startup template for building games with PandaJS

#### Glossary
1. [About](#about-panda2--pandajs)
2. [Why](#why)
3. [Setup](#setup)
4. [Tools](#tools)
5. [Workflows](#workflows)
6. [Deployment](#deployment)
6. [Vercel](#deploying-to-vercel)


#### About Panda2 / PandaJS

- [Panda2.io](https://www.panda2.io/) is a HTML5 game development platform made by [Eemeli Kelokorpi](https://github.com/ekelokorpi). It's based on Goodboy's PixiJS renderer v2 and while it is the less popular compared to its contemporaries, it offers a relatively simpler learning curve. Also, the documentation provided is easy enough for anyone to pickup / learn the basics of game development and start building their games in no time.
- While Panda2 provides a powerful editor and bundling / deployment to multi-platforms, the engine itself is open source and can be updated using the `panda-toolkit` library.

**Update: Panda2 is no longer maintained and their website is down but the most recent engine release still works well enough for production use cases.**

*Resources*

- Engine Documentation: https://www.panda2.io/docs/api
- Playground Examples: https://www.panda2.io/examples
- Repository for engine: https://github.com/ekelokorpi/panda-engine


#### Why?

- Although Panda2.io offers a powerful editor with features like bundling apps into different platforms, and easy assets & plugin management, my main use of the engine is mainly for creating web applications. Needless to say, in my personal development environment I prefer to use my own editors, with several base configurations such as (prettier/eslint). 
- This project is mainly aimed to help those who wish to quickly develop web based games using Panda2 engine and build / deploy them to production and also have a sample configuration that helps maintain their code readability and maintainability.


#### Setup

1. Install the dependencies of the project:

`npm run i`

2. Create a panda2 project with the latest `dev` version of the engine:

`npm run init`


#### Tools

1. Updates the game engine to latest version according to https://github.com/ekelokorpi/panda-engine :

`npm run update-engine`


#### Workflows

1. Serves the development build of the game locally, watches for any file changes in the game project folder:

`npm run dev`

2. Serves a production build of the game locally:

`npm run serve`

3. Creates a production build of the game and bundles it into the `public` folder:

`npm run build`




#### Deployment

##### Deploying to custom server

Perform an `npm run build` command and the **production** build of the game should be available for deployment in the **public** folder.
Be sure to setup the project with the game engine via `npm run init` or else the **build** command will fail.
##### Deploying to Vercel

All you have to do is link the project's repository to your account.
Setting the build process `npm run build` and `public` as the output directory would do the trick.

Vercel deployment link connected with this repository can be found below: 

https://create-pandajs-game.vercel.app

*Do note that since the repository is merely a template and doesn't include the Panda2 engine by default, the build script is using `npm run build:ci` as it includes the `npm run init` command necessary to setup the Panda2 engine source files needed to complete the **build**  process.

*If you have ran the initial setup via `npm run init` and pushed the `game` folder to your repository, just simply doing `npm run build` should work fine.

