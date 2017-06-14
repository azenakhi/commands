## Send an e-mail with the telnet command to test the configuration of an SMTP server.

### Syntax
```
telnet smtp-server.domain.net 25
  helo test.domain.com
  mail from: <test@example.com>
  rcpt to: <youruser@yourdomain.com>
  data
  subject: test seveur smtp
 <Type the desired content, press Enter, then put a dot (.), Then enter to exit>
```
### Test
```
> telnet smtp-server.domain.net 25
Trying 127.0.0.1...
Connected to smtp-server.domain.com.
Escape character is '^]'.
220 infmsg5f2.localdomain ESMTP Postfix
helo test.com
250 infmsg5f2.localdomain
mail from: <test.comain.com>
250 2.1.0 Ok
rcpt to: <loginuser@domain.net>
250 2.1.5 Ok
data
354 End data with <CR><LF>.<CR><LF>
subject: test smtp server
hello world
.
250 2.0.0 Ok: queued as 5DE2137C056
quit
```
