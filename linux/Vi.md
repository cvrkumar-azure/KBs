# Vi/Vim

vi/vim is  one of the most extensible and customizable and also difficult to learn.


vi has three modes

1. Command Mode - The default mode when you open vi/vim.
2. Insert Mode  - This mode is to edit text Press `i` to enter insert mode.
3. Visual Mode  - This mode will help you in selecting text. Press `v` to enter Visual mode



To enter command mode, press `esc` key on your keyboard.
In command mode you cannot edit and in Insert mode you cannot execute a command.

## Some Commands
:w      	--> Write changes meaning save the file

:q      	--> Quit the vi editor

:wq         --> Save and edit

:q!         --> exit without saving the recent changes

dd      	--> Deletes a line

ndd         --> deletes n no. of lines (where n is intezer greater than 0)

y       	--> yank / copy

nyy         --> yanks n no. of lines (where n is intezer greater than 0)

p       	--> Paste

u       	--> undo

ctrl+r  	--> redo

shift+g     --> Takes to the bottom of the page

gg      	--> Takes to the top of the page

:set number --> View line numbers

:n          --> Takes you to the nth line.

/string-to-search 	--> To search for a string

:s/string-to-search/string-to-replace/g  --> Searches string and replaces wiht the replacement on current line
Ex: :s/tect/text/g


:%s/string-to-search/string-to-replace/g  --> Searches string and replaces wiht the replacement through out the file

:set number            --> Sets the Line numbers
