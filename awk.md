#AWK
## Handy snippets

### Run awk script on file
```bash
awk -f script.awk input.txt
```


### Multiline match
Treat lines as fields
```bash
awk 'BEGIN {RS=""; FS="\n" }' input.txt
```