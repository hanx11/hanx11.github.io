+++
title = 'Python Regex Example'
date = 2023-09-26T18:29:23+08:00
draft = true
+++

## Python 正则表达式示例

#### 从文本中提取JSON格式字典

```python

import re
import json

s = '''[2023-04-19 10:18:36,070] [73709] [INFO] {"request": "GET /hello/?format=json HTTP/1.1", "status": "200", "bytes": "30", "remote_address": "127.0.0.1","duration": "0.883924", "referer": "-", "agent": "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/112.0.0.0 Safari/537.36"}'''

pattern = r"{.+[:,].+}"

items = re.findall(pattern, s)

for item in items:
    print(json.loads(items))

```

