First create or open (if already exists) file .vimrc :

`vim ~/.vimrc`
Now enter (in insert-mode activated with i) the following lines:

```sh
set expandtab
set tabstop=2
set shiftwidth=2
```
Save and close the file by pressing Esc followed by :x and Enter.

Settings explained:
```
expandtab: use spaces for tab
tabstop: amount of spaces used for tab
shiftwidth: amount of spaces used during indentation
```