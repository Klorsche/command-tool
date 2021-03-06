# Steganography Tool

# *Stegseek*

Stegseek is a lightning fast steghide cracker that can be used to extract hidden data from files. It is built as a fork of the original steghide project and, as a result, it is thousands of times faster than other crackers and can run through the entirety of rockyou.txt* in under 2 seconds.

Stegseek can also be used to extract steghide metadata without a password, which can be used to test whether a file contains steghide data.

```
stegseek --crack STEGOFILE.jpg Path/to/wordlist OUTPUT.txt
```
for more info
```
https://github.com/RickdeJager/stegseek
```


# *Steghide*

Steghide is a steganography program that is able to hide data in various kinds of image- and audio-files. The color- respectivly sample-frequencies are not changed thus making the embedding resistant against first-order statistical tests. 

to embed:
```
steghide embed -cf PICTURE.jpg -ef SECRET.txt
```

to extract:
```
steghide extract -sf PICTURE.jpg
```


# *Exiftool*

ExifTool is a platform-independent Perl library plus a command-line application for reading, writing and editing meta information in a wide variety of files. 

```
exiftool PICTURE.jpg
```
