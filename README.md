# Pointivo Reusable Workflows

Intentionally blank.

### Promotions

We are using `workflow_dispatch:` so that we can trigger promotions from an HTTP request.
The correct POST + payload is shown below:


```shell
curl --request POST \
  --url 'https://api.github.com/repos/<USERNAME>/<REPO>/dispatches' \
  --header 'authorization: Bearer <TOKEN>' \
  --data '{"event_type": "promotion","client_payload": {"image": "my-app", "tag": "3.0.0_release_GH1.abc123", "platform": "master" }}'
```