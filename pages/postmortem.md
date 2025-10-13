---
layout: two-cols-header
level: 2
transition: none
---

# Incident Summary (How I Crashed Prod)

::left::

- Wednesday Morning
  - Laid off at the end of the week
- $everance Agreement
  - Conditions include no sabotage

````md magic-move {lines: true}
```yaml
gab:
  user.present:
    - fullname: Gabriel Fournier
    - shell: /bin/bash
    - home: /home/gab
    - uid: 4000
    - gid: 4000
    - groups:
      - wheel
```
```yaml
gab:
  user.absent:
    purge: true
```
````
<v-click>

- Salt Apply

</v-click>

::right::

<v-click>

- CD starts failing all its jobs
  - No CD is not using my account

</v-click>
<v-click>

- Most every service gets in degraded state
  - Services don't restart

</v-click>
<v-click>
<hr/>

- SaltStack Updated Docker from 19 to 20
  - A config key was changed
  - Sentry didn't restart
    - Our services wait for Sentry when starting

</v-click>
<v-click>
<hr/>

- Update Docker Config
  - Sentry Restarts
    - All Services Bootstrap

</v-click>

---
layout: two-cols-header
transition: none
---

# Why Git Signing Saved Me

## Courts hold Crypto Signatures as Valid

::left::

<v-click>

### Expose malice from

```diff
gab:
-  user.present:
-    - fullname: Gabriel Fournier
-    - shell: /bin/bash
-    - home: /home/gab
-    - uid: 4000
-    - gid: 4000
-    - groups:
-      - wheel
+  user.absent:
+    purge: true
```

</v-click>

::right::

<v-click>

### Find a shortcoming in GPG
#### that invalidates the signature

Please Disclose Responsibly!

</v-click>

::bottom::

<v-click>

Ruled non-sabotage by all involved

Contributing factors:
- Helped Identify & Resolve the Incident
- Wrote the Incident Report

</v-click>