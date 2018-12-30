# Specify credentials in file

Sometimes it's useful to not get prompted for the mysql password and not put it plain in the command. For example a cron job should not contain the plain passwords. To access a password protected database anyway you can use an option file.

Just put the following in `~/.my.cnf` (or other supported locations, check link):

```bash
[client]
password="MYSECUREPASSWORD"
```


## Resources

- [https://dev.mysql.com/doc/refman/8.0/en/option-files.html](https://dev.mysql.com/doc/refman/8.0/en/option-files.html)
