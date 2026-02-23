
Для перегляду логів WebApi в реальному часі:

`````bash
sudo journalctl -fu DispatchHardware.WebApi
`````

Якщо потрібно подивитись логи за минулий час:
TIME - вказуєте число
minute/hour - потрібно вказати хвилини або години
`````bash
sudo journalctl -u DispatchHardware.WebApi --since "TIME minute/hour ago"
`````

Якщо потрібно подивитись лог після ребута:
INT - число ребутів ДО
`````bash
sudo journalctl -u DispatchHardware.WebApi.Service -b -INT
`````

Якщо потрібно подивитись коли заплановий хард ребут:
`````bash
cat /etc/crontab
`````

Якщо необхідно подивитись логи портів:
`````bash
sudo dmesg -w
`````
or
`````bash
sudo dmesg -T
`````

Якщо необіхдно глянути логи UI:
`````bash
sudo journalctl -fu DispatchHardware.UI.service
``````

Для перевірки підключених девайсів:
`````bash
sudo lsusb
`````
or
`````bash
 ls /dev/serial/by-id
`````