---
hideInToc: true
layout: section
transition: none
---

# But, wait!!!

## All your mitigations are positive validations

## They don't reject unsigned stuff

---
layout: two-cols-header
level: 2
---

# Still Saved Me!

::left::

- Wednesday Morning
  - Laid off at the end of the week
- Severance Agreement
  - Conditions include no sabotage
- 

::right::

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