per - Simple unix permission viewer and converter
---
per is a simple utility that can verbosely print unix permissions and
convert between symbolic and numeric notations and vice-versa.

## Synopsis:
`per [OPTIONS] TARGET`

## OPTIONS
 - -S      Treat notations as special notations.
 - -v      Print permissions verbosely.
 - -n      Print permissions in a numeric notation.
 - -s      Print permissions in a symbolic notation.

Options may be chained (e.g. -vns). Providing no options defaults to -vns.
Providing only -S as an option defaults to -Svns.

TARGET may be:
  * A symbolic notation (e.g. rwxr-xr-x)
  * A numeric notation (e.g. 755)
  * A file (e.g. /etc/passwd)

If -S option is used, per will accept and print special notations (e.g.
rwsrwsrwT or 6775).

## Building
Build deps: GNU make

Run `make` (`gmake` on non-GNU systems) and wait a sec. The build will
produce a binary called `per` which you can copy to somewhere into
your `$PATH` (e.g `cp per /usr/sbin/`). Building works on OpenBSD, Artix
GNU/Linux, NixOS (thanks Legend!) and macOS (thanks grylem!) but should
also work on different systems (including different *BSDs). You can
also compile it by hand, it's c99.

Bugs report to the github repo.

Made by jarmuszz (jarmusz at tuta dot io).
