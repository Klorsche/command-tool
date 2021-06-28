# VIM

Vim is a clone, with additions, of Bill Joy's vi text editor program for Unix. Vim's author, Bram Moolenaar, based it on the source code for a port of the Stevie editor to the Amiga and released a version to the public in 1991. Vim is designed for use both from a command-line interface and as a standalone application in a graphical user interface. Vim is free and open-source software and is released under a license that includes some charityware clauses, encouraging users who enjoy the software to consider donating to children in Uganda. The license is compatible with the GNU General Public License through a special clause allowing distribution of modified copies "under the GNU GPL version 2 or any later version".

*Open VIM*
```
vim
```
```
vim FILENAME
```

*Insert Mode*
	- h,j,k,l 	arrows functionality
	- esc 		enter command mode

*Command Mode*
```
:q!		     	(quit without saving)
:w		     	(save file)
:w FILENAME  	(save file with name)
:wq			 	(save file and quit)
:q 			 	(exit but if there are changes fail)
i 			 	(enter insert mode)
:%s/old/new/g 	(change lines asking for permission)
:%s/old/new/gc 	(change lines without asking for permission)
u 				(undo)
ctrl+R 			(redo)
:set number		(add number to lines)
/WORD			(find word and set cursor)
:LINESNUMBER	(set cursor on the line specified)
(N°)dd 			(delete number of line from the cursor position)
D 				(delete entire line)
y 				(copy - example 3yw copy 3 words)
yy or Y 		(copy entire line)
y$ 				(copy from the cursor to the end of the line)
p 				(print text after cursor)
P 				(print text before cursor)
x 				(delete character after cursor)
X 				(delete character before cursor)
dw 				(delete word)
```

*Visual Mode*
```
v + cursor movement 	(select character)
V 						(select entire line)
G 						(select from the cursor to the end)
gg 						(select from the cursor to the beginning)
w 						(move from word to word foreward - cursor on the first character)
e 						(move from word to word foreward - cursor on the last character)
b 						(move from word to word backword)
0						(move to begining line)
$						(move to end line)
A 						(move to end line and enter insert mode)
```
