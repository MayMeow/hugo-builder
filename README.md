# hugo-builder
Docker image for CI to build pages with Hugo

## How to use?

Example usage with GitlabCi and gitlab pages

```yaml
image: maymeow/hugo-builder:v0.71.1

pages:
  script:
    - hugo
  artifacts:
    expire_in: 1 week
    paths:
      - public
  only:
    - master
  tags:
    - docker
    - digitalocean

```
