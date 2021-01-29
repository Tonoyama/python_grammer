# `if __name__ == '__main__':` の働き
## ↑を書いているファイル自身が実行されない限り、下に書いてある処理は実行されない
例：

```shell
python3 module.py
```

`module.py`
```python
def func():
    print('Hello!')

if __name__ == '__main__':
    print("Good!")
    func()
```
ファイル自身が実行されると`if __name__ == '__main__':`以下の処理が実行される。

`output`
```
Good!
Hello!
```

`if __name__ == '__main__':`を定義していない他のファイルから呼び出されても`if __name__ == '__main__':`以下の処理は実行されない。

```python
import module

module.func()
```
`output`
```
Hello!
```