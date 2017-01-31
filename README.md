# The `extra` command for Unix text processing

Print the lines that are in any of the inputs.

Syntax:

    extra <input> ...

Example:

    $ extra 1.txt 2.txt
    => lines that are not in 1.txt, but are in 2.txt.


## Notes

The order doesn't matter.

In set theory, this command is (A extra B) a.k.a. (B - A).

This command is currently implemented using `awk` and POSIX.


## Related

Related commands for Unix text processing sets:

* [`union`](https://github.com/sixarm/union): print lines in (A union B)
* [`intersect`](https://github.com/sixarm/intersect): print lines in (A intersect B)
* [`except`](https://github.com/sixarm/except): print lines in (A except B) a.k.a. (A - B)
* [`extra`](https://github.com/sixarm/extra) : print lines in (A extra B) a.k.a. (B - A)

Examples:

    $ cat 1.txt
    alpha
    bravo

    $ cat 2.txt
    alpha
    charlie

    $ union 1.txt 2.txt
    alpha
    bravo
    charlie

    $ intersect 1.txt 2.txt
    alpha

    $ except 1.txt 2.txt
    bravo

    $ extra 1.txt 2.txt
    charlie


## Tracking

* Program: extra
* Version: 2.0.2
* Created: 2017-01-30
* Updated: 2017-01-30
* License: GPL
* Contact: Joel Parker Henderson (joel@joelparkerhenderson.com)
