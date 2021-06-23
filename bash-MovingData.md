# Moving Data

*Copying a file or a directory*
```
cp [OPTIONS] SOURCE DESTINATION
```
	- cp -i (ask before overwrite)
	- cp -v (verbose)
	- cp -R (copy directory and content)
	- cp -a (doesn't follow symbolic link, recorsive)

*Moving a file or a directory*
```
mv FILE path/to/destination
```

*Removing file or directory*
```
rm FILENAME
```
	- rm -i  (ask for confirm)
	- rm -v  (verbose)
	- rm -Rf (recorsive, doesn't ask for confirm)

```
shred FILENAME
```
	- overwrite file 25 times

*Execute a file that contain input*
```
sh FILE
```

*Replace a word into a file*
```
sed 's\WORDTOSUBSTITUTE\NEWWORLD\' FILENAME
```