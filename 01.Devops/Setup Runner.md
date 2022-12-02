## Create runner 

```bash
sudo docker run -d --name gitlab-runner --restart always   -v /srv/gitlab-runner/config:/etc/gitlab-runner   -v /var/run/docker.sock:/var/run/docker.sock   gitlab/gitlab-runner:alpine-v15.2.2
```

## Register runner

```bash
docker run --rm -v /srv/gitlab-runner/config:/etc/gitlab-runner gitlab/> gitlab-runner:latest register \
  --non-interactive \
  --executor "docker" \
  --docker-image alpine:latest \
  --url "https://master3.takima.io/" \
  --registration-token "PROJECT_REGISTRATION_TOKEN" \
  --description "docker-runner" \
```

-it -> interactive tty
--rm -> pour supprimer le container après utilisation