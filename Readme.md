# basic-html

1. Nginx only serves index.html as the default page.
2. http://localhost:8080
3. for app.html, COPY app.html /usr/share/nginx/html/app.html
4. http://localhost:8080/app.html

### Why this happens
1. Nginx automatically serves index.html
2. If you don’t replace it, you always get the default welcome page
3. If you copy a different file (app.html), Nginx does not use it unless you explicitly visit it

## Build
`docker build -t basic-html .`

## Run
`docker run -p 8080:80 basic-html`