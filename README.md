# iotapp-hello-world-tutorial

## Install Dependencies
```
npm install
```

## Project Setup
In the ```HelloWorld.vue``` file (around line 39), pass your channel API keys as arguments to the API functions.

#### Examples
```javascript
    iotapp.getPrivateChain("myOz8FZXhT4lBzJplmXtUbneP8eeXpSp","3imNnMduakmu6JmFafIxnu8WJj28BjQI")

    iotapp.getLatestTx("myOz8FZXhT4lBzJplmXtUbneP8eeXpSp","3imNnMduakmu6JmFafIxnu8WJj28BjQI")
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
