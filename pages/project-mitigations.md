---
hideInToc: true
layout: section
transition: none
---

# But, wait!!!

## All your mitigations are positive validations

## They don't reject unsigned stuff

---
layout: section
---

# Project-Level Mitigations

## When all your devs are signing

---
level: 2
---

# [Require Signed Commits](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-rulesets/available-rules-for-rulesets?versionId=free-pro-team%40latest&productId=authentication&restPage=managing-commit-signature-verification%2Cabout-commit-signature-verification#require-signed-commits)

| Default | Vigilant | State |
|---------|----------|-------|
| Verified | Verified | ✅ |
| Verified | Partially Verified | ✅ |
| Unverified | Unverified | ❌ |
| (Nothing)  | Unverified | ❌ |

---
level: 2
---

# Signature isn't enough

GitHub has an internal key you don't control!

![GH Internal Signatures](/GH-signature.png)

---
layout: two-cols-header
level: 2
---

# Shai-Hulud Worm

::left::

- Harvests
    - NPM Tokens
    - GitHub PATs
    - API Keys
        - AWS
        - Azure
        - GCP

::right::

- Persistence via `shai-hulud-workflow.yml`

---
level: 2
---

# Controlling Authorized Keys with `sq-git`

> $ sudo apt install sq-git  
> $ sq-git init  
> $ sq-git policy authorize  --project-maintainer "Gabriel Fournier <gab@gfournier.ca>" 8F570C8B1C01FCC8  
> $ git add openpgp-policy.toml  
> $ git commit -m 'Add signing policy.'  
> $ git push origin signing-policy  