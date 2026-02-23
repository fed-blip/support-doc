
Перервірити чи база заблокована можна переглянувши лог WebApi на самому поштоматі ([[investagion webApi logs]]), якщо в логові є рядок "database is locked", то база заблокована, для розблокування потрібно зробити наступне:

1. Завантажте на поштомат ці [файли](https://mintinnovations0-my.sharepoint.com/my?id=%2Fpersonal%2Fdzozulia%5Fmint%2Dinnovations%5Fcom%2FDocuments%2Fsupport%20inst%2Fbd%20unlock&viewid=62c09e8d%2D95f8%2D464c%2D9092%2Dda8374827445&login_hint=dzozulia%40mint%2Dinnovations%2Ecom&source=waffle) 
2. Оновлюємо пакети на поштоматі
```bash
 sudo apt update
```
3. По черзі вставляємо команди: 
```bash
sudo apt -o Acquire::Check-Valid-Until=false install sqlite3
```
   
```bash
sudo systemctl stop DispatchHardware.WebApi.service
```
    
```bash
sudo sqlite3 /opt/DispatchHardware/WebApi/BasicStructure_DBSQLite.db < /home/mint/Documents/fixDbLock.sql
```
      
```bash
sudo sqlite3 /opt/DispatchHardware/WebApi/BasicStructure_DBSQLite.db < /home/mint/Documents/fixDeviceSettings.sql
```
     
```bash
sudo systemctl restart DispatchHardware.WebApi.service
```
      
4. Дивимось по логах чи база розблокувалась
5. Робимо хард ребут