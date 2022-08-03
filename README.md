# NX Issue 1230

Here is a scenario that I would expect to work but it fails

**Scenario**

I have a node app that import a library

The node app uses
- `@nrwl/node:node` to serve (during development)
- `@nrwl/js:tsc` to build the output (during production deployment)

I would like to run `node dist/packages/demoapp/src/main.js` in prodution environment

**Outcome**

- `npx nx serve demoapp --watch=false` produces expected result
<img width="708" alt="image" src="https://user-images.githubusercontent.com/2660614/182497014-53e96bc3-bf1c-40a3-87a8-36d980adbd3c.png">

- `node dist/packages/demoapp/src/main.js` produces unexpected result

<img width="464" alt="image" src="https://user-images.githubusercontent.com/2660614/182497122-22cc33ab-414b-44c7-8e23-84d78954f7f6.png">

My expectation is that those two commands should produce similar result

**What would you recommend as a fix ?**

Here is a link to the sample code https://github.com/nshimiye/nx-sample-app
