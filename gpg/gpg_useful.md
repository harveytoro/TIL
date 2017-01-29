##gpg Useful commands


- List Keys

```bash
$ gpg --list-keys

$ gpg --list-secret-keys
```

- Export

```bash
$ gpg --armor --export <GPG KEY ID>

$ gpg --armor --export-secret-keys <GPG KEY ID>
```

- Edit key

```bash 
$ gpg --edit-key <GPG KEY ID>

gpg> adduid
```

- Import

```bash
$ gpg --import public.asc

$ gpg --allow-secret-key-import -- import private.asc
```
