## Saturday, March 27, 2021, 2:06:58PM EDT <1616868418>

```bash
#!/bin/bash

#pandoc -s README.md  -o index.html --template assets/template.html

for md in **/README.md; do
  dir=$(dirname $md )
  echo Building $md
  pandoc -s "${md}"  -o "${dir}"/index.html --template assets/template.html \
    2>/dev/null
done
```
