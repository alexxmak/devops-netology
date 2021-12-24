1.
![image](https://user-images.githubusercontent.com/44917492/147366724-12dc31c1-108a-4663-8ecf-09e830df040d.png)

2.
Первым получили 307 Internal Redirect (временное перенаправление на https://stackoverflow.com/) –Сейчас у Chrome политиками безопасности идет перенаправление по умолчанию на протокол https , и собственно первым «ловится» запрос  инициированный политиками безопасностями.

Второй запрос кидает нам  200 код и отдает нам как раз таки тело сайта но расположенного по https. Выполнялся дольше всех как раз он

![image](https://user-images.githubusercontent.com/44917492/147366765-a3f1f22f-e7af-4d2a-9475-e3a13f580a94.png)

Если вдаваться в подробности то, время затрачено на 
![image](https://user-images.githubusercontent.com/44917492/147366789-d543afba-cb7b-4bca-8e88-4fb91dbb9aeb.png)

![image](https://user-images.githubusercontent.com/44917492/147366795-1895227e-6665-4cac-be4e-5c8129385b54.png)

3.
![image](https://user-images.githubusercontent.com/44917492/147366807-98977fdc-9fba-4236-9ad4-49c2f780cf16.png)

4.
![image](https://user-images.githubusercontent.com/44917492/147366821-fad2088d-88bf-4154-865d-d5a0710c9644.png)

5.
С виртуалки не показывает дальше основного компьютера, но смотрел бы такой командой

![image](https://user-images.githubusercontent.com/44917492/147366830-31520cc0-56c4-492e-89fe-c3ad176397f1.png)

6.
![image](https://user-images.githubusercontent.com/44917492/147366848-b1ad9245-e5da-44a2-8a23-dd4c4d53d22f.png)

7 and 8.
dig +trace @8.8.8.8 dns.google +all

![image](https://user-images.githubusercontent.com/44917492/147366868-75d7961d-a422-407d-837b-e942ed8e07c3.png)
