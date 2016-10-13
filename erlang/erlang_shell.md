## The Erlang Shell

To start:

```bash
$ erl
```

Basic usage: expressions finished with dot and space.

```bash
1> X = 2. 
```

Compile and run in shell (hello.erl):

```bash
1> c(hello). 
2> hello:start(). 
```

Compile and run outside shell (hello.erl):

```bash
$ erlc hello.erl
$ erl -noshell -s hello start -s init stop
```

