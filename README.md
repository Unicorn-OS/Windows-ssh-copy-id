# Windows-ssh-copy-id
# Solution:
## PowerShell function
https://chrisjhart.com/Windows-10-ssh-copy-id/#:~:text=At%20the%20moment%2C%20Windows%2010's,Linux%20device%20for%20passwordless%20login.
ark: http://web.archive.org/web/20250000000000*/https://chrisjhart.com/Windows-10-ssh-copy-id/

```
function ssh-copy-id($server) { type $env:USERPROFILE\.ssh\id_rsa.pub | ssh $server "mkdir -p ~/.ssh && chmod 700 ~/.ssh && cat >> ~/.ssh/authorized_keys && chmod 600 ~/.ssh/authorized_keys" }
```

# Solution.Alt
## Cygwin
https://superuser.com/questions/1747549/alternative-to-ssh-copy-id-on-windows
