outline
---

Configure and run unprivileged Outline server as docker container into systemd.service.


### Links
- <https://getoutline.com>
- <https://github.com/outline>


### Variables
- **`outline_docker_image`** *(type=string, default="outlinewiki/outline:latest")* - Docker image for using into systemd.service.

- **`outline_docker_network`** *(type=string, default="bridge")* - Connect a container to a network as `docker run --network=...`.
- **`outline_docker_publish_ports`** *(type=list, default=["127.0.0.1:3000:3000"])* - List of strings with publish a container’s ports to the host as `docker run --publish=...`.

- **`outline_docker_envs`** *(type=list, default=[])* - List of objects in format `{KEY: value}` for set environment variables as `docker run --env=...`.
- **`outline_docker_labels`** *(type=list, default=[])* - List of objects in format `{key: value}` for set meta data on a container as `docker run --label=...`.


### Examples
```yaml
outline_docker_image: outlinewiki/outline:0.72.2
outline_docker_network: host
outline_docker_envs:
  PORT: "3000"
  NODE_ENV: production
  ENABLE_UPDATES: "false"
  DEFAULT_LANGUAGE: en_US
```
