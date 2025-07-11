# Windows-ssh-copy-id
# Solution:
## PowerShell function
https://chrisjhart.com/Windows-10-ssh-copy-id/

```
# works: true
type $env:USERPROFILE\.ssh\id_rsa.pub | ssh {IP-ADDRESS-OR-FQDN} "cat >> .ssh/authorized_keys"
```

```
function ssh-copy-id($server) { type $env:USERPROFILE\.ssh\id_rsa.pub | ssh $server "mkdir -p ~/.ssh && chmod 700 ~/.ssh && cat >> ~/.ssh/authorized_keys && chmod 600 ~/.ssh/authorized_keys" }
```

# Solution.Alt
## Cygwin
https://superuser.com/questions/1747549/alternative-to-ssh-copy-id-on-windows
