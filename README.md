# RustDesk Server application stack for Kubernetes on Wodby

Deploy the open-source RustDesk server on Kubernetes with Wodby.

This repository defines the Wodby stack manifests and default service
composition for RustDesk Server.

<!-- wodby:generated:start -->

## Stack contract

- [RustDesk Server stack on Wodby](https://wodby.com/stacks/rustdesk)
- [Browse Wodby application stacks](https://wodby.com/stacks)
- [Wodby stack documentation](https://wodby.com/docs/2.0/stacks/)
- [Stack manifest reference](https://wodby.com/docs/2.0/stacks/template/)

## Service definitions

- [RustDesk Server service](https://github.com/wodby/service-rustdesk)

## What's included

| Component / service | Default configuration |
| --- | --- |
| RustDesk Server<br>`rustdesk` | required; enabled by default |

Enabled optional services are selected by default but can be excluded when an
app is created. Disabled optional services are available but not selected by
default. Required services cannot be excluded.

## Validate the stack manifest

```bash
wodby stack validate-manifest stack.yml --org <org-id>
```

<!-- wodby:generated:end -->

## Connect devices

RustDesk devices connect over WebSocket to the `rustdesk` service's HTTPS domain, so no ports need publishing. Run the
service's **Show client settings** action and enter the values it prints in the RustDesk app on each device, with
**Use WebSocket** turned on. See the [service README](https://github.com/wodby/service-rustdesk#connect-devices).
