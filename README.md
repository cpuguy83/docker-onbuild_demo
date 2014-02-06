## Docker ONBUILD builder instruction demo
This is a little demo I through together to demonstrate Docker's new build instruction, ONBUILD.<br />
I probably went a little overboard with the ONBUILD instructions, it really only needs to contain the ADD line, however I wanted to demonstrate just how powerful (and maybe freighteningly so) ONBUILD can be.

This demo sets up Ruby in a base image, then uses ONBUILD to tell any other image that uses this base image as a parent to also perform the given operations before running anything else it's buildfile.  In this example, it's adding my skeleton Rails app, installs all them gem dependencies, and even sets a CMD to use.<br />
In reality you'll probably just want to use the ADD line in an ONBUILD, but it's certainly not limited to that!
