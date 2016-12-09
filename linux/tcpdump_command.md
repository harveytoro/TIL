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
Read a file, written using -w

```bash
$ tcpdump -r filename
```

Filter by port 

```bash
$ tcpdump port 80

$ tcpdump src port 80

$ tcpdump dst port 80
```

Filter by host

```bash
$ tcpdump host 127.0.0.1

$ tcpdump src host 127.0.0.1

$ tcpdump dst host 127.0.0.1
```
