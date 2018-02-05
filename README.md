Crypt0z integration/staging tree
================================

http://www.crypt0z.org

Copyright (c) 2009-2014 Bitcoin Developers
Copyright (c) 2011-2014 Crypt0z Developers

What is Crypt0z?
----------------

Crypt0z is a lite version of Bitcoin using scrypt as a proof-of-work algorithm for people to break by playing with it.
 - 2 minute block targets
 - subsidy halves... quite frequently..
 - ~25 million total coins
 - 620 coins per block
 - I think I set it over 5000 blocks to retarget difficulty

For more information, as well as an immediately useable, binary version of
the Crypt0z client sofware, see http://www.crypt0z.org.

License
-------

Crypt0z is released under the terms of the MIT license. See `COPYING` for more
information or see http://opensource.org/licenses/MIT.

Development process
-------------------

Developers work in their own trees, then submit pull requests when they think
their feature or bug fix is ready.

If it is a simple/trivial/non-controversial change, then one of the Crypt0z
development team members simply pulls it.

If it is a *more complicated or potentially controversial* change, then the patch
submitter will be asked to start a discussion with the devs and community.

The patch will be accepted if there is broad consensus that it is a good thing.
Developers should expect to rework and resubmit patches if the code doesn't
match the project's coding conventions (see `doc/coding.txt`) or are
controversial.

The `master` branch is regularly built and tested, but is not guaranteed to be
completely stable. [Tags](https://github.com/crypt0z-project/crypt0z/tags) are created
regularly to indicate new official, stable release versions of Crypt0z.

Testing
-------

Testing and code review is the bottleneck for development; we get more pull
requests than we can review and test. Please be patient and help out, and
remember this is a security-critical project where any mistake might cost people
lots of money.

### Automated Testing

Developers are strongly encouraged to write unit tests for new code, and to
submit new unit tests for old code.

Unit tests for the core code are in `src/test/`. To compile and run them:

    cd src; make -f makefile.unix test

Unit tests for the GUI code are in `src/qt/test/`. To compile and run them:

    qmake BITCOIN_QT_TEST=1 -o Makefile.test bitcoin-qt.pro
    make -f Makefile.test
    ./crypt0z-qt_test

