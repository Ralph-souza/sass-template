# Sass Project Starter Template

This is a basic Sass template to help starting new projects production.

## About NodeJS version

In order to run Sass we have to install or update NodeJS an NPM (Node Packages Manager) to do that we run the following commands:
OBS: Some might need some updated information which can be found in:</br></br>
&nbsp;[NodeJS Documentation](https://nodejs.org/en)</br>
&nbsp;[NPM (Node Packages Manager)](https://www.npmjs.com/)</br></br>

## Check NodeJS & NPM version

Since we have to install NodeJS and NPM it be a good thing to check if we doesn`t already have them install, we can do that with the following command:

> $ node --version

> $ npm --version

### OBS: By the time i wrote this tutorial i was using **node v18.15.0** and **npm 9.5.0**

## Install or update NodeJS & NPM

> $ sudo npm cache clean -f

> $ sudo npm install -g n

> $ sudo n stable

> $ sudo n latest

**TO FIX PATH**

> $ sudo n rm **version**

> $ sudo npm install -g n

## Steps taken to install Node-Sass

First of all we will create a **package.json** file by running the following command:

> $ sudo npm init -y

Then run:

> $ sudo npm install node-sass

Once it is installed it will be showed in the **package.json** file.

## Create a NPM Script

In order to run node-sass we are going to create a NPM script to run it while we work on our project.
We do that by removing the line containing the **test** and add the following script into **package.json** file:

```
"scripts": {
    "sass": "node-sass -w scss/ -o dist/css/ --recursive"
}
```

## Create Project Folders

Now we create two folders into projects root:
### OBS: **DO NOT** create manually a **/css** folder, it will be created further on automatically

```
dist
    |
    img
    index.html
scss
    |
    main.scss    
```

## Run Node-Sass

To run **node-sass** we will use our npm script created earlier by running the following command:

> $ npm run sass

Once it is running lets apply the following configuration to **main.scss** file so it can create our **/css** folder.

```
* {
    box-sizing: border-box;
    padding: 0;
    margin: 0;
}
```

Once we save the file it will create a **/css** folder inside dist.
Now we can start our project design.