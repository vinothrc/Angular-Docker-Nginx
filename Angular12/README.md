# Angular-Docker-Nginx

git clone https://github.com/vinothrc/Angular-Docker-Nginx.git 
cd Angular12 
sudo npm install -g @angular/cli
ng new example1
mv Dockerfile docker-compose.yml conf.d example1/
cd example1/
docker-compose build
docker-compose up &
