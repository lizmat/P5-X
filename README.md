[![Actions Status](https://github.com/lizmat/P5-X/workflows/test/badge.svg)](https://github.com/lizmat/P5-X/actions)

NAME
====

Raku port of Perl's -X built-ins

SYNOPSIS
========

    use P5-X; # exports -r -w -x -e -d -f -l -s -z

DESCRIPTION
===========

This module tries to mimic the behaviour of Perl's `-X` built-ins as closely as possible in the Raku Programming Language.

PORTING CAVEATS
===============

In future language versions of Raku, it will become impossible to access the `$_` variable of the caller's scope, because it will not have been marked as a dynamic variable. So please consider changing:

    -f;

to:

    -f $_;

AUTHOR
======

Elizabeth Mattijsen <liz@raku.rocks>

Source can be located at: https://github.com/lizmat/P5-X . Comments and Pull Requests are welcome.

COPYRIGHT AND LICENSE
=====================

Copyright 2018, 2019, 2020, 2021 Elizabeth Mattijsen

Re-imagined from Perl as part of the CPAN Butterfly Plan.

This library is free software; you can redistribute it and/or modify it under the Artistic License 2.0.

