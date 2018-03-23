# Redirection append vs overwrite

To write content to a file in bash you can either overwrite or append it by using the redirection operator.

```bash
# overwrites content
echo "hello world" > foo.txt

# appends to existing content
echo "hello world" >> foo.txt
```
