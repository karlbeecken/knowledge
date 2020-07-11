---
layout: default
title: Autosign Git commits
---

# Autosign Git commits

You need to do 2 things:

1. tell Git what should be your default GPG signing key: `git config --global user.signingkey <key id>`
2. enable autosign for every commit (can be done per-repo without the `--global` flag): `git config --global commit.gpgsign true`

_Source: [StackOverflow](https://stackoverflow.com/questions/10161198/is-there-a-way-to-autosign-commits-in-git-with-a-gpg-key "Is there a way to “autosign” commits in Git with a GPG key?")_
