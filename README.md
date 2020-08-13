# docker-vue-laravel

## Description
A customized vuejs frontend and laravel backend.

## Project technologies
- docker
- docker-compose
- laravel
- vuejs
  - axios
  - babel
  - router

## Prerequisites
- docker installed
- docker-compose installed
- any server/service using port 80 be disabled

## To run
Be sure when running this command, you are in the folder
with docker-compose.yml file.

```docker-compose up -d --build```

Go to http://localhost

## Web
A simple nginx server configured to proxy to the seperate services frontend and backend. Hot reloads have been enabled for frontend service.

## Frontend
You will need to add a vue.config.js file to the same folder as package.json.
In this file add the following:

> // vue.config.js
>
> module.exports = {
>    devServer: {
>        disableHostCheck: true
>    }
> }

## Backend
This uses laravel so we can use ajax calls to access controllers
So for example we can, in the frontend, call the classic HelloWorld controller in the following call:
```$.ajax.get(localhost + "api/HelloWorld", () => {...});```
