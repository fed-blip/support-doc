Іноді пам'ять на комп'ютері може повністю забитись, що буде заважати нормальній роботі поштомату. Подивитись скільки вільної пам'яті на SSD можна командою: 

`````bash
df -h /
`````

Якщо вільної пам'яті залишилось меньше 5-10 GB, то потрібно почистити логи:
`````bash
rm -rf /home/mint/snap/chromium/common/chromium/BrowserMetrics
`````

Почистити кеш хроміума:

`````bash
rm -rf /home/mint/snap/chromium/common/chromium/Cache
rm -rf /home/mint/snap/chromium/common/chromium/Code\ Cache
`````

Почистити snap-кеш:
`````bash
sudo rm -rf /var/lib/snapd/cache/*
`````

Видалити старі версії snap:
`````bash
sudo snap list --all | awk '/disabled/{print $1, $3}' | while read snap rev; do sudo snap remove "$snap" --revision="$rev"; done
`````

