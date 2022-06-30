# Web-dev-chat

Simple chat example for web dev class.

### Showcase

#### Implemented
- add nicknames
- save nicknames on client side (localStorage)
- reconnect when WebSocket connection is broken
- add chat history

#### Todo
- highlight messages sent by current user
- fix time issues

### Web security

Allows experimenting with XSS attack:

```html
<span onmouseover="alert('XSS testing!')">Hello all!</span>
```

```html
<img src='x' onerror='alert(1)' alt="">
```

Task: steal cookies and localStorage values from other chat participants.

## Docker

Build the image:

```shell
docker build -t web-dev-chat .
```

Run the image:
```shell
docker run --rm -it web-dev-chat:latest
```

Run and publish a port:
```shell
docker run -p 80:8080 --rm -it web-dev-chat:latest
```

Use the `docker tag` command to tag your image with the fully qualified destination path:
```shell
docker tag web-dev-chat registry.digitalocean.com/web-dev/web-dev-chat
```

Use the `docker push` command to upload your image:
```shell
docker push registry.digitalocean.com/web-dev/web-dev-chat
```