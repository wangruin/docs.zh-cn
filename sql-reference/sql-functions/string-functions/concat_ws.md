# concat_ws

## description

### Syntax

`VARCHAR concat_ws(VARCHAR sep, VARCHAR str,...)`

使用第一个参数 sep 作为连接符，将第二个参数以及后续所有参数拼接成一个字符串。
如果分隔符是 NULL，返回 NULL。
`concat_ws`函数不会跳过空字符串，会跳过 NULL 值

## example

```Plain Text
MySQL > select concat_ws("or", "d", "is");
+----------------------------+
| concat_ws('or', 'd', 'is') |
+----------------------------+
| starrocks                      |
+----------------------------+

MySQL > select concat_ws(NULL, "d", "is");
+----------------------------+
| concat_ws(NULL, 'd', 'is') |
+----------------------------+
| NULL                       |
+----------------------------+

MySQL > select concat_ws("or", "d", NULL,"is");
+---------------------------------+
| concat_ws("or", "d", NULL,"is") |
+---------------------------------+
| starrocks                           |
+---------------------------------+
```

## keyword

CONCAT_WS,CONCAT,WS
