---
owner_slack: "#govuk-developers"
title: Switch an app off temporarily
layout: manual_layout
section: Deployment
parent: "/manual.html"
---

In the event of a security incident an app may need to be switched off until it
can be patched.

Stop Puppet from running on the relevant machines:

```sh
$ fab $environment node_type:frontend puppet.disable:"Reason for disabling Puppet"
```

Stop the app on the relevant machines:

```sh
$ fab $environment node_type:frontend app.stop:frontend
```
