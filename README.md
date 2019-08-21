# WP_Devops
Deploy WP+Mysql + Ngiinx + php-fpm+letsEncrypt+docker Swarm

Create directories on host
Directories are created on the host and volume mounted to the docker containers. This allows the user to persist data beyond the scope of the container itself. If volumes are not persisted to the host the user runs the risk of losing their data when the container is updated or removed.
From the top level of the cloned repository, create the directories that will be used for managing the data on the host.

mkdir -p certs/ certs-data/ nginx/ logs/nginx/ db-data/ wordpress/


docker stack deploy -c docker-compose.yml stack-wp-acqio
