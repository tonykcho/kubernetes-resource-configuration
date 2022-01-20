# Trouble Shooting

## Host 127.0.0.1 is not allowed to connect to this MySQL server

Set username to 'user' and password to 'password'

```
kubectl exec -it <pod_name> -- /bin/bash
mysql -u root -p
CREATE USER 'user'@'%' IDENTIFIED BY 'password';
GRANT ALL PRIVILEGES ON *.* TO 'user'@'%' WITH GRANT OPTION;
FLUSH PRIVILEGES;
```