
Щоб перенести поштомат з одного середовища на інше, потрібно замінити 4 урла в appsetings.json.  Перед тим як міняти урли потрібно зупинити WebApi. 

Урли середовища на яке потрібно перенести поштомат можна знайти ось в цій [табличці](https://mintinnovations0-my.sharepoint.com/:x:/g/personal/rilyushyk_mint-innovations_com/EbU8ykIY0iVPgNQmHIuLFmQBbKnU29EpdWEGYH-KnIF-1A?wdOrigin=TEAMS-WEB.p2p_ns.rwc&wdExp=TEAMS-TREATMENT&wdhostclicktime=1762763631855&web=1&ovuser=87f432e5-0373-4d04-89ad-82289b8b79b0%2Cdzozulia%40mint-innovations.com&clickparams=eyJBcHBOYW1lIjoiVGVhbXMtRGVza3RvcCIsIkFwcFZlcnNpb24iOiI0OS8yNTExMDIwMjMxNSIsIkhhc0ZlZGVyYXRlZFVzZXIiOmZhbHNlfQ%3D%3D).  Урли потрібно замінити в трьох файлах:

- ```bash
  sudo nano /opt/DispatchHardware.Updater/appsettings.json
  ```
- ```bash
  sudo nano /opt/DispatchHardware/WebApi/appsettings.Production.json
  ```
- ```bash
  sudo nano /opt/DispatchHardware/Monitoring/appsettings.json
  ```


Замінити потрібно рядки які починаються з: 

- `"WebServerApiUrl":`
- `"PingWebSite":`
- `"MonitoringAPIUrl":`

Після заміни всіх урлів потрібно скопіювати GUID в апсетінгах WebAPi. Далі виконуємо хард ребут, переходим на середовище на яке перенесли поштомат, і шукаємо його там по скопійованому GUID, після переносу він завжди деактивований.