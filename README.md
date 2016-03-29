# docker-denyhosts

Runs a lightweight denyhosts instance on the log you supply (usually `/var/log/secure`) and outputs denying hosts to `/etc/hosts.deny`.

## Usage

```
docker run -v /var/log/secure:/var/log/secure -v /etc/hosts.deny:/etc/hosts.deny deviavir/docker-denyhosts:latest
```

Overwrite `denyhosts.cfg` with your own settings:

```
docker run -v /var/log/secure:/var/log/secure -v /etc/hosts.deny:/etc/hosts.deny -v /your/local/denyhosts.cfg:/usr/share/denyhosts/denyhosts.cfg deviavir/docker-denyhosts:latest
```