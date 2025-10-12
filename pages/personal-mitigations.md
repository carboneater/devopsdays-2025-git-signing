---
hideInToc: true
layout: section
transition: none
---

# Mitigation: Least Privileges

### ✅ I can't impersonate you on a repo I don't have write access to

---
layout: section
---

# Mitigation: Git Commit Signing

---
layout: two-cols-header
level: 2
---

# Cryptographic Signatures

::left::

![Carney's Signature](/100-front.jpg)

Source: [Bank of Canada](https://www.bankofcanada.ca/banknotes/bank-note-series/frontiers/100-polymer-note/)

::right::

- Authentication
- Integrity
- Non-Repudiation

<!--
Authentication: The Author is who they claim to be
Integrity: The document wasn't altered
Non-Repudiation: There is exactly one author and we can positively identify them. If they want to claim there was fraud, they have the duty to prove how someone could compromise the algorithms to be considered as them.
-->

---
level: 2
---

# [Generating a Key](https://docs.github.com/en/authentication/managing-commit-signature-verification/generating-a-new-gpg-key)

> $ gpg --default-new-key-algo ed25519 --gen-key

Answer all the prompts

``` {|2}
pub   ed25519 2025-10-12 [SC] [expires: 2028-10-11]
      9D38D37552251C5D354F5FC5A04163ECF659F045
uid                      Gabriel Fournier <gab@demo.dod>
```

<v-click>

> $ gpg --armor --export 9D38D37552251C5D354F5FC5A04163ECF659F045

```
-----BEGIN PGP PUBLIC KEY BLOCK-----

mDMEaOvShxYJKwYBBAHaRw8BAQdAClN956LDwVfUUeukMiSY72YBDYtgJaY1cLP7
vnpdney0H0dhYnJpZWwgRm91cm5pZXIgPGdhYkBkZW1vLmRvZD6ImQQTFgoAQRYh
BJ0403VSJRxdNU9fxaBBY+z2WfBFBQJo69KHAhsDBQkFo5qABQsJCAcCAiICBhUK
CQgLAgQWAgMBAh4HAheAAAoJEKBBY+z2WfBFAbQBAIvzJjB6EiMfwmHctwXzEmLP
ril30ZFjew8ZchIF2yD7AQDp2FXzrbnSN8R5tShWJiy+3OETH6tyZLkPWNcP3AZ+
CA==
=feSD
-----END PGP PUBLIC KEY BLOCK-----
```

</v-click>

---
level: 2
---

# Configuring Git to sign commits

``` {1|2|3|4|}
git config --global user.signingKey 9D38D37552251C5D354F5FC5A04163ECF659F045
git config --global commit.gpgsign true
git config --global tag.gpgsign true
git config --global push.signing if-asked
```

---
layout: center
level: 2
---

# [Publish your Public Key to github](https://docs.github.com/en/authentication/managing-commit-signature-verification/adding-a-gpg-key-to-your-github-account#adding-a-gpg-key)

---
layout: center
level: 2
---

# Protip: Private Key Propagation

### Do not export your keys, having 1+ key/device is very fine

---
layout: center
level: 2
---

# [Enable Vigilant Mode](https://docs.github.com/en/authentication/managing-commit-signature-verification/displaying-verification-statuses-for-all-of-your-commits)

| Default | Vigilant | Note|
|---------|----------|-----|
| Verified | Verified | |
| Verified | Partially Verified | |
| Unverified | Unverified | |
| (Nothing)  | Unverified | |