---
# You can also start simply with 'default'
theme: seriph
# some information about your slides (markdown enabled)
title: Git Commit Signing
hideInToc: true
info: One small step for Dev. One giant leap for Integrity.
# apply unocss classes to the current slide
class: text-center
# https://sli.dev/features/drawing
drawings:
  persist: false
# slide transition: https://sli.dev/guide/animations.html#slide-transitions
transition: none
# enable MDC Syntax: https://sli.dev/features/mdc
mdc: true
# open graph
# seoMeta:
#  ogImage: https://cover.sli.dev
---

# Git Commit Signing

## Or how I got away with crashing prod after being laid off

---
hideInToc: true
---

# $ whoami

- Gabriel Fournier
- 15 years DevSecOps
- Sign All My Commits Since ~2020
- Laid off in 2023
    - Crashed Prod on the day I was laid off
        - Accidentally!

---
hideInToc: true
---

# ToC

<Toc minDepth="1" maxDepth="1" />

---
hideInToc: true
layout: center
---

# Disclaimers

## I am not a lawyer

## I am not your lawyer

## This is  Not Legal Advice

---
hideInToc: true
layout: center
---

# Disclaimers

## Git Impersonation Attacks are shown as an educational aid only.

## Please replicate demos **responsibly**

---
hideInToc: true
layout: two-cols-header
---

# Scene 1

::left::

## Act 1

- Outage Over
  - Company Lost
    - Money
    - Reputation
    - SLAs
- Investigation reveals a malicious commit
  - eg: logic bomb
- Git Commit author is **you**
  - You never wrote that code

::right::

<v-click>

## Act 2
### Managers

Who fires on the spot?

</v-click>

<v-click>

### Devs

How do you defend yourself?


How do you prove Git is _wrong_ ?

</v-click>

---
src: ./pages/why-sign.md
hide: false
---

---
src: ./pages/personal-mitigations.md
---

---
src: ./pages/postmortem.md
---

---
src: ./pages/project-mitigations.md
---

---
src: ./pages/current-attacks.md
---

---

# Closing thoughts

I sign all my commits.

And so should you.

- Easy
- Mostly Transparent
- `git` is becoming an attack vector

---
hideInToc: true
layout: end
---

# Thank You!

# Questions?

<center><PoweredBySlidev/></center>

Slides: https://github.com/carboneater/devopsdays-2025-git-signing
