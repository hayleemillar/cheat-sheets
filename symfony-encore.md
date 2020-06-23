# Symfony Encore Cheat Sheet
A "Cheat Sheet" of commands for Symfony &amp; Encore.

### Documentation
__Symfony__: https://symfony.com/doc/current/index.html
__Encore__: https://symfony.com/doc/current/frontend.html#encore-documentation

### Starting Symfony Web Application _locally_
```
# start symfony web app
symfony server:start
```


### Building Encore Assets
```
# build all at once
yarn encore dev
```
```
# recompile automatically when a file changes
yarn encore dev --watch
```
```
#deploy, production build
yarn encore production
```
Stop and restart Encore each time (using an above cmd) you update your webpack.config.js file.
