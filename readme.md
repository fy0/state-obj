# State Object

Tested on py2.7/py3.4

```python
from state_obj import StateObject

class MyState(StateObject):
    DEL = 0
    HIDE = 10
    CLOSE = 30 # 禁止回复
    NORMAL = 50

    txt = {DEL: "删除", HIDE: "隐藏", CLOSE:"关闭", NORMAL:"正常"}


MyState.init()

print(list(MyState.keys()))
>>>> ['DEL', 'HIDE', 'CLOSE', 'NORMAL']

print(list(MyState.values()))
>>>> [0, 10, 30, 50]

print(list(MyState.items()))
>>>> [('DEL', 0), ('HIDE', 10), ('CLOSE', 30), ('NORMAL', 50)]

print(list(MyState.v2k.items()))
>>>> [(0, 'DEL'), (10, 'HIDE'), (30, 'CLOSE'), (50, 'NORMAL')]

print([MyState.get_txt(x) for x in MyState.values()])
>>>> ['删除', '隐藏', '关闭', '正常']

```
