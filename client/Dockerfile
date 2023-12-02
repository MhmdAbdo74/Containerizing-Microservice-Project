#muilti stage Docker file first stage for build and get artifact and second for host angular app on nginx
FROM node:14 AS web-build 

WORKDIR /usr/src/app

COPY ./ ./client

RUN cd client && npm install && npm run build --prod

#use nginx image to host angular app on it 
FROM nginx:latest

#copy the build from the previous stage to the nginx image
COPY --from=web-build /usr/src/app/client/dist/client/ /usr/share/nginx/html
#customize nginx file
COPY ./nginx.conf /etc/nginx/conf.d/default.conf
#expose port 4200
EXPOSE 4200
