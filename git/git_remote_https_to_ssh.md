## GIT - Change remote URL [HTTPS -> SSH]

Git asking for username and password when SSH was already configured. Originally cloned repository using HTTPS URL.

Check remote URL.

```bash
$ git remote -v
```

Change remote URL.

```bash
$ git remote set-url origin git@github.com:USERNAME/repository.git
```

[More details](https://help.github.com/articles/changing-a-remote-s-url/)
