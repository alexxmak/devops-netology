1.
linux
![image](https://user-images.githubusercontent.com/44917492/147366953-788b4bce-4796-4b34-babd-946adcfcd994.png)

![image](https://user-images.githubusercontent.com/44917492/147366963-f2f48c68-2e93-4310-8892-b50239df6689.png)

![image](https://user-images.githubusercontent.com/44917492/147366976-37c656ef-ea6d-44bb-b53d-df2018a540e8.png)

windows
![image](https://user-images.githubusercontent.com/44917492/147366996-275c4d80-a562-4eba-9769-7a095c0549b9.png)

![image](https://user-images.githubusercontent.com/44917492/147367004-91030ee1-a872-4f52-abff-cfd5fbdf5148.png)

![image](https://user-images.githubusercontent.com/44917492/147367013-9131cf99-54f2-47b2-ba62-c003800b4a4d.png)

2. LLDP

3. пакет  VLAN
![image](https://user-images.githubusercontent.com/44917492/147367037-a3ee001d-6bd3-4efd-90f0-68504da3e7b1.png)

4.

Mode-0(balance-rr) – Данный режим используется по умолчанию. Balance-rr обеспечивается балансировку нагрузки и отказоустойчивость. В данном режиме сетевые пакеты отправляются “по кругу”, от первого интерфейса к последнему. Если выходят из строя интерфейсы, пакеты отправляются на остальные оставшиеся. Дополнительной настройки коммутатора не требуется при нахождении портов в одном коммутаторе. При разностных коммутаторах требуется дополнительная настройка.

Mode-1(active-backup) – Один из интерфейсов работает в активном режиме, остальные в ожидающем. При обнаружении проблемы на активном интерфейсе производится переключение на ожидающий интерфейс. Не требуется поддержки от коммутатора.

Mode-2(balance-xor) – Передача пакетов распределяется по типу входящего и исходящего трафика по формуле ((MAC src) XOR (MAC dest)) % число интерфейсов. Режим дает балансировку нагрузки и отказоустойчивость. Не требуется дополнительной настройки коммутатора/коммутаторов.

Mode-3(broadcast) – Происходит передача во все объединенные интерфейсы, тем самым обеспечивая отказоустойчивость. Рекомендуется только для использования MULTICAST трафика.

Mode-4(802.3ad) – динамическое объединение одинаковых портов. В данном режиме можно значительно увеличить пропускную способность входящего так и исходящего трафика. Для данного режима необходима поддержка и настройка коммутатора/коммутаторов.

Mode-5(balance-tlb) – Адаптивная балансировки нагрузки трафика. Входящий трафик получается только активным интерфейсом, исходящий распределяется в зависимости от текущей загрузки канала каждого интерфейса. Не требуется специальной поддержки и настройки коммутатора/коммутаторов.

Mode-6(balance-alb) – Адаптивная балансировка нагрузки. Отличается более совершенным алгоритмом балансировки нагрузки чем Mode-5). Обеспечивается балансировку нагрузки как исходящего так и входящего трафика. Не требуется специальной поддержки и настройки коммутатора/коммутаторов.


![image](https://user-images.githubusercontent.com/44917492/147367113-0c37e331-cf61-489e-bcf4-bd12e1413b82.png)



5.с маской /29 имеем 8 адресов (6 хостов)

6.

/29 = 8ip (6 хостов)

32 подсети

Диапазон правых байтов для сетевой маски 255.255.255.248:
0-7, 8-15, 16-23, 24-31, 32-39, 40-47, 48-55, 56-63,
64-71, 72-79, 80-87, 88-95, 96-103, 104-111, 112-119, 120-127,
128-135, 136-143, 144-151, 152-159, 160-167, 168-175, 176-183, 184-191,
192-199, 200-207, 208-215, 216-223, 224-231, 232-239, 240-247, 248-255

7. 100.64.0.0/26
