# Remove duplicated files

Find all duplicate files (by content, not by name) in the current directory:

```sh
fdupes -r .
```

Find and manually confirm deletion of duplicated files

```sh
fdupes -r -d .
```

Find and automatically delete all copies but the first of each duplicated file (🚧 this actually deletes files):

```sh
fdupes -r -f . | grep -v '^$' | xargs rm -v
```

I'd recommend to manually check files before deletion:

```sh
fdupes -rf . | grep -v '^$' > files
```

Check files

```sh
xargs -a files rm -v
```
