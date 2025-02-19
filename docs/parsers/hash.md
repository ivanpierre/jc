[Home](https://kellyjonbrazil.github.io/jc/)
<a id="jc.parsers.hash"></a>

# jc.parsers.hash

jc - JSON CLI output utility `hash` command output parser

Usage (cli):

    $ hash | jc --hash

Usage (module):

    import jc
    result = jc.parse('hash', hash_command_output)

    or

    import jc.parsers.hash
    result = jc.parsers.hash.parse(hash_command_output)

Schema:

    [
      {
        "command":       string,
        "hits":          integer
      }
    ]

Examples:

    $ hash | jc --hash -p
    [
      {
        "hits": 2,
        "command": "/bin/cat"
      },
      {
        "hits": 1,
        "command": "/bin/ls"
      }
    ]

<a id="jc.parsers.hash.parse"></a>

### parse

```python
def parse(data, raw=False, quiet=False)
```

Main text parsing function

Parameters:

    data:        (string)  text data to parse
    raw:         (boolean) unprocessed output if True
    quiet:       (boolean) suppress warning messages if True

Returns:

    List of Dictionaries. Raw or processed structured data.

### Parser Information
Compatibility:  linux, darwin, cygwin, aix, freebsd

Version 1.3 by Kelly Brazil (kellyjonbrazil@gmail.com)
