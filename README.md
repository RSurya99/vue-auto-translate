# Translate HTTP Request
Is an app to translate any language to English created using Vuejs and Axios for http request

## Demo
![Demo gif](public/demo.gif)

## How it works
I'm using Vuejs two-way data binding and watch, so if there is a change on the input text, it will automatically make a request to the API using Axios.

## How to run

### Install all dependencies
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

## How to deploy

### Compiles and minifies project for production
```
npm run build
```
this will generate dist folder for deployment

### deployment
Go to [netlify](https://app.netlify.com/) and create a new project, then upload dist folder to your project.
