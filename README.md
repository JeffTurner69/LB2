# LB2 - Wordpress mit Mysql Datenbank

***Installation***

Als erstes muss ein Mysql Container aufgesetzt werden, dies kann mit folgedem Befehl durchgeführt werden:
```
docker run --detach --name=test-mysql --env="MYSQL_ROOT_PASSWORD=mypassword" mysql
```

Danach wird die Wordpress Installation vorgenommen, dies kann mit folgendem Befehl durchgeführt werden. Dabei wird auch direkt die Verlinkung mit der Datenbank hergestellt:
```
docker run --detach --name test-wordpress --link test-mysql:mysql -P wordpress
```

Um zu überprüfen ob die beiden Container korrekt aufgesetzt wurden, wird folgender Befehl ausgeführt:
```
docker ps
```
