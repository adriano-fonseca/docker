# docker-wordpress-mysql

This is compose file that intend to demostrate how use secrets, internally or externally in order to protect sensible data from the application.

To deploy it, you need to be running your engine in swarm mode and to create a secret, that is used externally in the file:

```

echo "wordpress" | docker secret create db_password -

```

To deploy:

```

docker stack deploy -c docker-compose.yml wordpress

```

Internally the secret can be created like it was from the file db_user.txt
