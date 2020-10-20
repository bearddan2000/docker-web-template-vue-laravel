# docker-web-template-vue-laravel

## Description
A customized vuejs frontend and laravel backend.

## Tech stack
- laravel
- vuejs
  - axios
  - babel
  - router

## Docker stack
- docker
- docker-compose
- php:fpm-alpine
- nginx:alpine
- current-node:alpine

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
