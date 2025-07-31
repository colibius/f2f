# f2f
Fortran 77 to Modern Fortran conversion script

f2f was originally written in about 2003, when I was in grad school, writing Fortran code for my thesis. I was too young to appreciate the syntax of Fortran 77, and too stubborn to just accept my fate. So I wanted to convert all the Fortran 77 code I had to use into Fortran 90. That's what prompted me to write this script, and I learned Perl to do it. At the time, Perl seemed to be the obvious language to use for this purpose (and might still be), and yet the other attempts to make conversion scripts were written in Fortran, if I recall. I think Fortran is a terrible language to use for translating a long chunk of text into a different chunk of text. Some years later, [Bob Apthorpe](https://github.com/apthorpe) rewrote my Perl code and sent it to me. Given that f2f was the first Perl script I had ever written, and his version just looked better, I figured it was probably better, and I just accepted his "pull request" without any testing (pull request in quotes because git did not even exist then). Even so, since it was essentially a complete rewrite, and since the version control at the time seemed particularly archaic and convoluted to me, I just kept them both and made both available. And since I don't have any other history of the code, I'll just post both of them here for historical purposes. Most likely you won't need the older version, but given that it was my first Perl script, it has a special place in my heart. There are no formal tests, and there are so many edge cases in Fortran 77 that it very well might not produce correct output for your very specific code. I've never actually seen it produce run-time bugs, only fairly obvious syntax errors that the compiler catches. But it has always been useful to me, when I needed it, and to some of you, too. So here it is.

# FORTRAN to Fortran

f2f is a Perl script which does much of the tedious work of converting FORTRAN 77 source code into modern Fortran. There seems to be a lot of Fortran hate in the world, and I think this comes from people who have been forced to use FORTRAN 77 at some time or another. Hopefully, this program will make you a less hateful person.

Download f2f.
USAGE:

> f2f [inputfile [outputfile]]

e.g.:

> f2f legacycode.f legacycode.f90

I wrote this program for my own needs, a long time ago, and I have successfully used it many times. It has generally worked well for me with standard FORTRAN 77 source code, but can sometimes give problems on mixed 77/90 code. I can’t guarantee it will spit out code that suits your aesthetic tastes, nor can I guarantee that it will generate code that compiles (you may need to make an edit or two first). In some cases it can generate really wacky code, especially if you feed it really wacky code. So I make no guarantees, but hopefully it makes your life easier rather than harder.
