## GIT Signing Commits


- Setting up gpg key id

```bash
$ git config --global user.signingkey <GPG KEY ID>
```

- Default to always sign commits 

```bash
$ git config --global commit.gpgsign true 
```

- Sign individual commit

```bash
$ git commit -S -m <COMMIT MESSAGE>
```
