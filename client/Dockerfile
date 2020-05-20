# Build Phase 
FROM node:alpine

WORKDIR /app

#  AWS Elastic beanstalk deployment issue
COPY package*.json ./ 

RUN npm install 

COPY . .

# produces a /build directory in /app
RUN npm run build

# Run Phase
# nginx is used for routing
FROM nginx

EXPOSE 3000

COPY ./nginx/default.conf /etc/nginx/conf.d/default.conf

COPY --from=0 /app/build /usr/share/nginx/html
