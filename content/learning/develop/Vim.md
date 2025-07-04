# Vim でたまに使う便利な操作

### 検索
* 先頭から空白が連続して続く文字列
```sh
/^ \+       # 空白が１つ以上
/^ \{2, }   # 空白が２つ以上
```

### 比較
* 複数のファイルを開いて比較
```sh
vimdiff file1.txt file2.txt
vim -d file1.txt file2.txt
```

* 今開いているファイルを比較する。
```sh
# 現在のタブで開いているファイルをまとめて比較
:windo diffthis  # diffモードをON
:windo diffoff   # diffモードをOFF

# 個別にdiffモードをONにする方法 (現在のペインで表示しているファイル)
#   ペインの移動は 'Ctrl + w' -> 'h/j/k/l'
:diffthis        # diff ON
:diffoff         # diff OFF
```
