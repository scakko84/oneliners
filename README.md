# oneliners
A collection of terminal oneliners

## Bash

Replace spaces with dots in filenames recursively
```console
find . -depth -name "* *" -execdir rename 's/ /./g' "{}" \;
```
Copies directory to remote path via scp
```console
scp -r directory user@host:"'path/with spaces/'"
```

## MacOS

Convert iso file to img file
```console
hdiutil convert -format UDRW target.iso -o target.img
```
