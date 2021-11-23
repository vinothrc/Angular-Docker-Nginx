# Angular-Docker-Nginx

git clone https://github.com/vinothrc/Angular-Docker-Nginx.git \n
cd Angular12 \n
sudo npm install -g @angular/cli
ng new example1
mv Dockerfile docker-compose.yml conf.d example1/
cd example1/
docker-compose build
docker-compose up &
