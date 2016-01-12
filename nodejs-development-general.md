> During the past months, I spent quite some time reading about and developing 
> with [node.js](https://nodejs.org).
> Following, I'll share some of the resources that helped me understanding
> concepts and increasing productivity.

# Setup IDE and plugins
I'm using [Sublime Text 3](http://www.sublimetext.com/3) as editor, along with a list of 
plugins that help keeping my code clean. Find a full list incl. 
configuration [shared here](https://github.com/benkroeger/setup-sublime)

# Node.js Styleguide
After evaluating a couple of great styleguides,
I sticked with the one from [Airbnb styleguide](https://github.com/airbnb/javascript).
There is a [shared](https://www.npmjs.com/package/eslint-config-airbnb) [eslint](http://eslint.org/) 
config for this styleguide (well maintained), that I like to use with the following small
extensions in my projects:

```js
{
  "extends": "airbnb/base",
  "rules": {
    "callback-return": [2, ["callback", "next"]],
    "handle-callback-err": [2, "^.*(e|E)rr" ],
    "max-len": [1, 120, 2, {"ignoreComments": true}],
    "no-unused-vars": [1, {"vars": "all", "args": "none"}]
  }
}
```

Since I don't use [react](https://facebook.github.io/react/) I only extend the `airbnb/base` config.

# Developing node modules
In order to stay consistent with how I structure my node.js modules, 
I'm using [yeoman](http://yeoman.io/) to scaffold my projects. 
My generator of choice [generator-node](https://github.com/yeoman/generator-node) comes with
an [eslint](http://eslint.org/) config as well as a preconfigured [gulp](http://gulpjs.com/) build
pipeline for automated workflows (e.g. for publishing or testing). Since I prefer to follow
the [Airbnb styleguide](https://github.com/airbnb/javascript), I typically replace the
scaffolded `.eslintrc` with the config mentioned above.

*On a side-note:* my favourite generator for [angular](https://angularjs.org/) is 
[generator-gulp-angular](https://github.com/Swiip/generator-gulp-angular). Combine it with 
[eslint-plugin-angular](https://www.npmjs.com/package/eslint-plugin-angular) 
to enable static code analysis with best-practices from 
[John Papa's Angular styleguide](https://github.com/johnpapa/angular-styleguide)

# References
Following are some references to good reads regarding [Node.js](https://nodejs.org) development

## Best Practices
- https://blog.risingstack.com/node-js-best-practices/
- https://blog.risingstack.com/node-js-best-practices-part-2/
- https://blog.risingstack.com/fundamental-node-js-design-patterns/
- https://blog.risingstack.com/how-to-become-a-better-node-js-developer-in-2016/

## Security
- https://blog.risingstack.com/node-js-security-tips/
- https://blog.risingstack.com/node-js-security-checklist/

## Logging
- https://strongloop.com/strongblog/practical-examples-of-the-new-node-js-streams-api/
- https://strongloop.com/strongblog/automatic-node-js-clustering-with-log-aggregation/
- https://strongloop.com/strongblog/compare-node-js-logging-winston-bunyan/

## Other
- [Operating Node in Production](https://blog.risingstack.com/operating-node-in-production/)
- [Stream Handbook](https://github.com/substack/stream-handbook)

## Youtube Videos
- [Node.js Transaction Tracing & Root Cause Analysis with StrongLoop Arc](https://www.youtube.com/watch?v=E_tEmPwFa-U)
- [StrongLoop Tutorial: Getting Started with the Node.js API Gateway](https://www.youtube.com/watch?v=CRJh9SRglAc)
- [Best Practices for Deploying Node.js in Production](https://www.youtube.com/watch?v=if2bHALlAkw)
- [Nodejs Tutorial: Getting Started with Node.js Transaction Tracing](https://www.youtube.com/watch?v=eFJqgLjwnMU)
- [Working with Arrays and Objects in Modern JavaScript](https://www.youtube.com/watch?v=2vN28gH-sLE)
- [Node.js Tutorial: Getting Started with the ExpressJs Framework](https://www.youtube.com/watch?v=54zvhU5Y4pM)
- [JavaScript and Node.js Fundamentals](https://www.youtube.com/watch?v=iHcEZ5z7G-M)
- [zero to hero](https://www.youtube.com/watch?v=czmulJ9NBP0)
- [getting started with npm](https://www.youtube.com/watch?v=sGlJUZyapRc)
- [custom tasks with grunt](https://www.youtube.com/watch?v=ByLnV3HMyuE)
- [Nodejs in Production](https://www.youtube.com/watch?v=1b831QnPIeo)
- [Node.js npm package management and module development with Tony Pujals](https://www.youtube.com/watch?v=emXJxJb06uY)
- [nodejs fundamentals](https://www.youtube.com/watch?v=FVdH9YcB3Dg)
- [strongloop arc deep-dive](https://www.youtube.com/watch?v=ckD8KlZMl0k)
