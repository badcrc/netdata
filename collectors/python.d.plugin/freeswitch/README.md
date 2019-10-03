# freeswitch

This module will monitor one freeswitch server. Server can be either local or remote.

**Requirements:**

-   freeswitch with configured 'Event Socket Library'
-   Python library for connecting to ESL

Example freeswitch configuration can be found in 'python.d/freeswitch.conf'

It produces following charts:

1.  **Active calls**

    -   calls

2.  **Registrations**

    -   registrations

3.  **Gateways** by Status

    -   UNREGED
    -   TRYING
    -   REGISTER
    -   REGED
    -   UNREGISTER
    -   FAILED
    -   FAIL_WAIT
    -   EXPIRED
    -   NOREG
    -   TIMEOUT

4.  **Profiles** by Status

    -   RUNNING
    -   DOWN

## configuration

Needs only `url` to server's `stub_status`

Here is an example for local server:

```yaml
update_every : 10
priority     : 90100

localhost:
  name : 'local'
  host  : '127.0.0.1'
  port  : 8021
  password  : 'ClueCon'
```

Without configuration, module attempts to connect to `localhost:8021` with `ClueCon` as default password.

---

[![analytics](https://www.google-analytics.com/collect?v=1&aip=1&t=pageview&_s=1&ds=github&dr=https%3A%2F%2Fgithub.com%2Fnetdata%2Fnetdata&dl=https%3A%2F%2Fmy-netdata.io%2Fgithub%2Fcollectors%2Fpython.d.plugin%2Ffreeswitch%2FREADME&_u=MAC~&cid=5792dfd7-8dc4-476b-af31-da2fdb9f93d2&tid=UA-64295674-3)](<>)
