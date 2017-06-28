
# build commands

- docker build --rm -t lvguanming/mysql56 .
- docker login
- docker push lvguanming/mysql56
- docker run -p 127.0.0.1:3306:3306 --name mysql-a lvguanming/mysql56
- mysql -uroot -p