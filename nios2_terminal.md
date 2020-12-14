## Nios 2 terminal
Trying to setup a simple "Hello world" in the DE0-nano board with a Nios 2 softcore it turns out that it works fine with
Quartus 13.1: I can create the project, uploaded into the board run the Nios II Software Build Tools for Eclipse create
the "Hello world" app, run it and see the output in the Nios console. I try the same using the 20.1 version and I can't
see the output in the Nios console, not only that but the Nios II Software Build Tools for Eclipse crashes after I try to
run the program.

The solution could be to just use the older version, and I was about to just do that when I found the ["Nios II
Command-Line Tools" documentation](!https://www.intel.com/content/dam/www/programmable/us/en/pdfs/literature/hb/nios2/edh_ed51004.pdf).
Ok, so... I can just call nios2-download to load the elf and nios2-terminal to see the terminal output. And it works!
I can finally see the "Hello world".

Upload the elf:

    nios2-download -g <file.elf>

Open the terminal:

    nios2-terminal

Then `Ctrl-C` to exit the terminal

You can also type into this terminal, but it doesn't echo what you type so you don't see what you are writting. Also each
character is send one by one, it doesn't wait for `Enter`. But that's not really a problem, actually it could be
something good depending on the application and it's definetely better than not seeing any input at all or a crash as 
it happens with the Nios II console built-in in the Nios II Software Build Tools.

For not that's all, I got what I wanted which was communicating with the Nios II core in the DE0-nano board,
but I would like to go into more deep to properly document what are those commands doing and then see if
I can generate the BSP and compile the software directly from the command line.
It would be great to avoid using GUI and have some script or Makefile that does everything for me.

[Home](index.md)
(I'm getting used to github pages, for now I'm using markdown as all I want is a fast way to document the things I do,
someday I might spend some time to see if I can customize the theme, put top or side bars with links, etc)
