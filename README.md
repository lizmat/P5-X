NAME
====

Raku port of Perl's -X built-ins

SYNOPSIS
========

    use P5-X; # exports -r -w -x -e -d -f -l -s -z

DESCRIPTION
===========

This module tries to mimic the behaviour of Perl's `-X` built-ins in Raku as closely as possible.

PORTING CAVEATS
===============

In future language versions of Raku, it will become impossible to access the `$_` variable of the caller's scope, because it will not have been marked as a dynamic variable. So please consider changing:

    -f;

to:

    -f $_;

AUTHOR
======

Elizabeth Mattijsen <liz@wenzperl.nl>

Source can be located at: https://github.com/lizmat/P5-X . Comments and Pull Requests are welcome.

COPYRIGHT AND LICENSE
=====================

Copyright 2018-2020 Elizabeth Mattijsen

Re-imagined from Perl as part of the CPAN Butterfly Plan.

This library is free software; you can redistribute it and/or modify it under the Artistic License 2.0.

