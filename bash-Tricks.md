# Bash Trick

*Shell shortcut*

 - Ctrl+L: Clear the screen. This is similar to running the “clear” command.
 - Ctrl+S: Stop all output to the screen. This is particularly useful when running commands with a lot of long, verbose output, but you don’t want to stop the command itself with Ctrl+C.
 - Ctrl+Q: Resume output to the screen after stopping it with Ctrl+S.
 - Ctrl+C: Interrupt (kill) the current foreground process running in in the terminal. This sends the SIGINT signal to the process, which is technically just a request—most processes will honor it, but some may ignore it.
 - Ctrl+Z: Suspend the current foreground process running in bash. This sends the SIGTSTP signal to the process. To return the process to the foreground later, use the fg process_name command.
 - Ctrl+D: Close the bash shell. This sends an EOF (End-of-file) marker to bash, and bash exits when it receives this marker. This is similar to running the exit command.
 - Ctrl+A or Home: Go to the beginning of the line.
 - Ctrl+E or End: Go to the end of the line.
 - Alt+B: Go left (back) one word.
 - Ctrl+B: Go left (back) one character.
 - Alt+F: Go right (forward) one word.
 - Ctrl+F: Go right (forward) one character.
 - Ctrl+XX: Move between the beginning of the line and the current position of the cursor. This allows you to press Ctrl+XX to return to the start of the line, change something, and then press Ctrl+XX to go back to your original cursor position. To use this shortcut, hold the Ctrl key and tap the X key twice.
 - Ctrl+D or Delete: Delete the character under the cursor.
 - Alt+D: Delete all characters after the cursor on the current line.
 - Ctrl+H or Backspace: Delete the character before the cursor.
 - Alt+U: Capitalize every character from the cursor to the end of the current word, converting the characters to upper case.
 - Alt+L: Uncapitalize every character from the cursor to the end of the current word, converting the characters to lower case.


*Operators*
 - * 						() 
 - -						()
 - =						()
 - s 						()
 - b 						()
 - c 						()
 - p 						()
 - & 						()
 - ; 						()
 - && 						()
 - ||						()
 - $() 						()
 - |		 				()
 - >						()
 - >>						()
 - <						()
 - & (es. cmd &> file)		()