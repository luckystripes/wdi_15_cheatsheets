Command Line Cheatsheet

Basic Commands

$ ls -la (lists everything in dir and provides datestamp, and shows how large file is)

$ mkdir (make directory)

$ cat sampleFile (displays the content of the file to the screen)

$ less sampleFile (displays the content of the file to the screen)

$ cat sampleFile | less (displays your text by page, hit spacebar to go through pages)



VI Editor

"vi" sampleFile (to create and open a file to edit)

"i" (to insert yourself into edit mode, and start typing text)

"Esc" (to remove yourself from insert mode)

":wq" (write quick to save changes and exit sample file)



Killing a process

Top -c -d2 (shows real-time processes on your computer)

ps auwx | grep rails (list all rail processes by process id)

kill -9 processID ()