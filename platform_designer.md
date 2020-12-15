## Schrödinger PLL
Let's start with a mysterious thing, in Quartus 20.1 I can't instantiate a PLL in the Platform Designer. I can add it,
configure it and then when the configuration is done and I click finish to close the configuration window... Puff! it
dissapears. The weird thing is that yesterday it worked and I could instantiate it (though I didn't test if it actually
worke).

As far as I know, I haven't changed anything related to Quartus or Platform Design so I'm lost and don't know why
something that worked once it is no longer working.

A possible workaround could be to manually instantiate the PLL, with or without the help of the MegaWizard IP manager
(I don't remember the exact name but it's something like that, which makes sense because this weird magic must come
from somewhere) which can be used to create a wrapper.
Another solution is to use Quartus 13.1. Seriously maybe I should just use that version.

For now I gave up and used the on-borad 50 MHz reference clock.
