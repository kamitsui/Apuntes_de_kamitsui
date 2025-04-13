# C++ Getting Start

C言語の学習を経て、C++98を学ぶために調べたことをまとめる記事です。

## イントロ

### 主要概念

#### オブジェクト指向プログラミング（Object Oriented Programming : OOP）
> データ (属性) と動作 (メソッド) 　→　カプセル化　「オブジェクト」
>
> クラスとオブジェクト：設計図（クラスの定義方法）
>
> カプセル化：クラス内のデータと実装
>
> 継承：既存のクラスし、コードの再利用
>
> ポリモーフィズム：異なるクラスのオブジェクトを共通タイプのオブジェクトとして扱うことを可能にします。

---

#### C++固有の構文と機能

##### iostream (入出力ストリーム) : `cin`, `cout`
scanfやprintfは使わなくなる。
```cpp
#include <iostream>

int main() {
    int number;
    std::cout << "Enter a number: ";
    std::cin >> number;
    std::cout << "You entered: " << number << std::endl;
    return 0;
}
```

実行結果
```

```

```cpp
    std::cin >> str;
        std::cout << "You entered: " << str << std::endl;
```



Reference


* 標準テンプレートライブラリ（Standard Template Library : STL）

### CPP Module 課題との関係性

* C++構文、OOP概念、STLや例外処理
* クラスの設計と実装、コンテナとアルゴリズムの使用、メモリ管理
* コーディング方法？を学習し、クリーンかつ適切に記述されたコードの重要性

### 

