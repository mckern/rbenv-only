# rbenv-only

```
Run a command against specified installed ruby versions
    rbenv only -r <version> <command>
    rbenv only -r <version> -- <command --with --flags>

options:
    --help, -h:                      show this message
    --quiet, -q:                     quiet mode; don't print a header for each ruby
    --ruby <version>, -r <version>:  run <command> in ruby <version>
                                       (may be specified more than once)
```

## Installation

```shell
$ mkdir -p ~/.rbenv/plugins
$ cd ~/.rbenv/plugins
$ git clone https://github.com/rodreegez/rbenv-only.git
```

## Usage

```shell
$ rbenv only -r 2.6.3 -r 2.5.5 bundle exec rake
# Or, if your command has flags in it, use the double-dash
# convention that many GNU & BSD utilities support
$ rbenv only --ruby 2.6.3 -- gem --version
```

## Credits

This started life as a fork of [rbenv-only](https://github.com/mckern/rbenv-only), which was in turn mostly ripped off from [rbenv-each](https://github.com/chriseppstein/rbenv-each). It has been completely rewritten, but credit where credit is due.

## License

Unfortunately, [rbenv-only](https://github.com/mckern/rbenv-only) was unlicensed so licensing is questionable at best. My changes made as part of the rewrite are licensed under the Apache License, Version 2.0.
