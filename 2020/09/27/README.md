## Sunday, September 27, 2020, 8:26:58PM EDT <1601252818>

TIL that this works to do regex substitution in Vim (technically `ex`):

```
:.s/\(\w\{1,\}\)/"\1",/ ::.s/\(\w\+\)/"\1",/
```

