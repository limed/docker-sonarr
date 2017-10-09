#### Building image
```
docker build -t sonarr .
docker push limed/sonarr
```

#### Running image
```bash
docker pull limed/sonarr
docker run -d \
        -p 127.0.0.1:8989:8989 \
        -v /docker/sonarr/:/config \
        -v /data/media/TV:/data \
        --restart=always \
        --name sonarr  \
        limed/sonarr

```

```bash
cd docker-sonarr/ansible
ansible-playbook -vv -K sonarr.yml
```
