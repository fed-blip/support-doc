
Для оновлення прошивки на принтері потрібно підключитись до поштомату, загрузити [файли](https://mintinnovations0-my.sharepoint.com/my?id=%2Fpersonal%2Fdzozulia%5Fmint%2Dinnovations%5Fcom%2FDocuments%2Fsupport%20inst%2Fprinter%20update%2F%D0%9F%D1%80%D0%BE%D1%88%D0%B8%D0%B2%D0%BA%D0%B0&viewid=62c09e8d%2D95f8%2D464c%2D9092%2Dda8374827445&login_hint=dzozulia%40mint%2Dinnovations%2Ecom&source=waffle) з прошивкою на поштомат, а саме в `\home\mint\Downloads`, після цього потрібно виконати наступні команди в терміналі:

`````bash
sudo systemctl stop DispatchHardware.WebApi.service
`````

`````bash
sudo chmod -R 777 /home/mint/Downloads
`````

`````bash
cd /home/mint/Downloads/K_Printer_Setting_Tool/
`````

`````bash
sudo ./KPOS_Linux_Setting_Tool_build.sh
`````

Після цього, відкриється вікно в якому потрібно натиснути "Set printer", далі вибрати шлях до файлу з прошивкою, після цього натиснути "Update", дочекавшись кінця апдейту потрібно зробити хард ребут на поштоматі.
