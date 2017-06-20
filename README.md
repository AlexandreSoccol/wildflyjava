mysqldb:
  container_name: "db"
  image: mysql:latest
  environment:
    MYSQL_DATABASE: sample
    MYSQL_USER: mysql
    MYSQL_PASSWORD: mysql
    MYSQL_ROOT_PASSWORD: supersecret
mywildfly:
  image: arungupta/wildfly-mysql-javaee7
  environment:
    - MYSQL_URI=db:3306
  ports:
    - 8080:8080
