из интересного: столкнулся с особенностью: если вошел в GitLab с помощью аккаунта GitHub,  и склонировал через https 
при попытке push запросится авторизация в аккаунте GitLab но использовать аккаунта гитхаба не получится, 
подкинул SSH ключ, прописал пуш по SSH git remote set-url origin git@github.com:username/repo.git
но push все равно не проходил (писал нет файлов).
Решилось клонированием через SSH, похоже клонировать по https, а пушить по ssh -- нельзя=)

ex.1
![image](https://user-images.githubusercontent.com/44917492/140533650-6a51871e-a2ca-4013-baff-654a83f6042b.png)
ex.2 
не понял как увидеть разницу между аннотированными и легковесными тегами в веб интерфейсе 
![image](https://user-images.githubusercontent.com/44917492/140538360-c26e36bb-be2e-47a9-af64-ec2df5204871.png)
![image](https://user-images.githubusercontent.com/44917492/140538436-677d3d9e-91b8-4b18-a9e5-7045fa4e6900.png)
![image](https://user-images.githubusercontent.com/44917492/140538471-8e23b6c5-bd7c-4c89-b11d-3a017b93ba89.png)
![image](https://user-images.githubusercontent.com/44917492/140539148-dba945d4-d52c-47ee-a6b7-ee65d058cda8.png)

оказывается, если добавляешь комментарий, тег автоматически становится аннотированным 
![image](https://user-images.githubusercontent.com/44917492/140539561-8d3c1f27-b372-4daa-b1da-7e2ce5d59101.png)
и тогда разница уже видна: в вебке нет автора данного тега, 
![image](https://user-images.githubusercontent.com/44917492/140539911-d959fff4-a110-4b6d-9938-853b435e17d8.png)
зато к нему можно добавить заметку к релизу и вполне себе вариант использования: релизы общие, помечать автора на них бессысленно (имхо)
![image](https://user-images.githubusercontent.com/44917492/140540305-1a898367-9cf2-47ae-9bc6-9920e721e7f3.png)


ex.3
![image](https://user-images.githubusercontent.com/44917492/140542297-470f7df0-4874-4d6a-af1c-f2526b8ef72f.png)
![image](https://user-images.githubusercontent.com/44917492/140544044-009c4eee-ea2f-427e-8325-b693b92c72b8.png)


ex.4
![image](https://user-images.githubusercontent.com/44917492/140546242-ee3a39fe-28be-4667-a545-1b8c28a125a2.png)


https://gitlab.com/alexxmak/devops-netology.git
https://github.com/alexxmak/devops-netology.git
https://alexxmak@bitbucket.org/alexxmak/devops-netology.git
