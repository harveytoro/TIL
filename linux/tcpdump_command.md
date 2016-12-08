## TCPDUMP

Determine available interfaces

```bash
$ tcpdump -D
```

Change interface

```bash
$ tcpdump -i lo0
```

Write to a file

```bash
$ tcpdump -w filename
```

Filter by port 

```bash
$ tcpdump port 80

$ tcpdump src port 80

$ tcpdump dst port 80
```


