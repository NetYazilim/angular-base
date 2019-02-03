# angular-base
## Base image for Angular app

````
# Example Dockerfile
  FROM netyazilim/angular-base
  EXPOSE 80
  RUN rm /var/lib/nginx/html/*
  COPY dist/ /var/lib/nginx/html/

# Build app 
  ng build --prod --outputPath=dist

# Build & Run image
  docker build -t app . 
  docker run -p 80:80 app
````