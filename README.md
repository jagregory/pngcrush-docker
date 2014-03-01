# pngcrush Docker container

[Docker](https://www.docker.io/) container for [pngcrush](http://pmt.sourceforge.net/pngcrush/). Has pngcrush set as the entrypoint.

```sh
docker run jagregory/pngcrush

 | pngcrush 1.7.9
 |    Copyright (C) 1998-2002,2006-2010 Glenn Randers-Pehrson
 |    Copyright (C) 2005      Greg Roelofs
 | This is a free, open-source program.  Permission is irrevocably
 | granted to everyone to use this version of pngcrush without
 | payment of any fee.
 | Executable name is pngcrush
```

A `/source` directory is created in the container, which can be mapped for use with relative file paths. pngcrush will always be run from the `/source` directory in the container.

```sh
docker run -v `pwd`:/source input.png output.png
```
