# #KusoKoudoKaigi提出物の解説
## kuso.perl

### 実行例

`curl -sL 'https://raw.githubusercontent.com/Moffu360/kusokoudo-1/master/kuso.perl' | perl`

### 出力例

      % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                     Dload  Upload   Total   Spent    Left  Speed
      0     0    0     0    0     0      0      0 --:--:-- --:--:-- --:--:--     0curl: (6) Could not resolve host: sL
    100    15  100    15    0     0    126      0 --:--:-- --:--:-- --:--:--   405
    + 404: Not Found

### 中身

* perlとは名ばかりのsystem関数を用いシェェルスクリプト `jittai.sh` を呼び出します。

以下がコードです。

    #!/usr/bin/perl
    system("curl -sL 'https://raw.githubusercontent.com/Moffu360/kusokoudo-1/master/jittai.sh' | bash /dev/stdin");

## jittai.sh

### 中身

* `maim.sh`を呼び出します。
* curlのオプションが間違えていますが、それは些細なことです。

以下がコードです。

    #!/bin/sh
    #echo thisisgithubcontent

    curl sL "https://raw.githubusercontent.com/Moffu360/kusokoudo-1/master/maim.sh" | bash -x


## maim.sh

### 中身

* 現在は存在しませんが、コンテスト後に追加され、404は解消される予定です。
* 突然英語を使用しようとした結果、綴りを間違えます。

## あとがき

クソコードとは、現場ではえてしてコンテキストを含むと考えています。クソな内容自体が、技術的にシンプルでかつ面白くなかったとしても、コンテキストで面白いと思えるものがあるわけです。

本作品は、このコンテキストを重要視しています。具体的には、下記のようなクソポイントです。

* このクソコードを書いた人は「あれ、おかしいなあ実装したはずなんだけどなあ」と言い、納期を伸ばします。
* このクソコードは、ドキュメントだけは丁寧に作られます。
* このクソコードは、締め切りギリギリに送られます。

いかがでしたか？