# NASA Deno API

This project is the final project from a udemy course.
Intitial release on 14/11/2020.

---

## Project Structure:

```
 ┣ data
 ┃ ┗ kepler_exoplanets_nasa.csv
 ┣ public
 ┃ ┣ images
 ┃ ┃ ┗ favicon.png
 ┃ ┣ javascripts
 ┃ ┃ ┗ script.js
 ┃ ┣ stylesheets
 ┃ ┃ ┗ style.css
 ┃ ┣ videos
 ┃ ┃ ┗ space.mp4
 ┃ ┗ index.html
 ┣ src
 ┃ ┣ models
 ┃ ┃ ┣ launches.ts
 ┃ ┃ ┣ planets.test.ts
 ┃ ┃ ┗ planets.ts
 ┃ ┣ api.ts
 ┃ ┣ deps.ts
 ┃ ┣ mod.ts
 ┃ ┗ test_deps.ts
 ┣ Dockerfile
 ┣ lock.json
 ┗ README.md
```

---

## Documentation:

### Deno commands:

- To run (localhost)
`deno run --allow-net --allow-read --allow-env src/mod.ts`

- To test
`deno test --allow-read`


### Docker commands:

- To build
`docker build -t <NAME_OF_THE_CONTAINER>`

- To run (localhost)
`docker run -it -p 8000:8000 <CONTAINER_LOCATION_ON_DOCKER_HUB>`

- To run (deployment)
`docker run -it -p 8000:8000 --restart=always <CONTAINER_LOCATION_ON_DOCKER_HUB>`

### Deployment (on heroku)

- Step 1: Login
`heroku login`
`heroku container:login`

- Step 2: Create heroku app
`heroku create`
NOTE: This step will return the name of the app which was created, please copy it, it will be needed for the next step (For example: abc_xyz_1234.herokuapp.com, abc_xyz_1234 is the app name)

- Step 3: Push container to heroku
`heroku container:push web -a <APP_NAME>`

- Step 4: Release container to heroku 
`heroku container:release web -a <APP_NAME>`

- Step 5: Launch!
`heroku open -a <APP_NAME>`

Congratulations! Your app is now deployed!

NOTE: In order to update the container, repeat steps 1, 3 and 4 (step 1 if not logged in)