 ### FROM node:alpine -> Specify base image
 ### WORKDIR /app -> set the working directory to '/app' in the container. all following commands will be issued relative to this dir
 ### COPY package.json/ -> Copy over the package.json file
 ### RUN  npm install -> install all dependencies
 ### COPY  ./ ./  -> copy over all of our remaining source code 

 ### CMD ["npm","start"]
 
   
 
