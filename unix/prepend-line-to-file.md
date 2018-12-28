# Prepend line to file

To prepend a line to an existing file (such as a shebang) you can use the following snippet. Note that the existing file can not be used as output directly.

```bash
echo '#!/usr/bin/env node' | cat - existing.txt > new.txt
```
