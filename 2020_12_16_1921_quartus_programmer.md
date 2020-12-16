## Quartus programmer from command line
[Home](index.md)

Today I wanted to run some test on the FPGA, I tried to load the software and I couldn't. No
Nios core was detected on the FPGA. Of course not, I haven't programmed the FPGA! Then I was
about to open the Quartus Programmer to load the sof file but... Wait! Why don't I do it from
the command line, I already load the software from the command line so why not load the FPGA
configuration too?
"
The Quartus Programmer can be used from the command line using `quartus_pgm`.
To check for the different options you can run:
    quartus_pgm --help

Now to program the FPGA throught the JTAG chain we specify the programming mode using `-m JTAG` and choose the
file with `-o "p;file.sof"`.
    quartus_pgm -m JTAG -o "p;<path_to_file>/file.sof"

## Reference
http://billauer.co.il/blog/2018/08/altera-intel-fpga-command-line-jtag/
