##LaTeX - Count words

Count words in tex document.

```bash
$ detex document.tex | tr -cd '0-9A-Za-z \n' | wc -w
```

Count words in PDF document.

```bash
$ ps2ascii document.pdf | wc -w
```