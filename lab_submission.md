## 1. Docker command to create and run a container named `dbserver-mysql-nairobi`

Use the `customized-ubuntu:1.0` image to create a container named `dbserver-mysql-nairobi`. The command should map the container’s port 3306 to the host’s port 3309.

```bash
docker run -d --name dbserver-mysql-nairobi -p 3309:3306 customized-ubuntu:1.0
```

## 2. MySQL Server and MySQL Client Installation in Ubuntu

```bash
apt-get update && apt-get install -y mysql-server mysql-client
```

## 3. Login using the MySQL Client and Change the MySQL Root Password

```sql
mysql -u root -p
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY '5trathmore';
FLUSH PRIVILEGES;
EXIT;
```
