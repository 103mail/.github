# 103mail

European email that stays in Europe.

[103mail](https://103mail.com) is a webmail service that looks and feels like
regular email, but your messages don't travel across the globe. They live in
one European data center, and only a notification with a secure link leaves
the server. That is how we do privacy by design.

We are building a federated version, so independently run domains can
exchange mail with each other without falling back to SMTP.

## Repositories

| Repository | What it is |
| --- | --- |
| [webmail-federation](https://github.com/103mail/webmail-federation) | The RFC, design and plan for federating Webmail Domains |
| [webmail-server](https://github.com/103mail/webmail-server) | Go backend serving the JSON API and the federation endpoints |
| [webmail-client](https://github.com/103mail/webmail-client) | React client that every Domain runs for its users |
| [webmail-e2e](https://github.com/103mail/webmail-e2e) | End-to-end stories that run against several federated Domains |
| [webmail-deploy](https://github.com/103mail/webmail-deploy) | Local stack with four Domains federating on one machine |

To try it locally, clone the repositories side by side and run
`docker compose up -d --build` in `webmail-deploy`. Then open each Domain in
your browser:

- http://localhost:8001/ (103mail.com)
- http://localhost:8002/ (example.com)
- http://localhost:8003/ (mail.acme.test)
- http://localhost:8004/ (acme.test)
