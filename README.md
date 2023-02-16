---
description: >-
  以下对SQLAlchemy简称SA，网上的中文教程多为1.3版本的，而且个人觉得1.3的语句更加与Django的相似，但pandas的to_sql要求1.4以上版本，最终使用了1.4.46版本。
layout: landing
---

# Tutorial One

```python
# 安装1.3版本
pip install sqlalchemy==1.4.46
```

{% hint style="info" %}
官方文档网址：[https://docs.sqlalchemy.org/en/13/index.html](https://docs.sqlalchemy.org/en/13/index.html)

_以下对SQLAlchemy简称SA_
{% endhint %}

SQLite允许在内存中的DB，在SA中用如下命令：

```python
from sqlalchemy import create_engine
engine = create_engine('sqlite:///:memory:', echo=True)  # echo用于输出SA的指令以及DB的报错等
# 这里可以指定指定DB的驱动，这里用了pysqlite，不指定，则用默认的DBAPI
 engine = create_engine("sqlite+pysqlite:///:memory:", echo=True)
```

