# Installation Notes

- Go to [cloudflare team dash](https://dash.teams.cloudflare.com)
  and create a tunnel or migrate a current tunnel(this action is not reversible)

- Copy the token from tunnel's overview **Install and run a connector** section.

  This is what your token may look like.

  ```text
  eyJhIjoiNDJhYmYwMTQzNGMyMeUzNDMzMTE1Y2M0YmFhZGY0YTciLCJ0IjoiNzBiNza5zTItMWViMS00MjdjaWFiZjEtZWMwdzIwNmQwZmI3IiwicyI6IlltRmxPV1ExTldZdE16a3lOUzAwsW1KbUxUZzJPVGN0Wm1VelptVmpaak00T1dZeiJ5
  ```

- Set `token` with **your** tunnel's token. the tunnel ID will NOT work.
- Now you can manage the tunnel via cloudflare dash by setting a private network or create ingress rules for your services and domain, you can use this as a reverse proxy directly or use it in conjunction with traefik if you are behind a CGNAT, do not have a static IP, nor can not portforward 443(SSL).
- Please note you MAY need to modify cloudflared Zero Trust various settings in order for this work out-of-the-box which is beyond the scope of this guide.
