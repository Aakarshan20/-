```
crontab -e
```

```

* * * * * /usr/local/bin/kill_kinsing_and_kdevtmpfsi.sh
```

```
vim  kill_kinsing_and_kdevtmpfsi.sh

```

```
#!/bin/bash

ps aux | grep kinsing | awk '{print $2}' | xargs -I {} kill -9 {}
ps aux | grep kdevtmpfsi | awk '{print $2}' | xargs -I {} kill -9 {}
```
```
cp kill_kinsing_and_kdevtmpfsi.sh /usr/local/bin/kill_kinsing_and_kdevtmpfsi.sh
```