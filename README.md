# NAME

epic

# USAGE

    epic [OPTION]... [FILE]...

# DESCRIPTION

    > type epic
    epic is epic

# OPTIONS

## CONDITIONALS

    -p, --pattern  must match pattern PATTERN
    -s, --size     image dimensions must equal SIZE
    -hd            short for -s 1920x1080

## ACTIONS

    -c,  --copy    copy FILEs to destination
    -m,  --move    move FILEs to destination
    -ex, --exec    exec COMMAND, with FILEs as its arguments
    -ev, --eval    perl code, inserted in a map expr: C<map { HERE } @_>

## OTHER STUFF

    -w,  --why     why did the files end up here?

    -h,  --help    show the help and exit
    -v,  --version display version info and exit
    -m,  --man     rtfm :)

# EXAMPLES

Print a list of HD images:

    epic -hd *

Print mtime and filename for each file matching pattern

    epic -p pattern -eval 'p scalar localtime +(stat($_))[9], " ", $_' *

Copy FILEs matching foobar OR fuubar, with a resolution of 1680x1050, to /tmp

    epic -p 'f[ou]{2}bar' -s 1680x1050 -copy  /tmp/ *

[stat(1)](http://man.he.net/man1/stat) HD images matching pattern:

    epic -p pattern -exec stat

# AUTHOR

    Magnus Woldrich
    CPAN ID: WOLDRICH
    m@japh.se
    http://japh.se

# REPORTING BUGS

Report bugs and/or feature requests on rt.cpan.org, the repository issue tracker
or directly to [m@japh.se](http://search.cpan.org/perldoc?m@japh.se)

# CONTRIBUTORS

None required yet.

# COPYRIGHT

Copyright 2011 __epic__s ["AUTHOR"](#AUTHOR) and ["CONTRIBUTORS"](#CONTRIBUTORS) as listed above.

# LICENSE

This program is free software; you can redistribute it and/or modify
it under the same terms as Perl itself.

# SEE ALSO

[stuff](http://github.com/trapd00r)