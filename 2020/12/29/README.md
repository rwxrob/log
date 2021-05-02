## Tuesday, December 29, 2020, 1:19:22AM EST <1609222762>

TIL some cool Bash tricks.

To split a file on semicolon just turn it into an array after resetting
the IFS value for only that line:

```bash
IFS=\; fields=($line)
```

I also learned of a *really amazing* way to convert between base 16
(hexadecimal) and base 10.

```bash
local u=${fields[0]}
local v=$((16#$u))
```

I also need to remember the following:

* `shellcheck`
* <https://explainshell.com>

