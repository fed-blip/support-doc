Якщо є проблема з темою/сценрієм на поштоматі, по типу зїхала UI, спочатку потрібно спробувати перезавантажити сторінку, або перезавантажити поштомат, або перезастосувати сценарій, якщо це не допомогло, можна замінити фіайли зі сценарієм та темою:

1. Зупиняємо UI сервіс:
```bash
sudo systemctl stop DispatchHardware.UI.service
```

2. Переходимо в цю папку на поштоматі:
	`\opt\DispatchHardware\UI\wwwroot`

3. Заміняємо всі файли в ній на нові.

4. Надаємо доступ до нових файлів:
```bash
sudo chmod 777 /opt/DispatchHardware/UI/
```
 
5. Перезапускаємо UI сервіс:
```bash
sudo systemctl restart DispatchHardware.UI.service
```

--------------------------------------------------------------------

> [!tip] [File on OneDrive](https://mintinnovations0-my.sharepoint.com/my?id=%2Fpersonal%2Fdzozulia%5Fmint%2Dinnovations%5Fcom%2FDocuments%2Fsupport%20inst%2FUI%20file&viewid=62c09e8d%2D95f8%2D464c%2D9092%2Dda8374827445)