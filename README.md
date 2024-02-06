# sample-project
# Simplifying Docker 
-v "$(pwd):/app" -v /app/node_modules docker <image name>
docker build -t  docker .

# clone the repository from github
git clone https://github.com/dockersamples/node-web-app.git

# switch to your own new line of  code (branch)
git checkout -b <branch-name>


# make changes and commit them
git add . && git commit -m "Made some changes"

#switch back to the stage branch
git checkout stage


# pull in your  latest changes from upstream
git pull origin stage

# push your branch up to Github so it can be pulled by others for collaboration
git push origin <branch-name>


# pull down someone else's branch onto yours, then merge their work into yours
git pull origin <someone-elses-branch>:<your-new-branch>

# create a PR in GitHub to get your code reviewed and merged with the mainline



# create a repository in dockerhub.
# copy the name of the repository from your dockerhub.
# tag the image
# docker tag docker_img <username>/<repo>:latest
docker tag docker bukola541/docker-sampler:0.0.1

# log in to dockerhub
docker login --username=bukola541 --email=bukola54@gmail.com --password=*********

# push the image to the repo
docker push bukola541/docker-sampler:0.0.1
# run the container with port mapping and volume mounting
docker run -d -p 8080:3000 -v "$(pwd)":/app bukola541/docker-sampler:0.0.1 node app.js

docker
docker images 
docker tag
docker run --name my-running-app -p 8080:80 <name-of-image>
docker ps 
docker ps -a 