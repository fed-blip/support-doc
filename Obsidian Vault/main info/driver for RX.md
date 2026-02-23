# Драйвер CUPS для принтера **RX1131-H80** (Linux Mint)

> [!tip] [File on OneDrive](https://mintinnovations0-my.sharepoint.com/my?id=%2Fpersonal%2Fdzozulia%5Fmint%2Dinnovations%5Fcom%2FDocuments%2Fsupport%20inst%2FRX%20driver&viewid=62c09e8d%2D95f8%2D464c%2D9092%2Dda8374827445)

------------------------------------------------------------------------

##  Крок 1. Зупинити сервіс WebApi

``` bash
sudo systemctl stop DispatchHardware.WebApi.service
```

------------------------------------------------------------------------

##  Крок 2. Встановити CUPS та залежності

``` bash
sudo apt update
sudo apt install cups cups-filters cups-bsd printer-driver-gutenprint
sudo systemctl enable cups
sudo systemctl start cups
```

------------------------------------------------------------------------

##  Крок 3. Завантажити файли драйвера

-   Завантаж файли пакета **RX1131-H80**

-   Розпакуй у папку:

        /home/mint/Downloads/

Очікувана структура:

    /home/mint/Downloads/RX1131-H80/

------------------------------------------------------------------------

##  Крок 4. Встановити драйвер

1.  Відкрий термінал: **Ctrl + T**

2.  Перейди в папку з драйвером:

    ``` bash
    cd /home/mint/Downloads/RX1131-H80/
    ```

3.  Надати доступи до файлів:

    ``` bash
    sudo chmod 777 -R ./
    ```

4.  Дозволити виконання інсталяційного скрипта:

    ``` bash
    sudo chmod a+x ./install_cprastertocmd_to_system.sh
    ```

5.  Запустити встановлення драйвера:

    ``` bash
    sudo ./install_cprastertocmd_to_system.sh
    ```

6.  Скопіювати PPD-файл у системні каталоги CUPS:

    ``` bash
    sudo cp RX1131-H80.ppd /usr/share/cups/model/
    sudo cp RX1131-H80.ppd /etc/cups/ppd/
    ```

------------------------------------------------------------------------

##  Крок 5. Налаштувати принтер у CUPS

1.  Перезапусти CUPS:

    ``` bash
    sudo systemctl restart cups
    ```

2.  Відкрий у браузері:

        http://localhost:631

3.  Перейди у вкладку **Administration** → **Add Printer**

4.  Введи логін і пароль системи (Linux Mint)

5.  Обери принтер **RX1131-H80**

6.  Коли попросять драйвер --- обери файл:

        /home/mint/Downloads/RX1131-H80/RX1131-H80.ppd

7.  Натисни **Add Printer**

------------------------------------------------------------------------

##  Крок 6. Встановити додаткові залежності

``` bash
sudo apt install libusb-1.0-0-dev
sudo apt install mono-complete
```

------------------------------------------------------------------------

##  Крок 7. Запустити WebApi та перевірити друк

``` bash
sudo systemctl restart DispatchHardware.WebApi.service
```

------------------------------------------------------------------------


> [!Warning]
> Не забудь сконфігурувати на сервері (якщо використовується
> серверна частина).

