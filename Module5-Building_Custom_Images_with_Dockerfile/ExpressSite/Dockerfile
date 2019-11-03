FROM node:latest        
# Pulls the latest node image. New image will be built on top of this.

MAINTAINER Sudarshan Veeramreddy

WORKDIR /var/www	
# Commands will be run from this director

COPY . .		
# Copy all contents in current directory to workdir in the image.

ENV PORT=3000

VOLUME ["/logs"]	
# we can provide multiple volume paths. This will be stored in host system. If  we give, /var/www here, it mounting it will wipe out contents in the folder. So RUN npm install etc would be gone and container wouldn't come up.

RUN npm install		
# npm install in workdirector

EXPOSE $PORT

ENTRYPOINT ["npm", "start"]   
# command to run when container starts.
