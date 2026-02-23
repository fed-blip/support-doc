
Для перегляуд стріма з камери на поштоматі потрібно:

1. Встановлюємо собі на ноут vlc media player
2. Підключаємось до потрібно поштомату
3. Прокидаємо через Anydesk собі віддалений порт (6668 localhost 6666)
4. Виконуємо наступні команди на поштоматі
```bash
sudo apt update
```
```bash
sudo apt install vlc
```
5. Виконуємо команду в терміналі: 
```bash
/opt/DispatchHardware/WebApi/cvlc v4l2:///dev/video0 :v4l2-width=640 :v4l2-height=480 :v4l2-fps=30 --sout '#transcode{vcodec=h264,vb=800,acodec=none}:standard{access=http,mux=ts,dst=:6666}' 
```
 
6. Відкриваємо в себе vlc media player натискаємо Ctrl+N, вписуємо туди "http://localhost:6668" та натискаємо Enter