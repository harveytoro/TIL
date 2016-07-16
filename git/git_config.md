##GIT Config

Replace all global emails with single email address.

```bash
$ git config --global --replace-all user.email "email@email.com"
```

Check what email addresses are configured with git.

```bash
$ git config --get-all user.email
```
