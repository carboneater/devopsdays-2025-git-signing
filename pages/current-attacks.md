---
level: 2
transition: none
---

# Current Supply Chain Attacks

Bypass the source git repo to publish malicious packages

```mermaid
flowchart LR

G[Git]
N[NPM]
P[🏴‍☠️Pirate🏴‍☠️]

G -.->|tokens<br/>Package|N
P -->|tokens<br/>☠️Package☠️|N
```

---
layout: two-cols-header
level: 2
---

### OpenSSF Trusted Publishing

::left::

- Uses Short-Lived OIDC Tokens
- Allows Deactivating Traditional Tokens
- Allows MFA validations
- Limits Packages Origin to a Single Provider

::right::

![NPM Trusted Publisher](/npm-sigstore.png)

::bottom::

Another cool part of SigStore?
It offers the same flows for signing
- git commit
- container

---
layout: two-cols-header
level: 2
---

# Some predictions

::left::

```mermaid
flowchart LR

GH[Git Host] ==>|🔒| R[Package<br/>Repository]
P[🏴‍☠️Pirate🏴‍☠️]

Dev -->|Code| GH

P-->|☠️Code☠️| GH
P -.-x R
```
Expect

<v-click>

- More Attacks against git?

</v-click>
<v-click>

- More Attacks targetting devs?

</v-click>
<v-click>

- New Phishing Attacks?

</v-click>

::right::

<v-click>

![🎣 📧](/phish.png)

</v-click>