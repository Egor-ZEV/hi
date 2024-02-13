version: '3.7'

services:
  mariadb:
    image: mariadb
    restart: always
    environment:
      MYSQL_ROOT_PASSWORD: example
    ports:
      - "3306:3306"
    volumes:
      - mariadb_data:/var/lib/mysql

  daloradius:
    image: osixia/daloradius:latest
    restart: always
    environment:
      DALORADIUS_DB_HOST: mariadb
      DALORADIUS_DB_PORT: 3306
      DALORADIUS_DB_NAME: radius
      DALORADIUS_DB_USER: radius
      DALORADIUS_DB_PASSWORD: radius
    ports:
      - "80:80"
    depends_on:
      - mariadb

volumes:
  mariadb_data:

