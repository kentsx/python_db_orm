---
description: 整个SA学习过程结合了自己编写的一个项目，并以SQLite为数据库
---

# 建立engine

**SQLite允许在内存中的DB，在SA中用如下命令：**

```python
from sqlalchemy import create_engine
engine = create_engine('sqlite:///:memory:', echo=True)  # echo用于输出SA的指令以及DB的报错等
# 这里可以指定指定DB的驱动，这里用了pysqlite，不指定，则用默认的DBAPI
 engine = create_engine("sqlite+pysqlite:///:memory:", echo=True)
```

这个时候其实还没有正在创建数据库，只是建立了一个engine而已。

{% hint style="info" %}
后面的学习会比较跳跃，我是以读取一个金融网页并抓取数据的一个客户端为基础，进行学习了SA。
{% endhint %}
