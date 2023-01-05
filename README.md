# dockerized-mern-app-template

This code was created as a means for me to understand the basics of Docker and is meant to eventually be used as a template for a "Dockerized" MERN stack app that can be forked from for easy future set up.

## To use

**This requires that you have [Docker](https://www.docker.com/products/docker-desktop/) installed already**

1. On Github.com for this repo, click "Use this Template" 
2. Select "Create new repository" from the dropdown if it appears
3. Clone the repo generated from this repo locally.
4. Run `docker-compose up`
     * The final output should look something like this:
  ```
  Use 'docker scan' to run Snyk tests against images to find vulnerabilities and learn how to fix them
[+] Running 7/7
 - Network test-template_default      Created                                                                                                          0.7s
 - Volume "test-template_mongoDB"     Created                                                                                                          0.0s
 - Volume "test-template_nodeVolume"  Created                                                                                                          0.0s
 - Container test-template-mongo-1    Started                                                                                                          5.1s
 - Container test-template-cors-1     Started                                                                                                          5.2s
 - Container test-template-node-1     Started                                                                                                          6.3s
 - Container test-template-react-1    Started
  ```
6. In your browser, navigate to http://localhost:3000/ (or whatever you set as your host port for the react container).
   * You should see the react app. 
   * You should be able to see the HTTP GET request to the backend server's `/ping` endpoint in the Network tab of the dev tools.

## Additional Note
This dockerized MERN stack template was built with the help of [this tutorial](https://adamtheautomator.com/mern-stack-tutorial/) and [this medium article](https://maximillianxavier.medium.com/solving-cors-problem-on-local-development-with-docker-4d4a25cd8cfe) with some tweaking based on [Docker Docs](https://docs.docker.com/compose/). An additional example of how to reach the backend Express server from the client can be found on lines 10-22 of /client/src/App.tsx. 
