# ↔️ Sync folder 

## Command

### Sync two folders

```sh
# -a Do the sync preserving all filesystem attributes
# -v run verbosely
# -u only copy files with a newer modification time (or size difference if the times are equal)
rsync -avu origin/ destination/
```

### Sync two folders (⚠️ with delete missing files)

```sh
# -a Do the sync preserving all filesystem attributes
# -v run verbosely
# -u only copy files with a newer modification time (or size difference if the times are equal)
# --delete delete the files in target folder that do not exist in the source
rsync -avu --delete origin/ destination/
```
## Example

```sh
mkdir origin;
mkdir destination;
echo "test" origin/test.txt;
# -a Do the sync preserving all filesystem attributes
# -v run verbosely
# -u only copy files with a newer modification time (or size difference if the times are equal)
# --delete delete the files in target folder that do not exist in the source
rsync -avu --delete origin/ destination/
cd origin/;
echo "test2" origin/test2.txt;
cd ..
rsync -avu origin/ destination/
#tree
#.
#├── destination
#│   ├── test.txt
#│   └── test2.txt
#└── origin
#    ├── test.txt
#    └── test2.txt
cd origin/; rm test.txt; cd -
rsync -avu --delete origin/ destination/
#tree
#.
#├── destination
#│   └── test2.txt
#└── origin
#    └── test2.txt
```
