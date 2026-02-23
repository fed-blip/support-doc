## Драйвер CUPS для принтера **TPTCM112III**

> [!tip] [File on OneDrive](https://mintinnovations0-my.sharepoint.com/my?id=%2Fpersonal%2Fdzozulia%5Fmint%2Dinnovations%5Fcom%2FDocuments%2Fsupport%20inst%2FCUSTOM%20driver&viewid=62c09e8d%2D95f8%2D464c%2D9092%2Dda8374827445).

------------------------------------------------------------------------

##  Опис пакета

Цей пакет містить драйвер принтера для CUPS та необхідні файли:

-    Скомпільований драйвер для принтера **TPTCM112III**
    -   `rastertotptcm112iii`
-    Файл налаштувань та довідки параметрів друку (PPD)
    -   `TPTCM112III.ppd.gz`
-    Скрипт встановлення драйвера та PPD-файлу

------------------------------------------------------------------------

##  Вимоги

Для роботи цього програмного забезпечення на комп'ютері має бути
встановлений:

-   **CUPS сервер та його архітектура**\
    https://www.cups.org

------------------------------------------------------------------------

##  Інструкція з встановлення

1.  Відкрий термінал (bash або інший shell).

2.  Виконай команду:

    ```bash
    ./setup
    ```

3.  Перейди в браузері на:

        http://localhost:631

4.  Додай нову чергу друку для своєї моделі принтера.

5.  Надрукуй тестову сторінку та перевір результат.

------------------------------------------------------------------------

##  Налаштування драйвера

###  1. Page Sizes:
   - 112mm * 85mm
   - 112mm * 125mm
   - 112mm * 185mm
   - 112mm * 245mm
   - 112mm Roll
   - ZOOM 112mm * 85mm
   - ZOOM 112mm * 125mm
   - ZOOM 112mm * 185mm
   - ZOOM 112mm * 245mm
   - ZOOM 112mm Roll
   `the default page is 112mm * 125mm`

###  2.  Halftoning Algorithm:
  - Accurate
  - Radial
  - WTS
  - Standard

###  3.  Printer Quality:
   - High Quality
   - Normal
   - HighSpeed
   `the default is normal`


###  4. Print Density:
   - -25%
   - -12%
   - 0%
   - +12%
   - +25%
   `the default is 0%`

###  5.  Paper presentation:
   - 21 mm
   - 35 mm
   - 48 mm
   - 62 mm
   `the default value is 21 mm`

###  6.  Black Mark Alignement
   - Off
   - On
   `the default value is Off`

###  7.  Cut Type:
   - Total Cut End Page and Recovery
   - Total Cut End Page Without Recovery
   - Total Cut End Doc and Recovery
   - Total Cut End Doc Without Recovery
   `the default is Total Cut End Page and Recovery`