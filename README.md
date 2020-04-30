## `bin/`

### [`mkstruct`](bin/mkstruct)

`structure.txt` content (**indentation** is equal to **two spaces**):

```
root/
  a/
    .git/
  b/
    file
    script.py
    module/
      lib.py
```

```console
$ cat structure.txt | mkstruct
$ ls root -AR
```

```
root:
a/  b/

root/a:
.git/

root/a/.git:

root/b:
file  module/  script.py

root/b/module:
lib.py
```