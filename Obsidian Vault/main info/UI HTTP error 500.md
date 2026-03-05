Якщо UI виглядає ось так:

![UI screenshot](Pasted image 20260212183603.png)

Це означає що файли `primary-key` биті, і їх потрібно видалити. 
Для цього підключаємось до поштомату, зупиняємо сервіс UI

`````bash
sudo systemctl stop DispatchHardware.UI
`````

Далі йдемо по цьому шляху `/opt/DispatchHardware/UI/temp-keys` і видаляємо всі файли в цій папці, після цього рестартуємо UI сервіс

`````bash
sudo systemctl restart DispatchHardware.UI
`````

Перевіряємо чи тема і сценарій запрацювали.

