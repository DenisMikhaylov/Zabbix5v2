Добавление без агентового узла 

```
Host name: google.com
  interface agent: DNS google.com
  New group: External Hosts
```

```
Host name: ya.ru
  interface agent: DNS ya.ru
  New group: External Hosts
```



Простые проверки

```
Host: ya.ru
  Items 
    Name: check perf http
    Type: Simple check
    Key: net.tcp.service.perf[https]
    Type of information: Numeric (float)

```
```
Host: google.com
  Items 
    Name: check perf http
    Type: Simple check
    Key: net.tcp.service.perf[https]
    Type of information: Numeric (float)

```
```
Host: Zabbix
  Items
    Name: check ping
    Type: Simple check
    Key: icmpping[<Windows ip or DNS>]

```

```
Host: Zabbix
...
  Items
    Name: check rdp admin/host windows
    Type: Simple check
    Key: net.tcp.service[tcp,<Windows ip or DNS>,3389]
```

