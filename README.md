# ansible-k8s-baremetall

### Команда запуску копіювання ссш

`cd setup_ssh_access && ansible-playbook playbook.yml -i "127.0.0.1," -e "login=root password=password"`

### Команда запуску встановлення інфраструктурм

ansible-playbook playbook.yml \
  -i "127.0.0.1," \
  -u root \
  -e "service_name=my-service \
       postgres_user=user \
       postgres_password=password \
       postgres_db=db \
       redis_password=password \
       control_plane_endpoint=hostname \
       metallb_ip=127.0.0.1 \
       storage_size=4Gi \
       ns=dev \
       use_redis=true"