# インストール手順
## 1. homebrew
```
brew install gradle
```

- 上記コマンドで、ダウンロード+解答

ログ。
```
==> openjdk
For the system Java wrappers to find this JDK, symlink it with
  sudo ln -sfn /usr/local/opt/openjdk/libexec/openjdk.jdk /Library/Java/JavaVirtualMachines/openjdk.jdk

openjdk is keg-only, which means it was not symlinked into /usr/local,
because macOS provides similar software and installing this software in
parallel can cause all kinds of trouble.

If you need to have openjdk first in your PATH, run:
  echo 'export PATH="/usr/local/opt/openjdk/bin:$PATH"' >> /Users/satouriho/.bash_profile

For compilers to find openjdk you may need to set:
  export CPPFLAGS="-I/usr/local/opt/openjdk/include"
```

## 2. 手動インストール
- 仕事でGradleのバージョン指定されているならこちらを利用する方が良さそう。
- 手順割愛。詳細は以下URL  
https://gradle.org/install/#manually

# その他
- 詳細は各PJのREADME.mdを参照
- Gradleのチュートリアルにて参照するURL
  https://docs.gradle.org/current/samples/index.html#java
- 後で読むリスト
  - Gradleの特徴5つ
    https://docs.gradle.org/current/userguide/what_is_gradle.html#five_things
