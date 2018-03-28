# ssh-copy-id

To put a public SSH key on a server you can login and paste the key or use the tool [ssh-copy-id](https://www.ssh.com/ssh/copy-id). It will login and copy your key (`id_rsa.pub` by default) to the `authorized_keys` file.

```bash
ssh-copy-id user@192.168.1.111
```