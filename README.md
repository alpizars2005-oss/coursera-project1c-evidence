# Coursera Project 1c — Public OpenPGP Evidence
This is a **public-only static mirror** for the Project 1c coursework. Its source-of-truth is a **separate, private** development repository named `coursera-project1c-gpg`. The private repository is where future corrections, new tests, and improvements should be made. This public mirror should only be updated after the changes have been validated and deliberately approved for public distribution.

## Hosting
Enable **Settings → Pages → Deploy from a branch → main → /(root)**. Then the expected site URL is:

https://alpizars2005-oss.github.io/coursera-project1c-evidence/

Do not report it as live before it loads correctly.

## Cryptographic evidence
- Original public key: `pgp/mypubkey.asc` (fingerprint `8B1F9D51E6274659A85A255ACDB64ABE6D434410`; both keyservers verified this key).
- Replacement signing public key: `pgp/mypubkey-new.asc` (fingerprint `29B7AA73720168E2E21A546B5DE6353FAA731507`; separate from the original key).
- Real Apache source upstream signature: `pgp/httpdVerified.html`.
- Genuine academic student signature: `pgp/httpd.bz2.gpg` over `pgp/httpd.bz2`.
- Actual student GPG verification transcript: `pgp/personalSignatureVerified.html`.
- Verification guide: `pgp/myhttpd.html`.
- Official source archive SHA-256: `eb397feeefccaf254f8d45de3768d9d68e8e73851c49afd5b7176d1ecf80c340`.
- This repository uses the **Apache 2.4.54 historical source** for classroom signature checks only. No claim of student authorship or production safety.

## Security
The public site contains no secret keys, revocation certificates, login credentials, or private GitHub Actions tokens. Only public OpenPGP keys and student-authorized public academic evidence are included. The original key has **not** yet been revoked. Never automatically synchronize arbitrary files from the private repository to the public one.

## AWS Academy
The learner requested AWS Academy access and did not receive it. The alternative GitHub Pages deployment is disclosed in `statement.html`; **this is not AWS EC2 evidence**.

## Publishing the archived Apache source
The `stage-archive.yml` GitHub Actions workflow downloads the original Apache source over HTTPS, checks its pinned SHA-256 and the student's detached signature against the replacement public key, and only on success commits `pgp/httpd.bz2` to the public repository. A failed check must leave the archive unpublished.
