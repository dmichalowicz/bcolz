===============================================================
 Announcing c-blosc 1.9.3
 A blocking, shuffling and lossless compression library for C
===============================================================

What is new?
============

This is a maintenance release for reverting a mistake introduced in
1.7.1. At that time, bit-shuffling was enabled for typesize == 1 (i.e.
strings), but the change also included byte-shuffling accidentally. This
only affected performance, but in a quite bad way (a copy was needed).
This has been fixed and byte-shuffling is not active anymore when
typesize == 1.

For more info, please see the release notes in:

https://github.com/Blosc/c-blosc/blob/master/RELEASE_NOTES.rst


What is it?
===========

Blosc (http://www.blosc.org) is a high performance meta-compressor
optimized for binary data.  It has been designed to transmit data to
the processor cache faster than the traditional, non-compressed,
direct memory fetch approach via a memcpy() OS call.

Blosc has internal support for different compressors like its internal
BloscLZ, but also LZ4, LZ4HC, Snappy and Zlib.  This way these can
automatically leverage the multithreading and pre-filtering
(shuffling) capabilities that comes with Blosc.


Download sources
================

Please go to main web site:

http://www.blosc.org/

and proceed from there.  The github repository is over here:

https://github.com/Blosc

Blosc is distributed using the MIT license, see LICENSES/BLOSC.txt for
details.


Mailing list
============

There is an official Blosc mailing list at:

blosc@googlegroups.com
http://groups.google.es/group/blosc


Enjoy Data!

