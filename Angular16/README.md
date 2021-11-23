# Angular-Docker-Nginx

git clone https://github.com/vinothrc/Angular-Docker-Nginx.git
sudo npm install -g @angular/cli
ng new example1
mv Dockerfile docker-compose.yml example1/
cd example1/
docker-compose build
docker-compose up &
