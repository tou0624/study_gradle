# チュートリアル
https://docs.gradle.org/current/samples/sample_building_java_applications.html

- 初期化(このコマンドを打つとプロジェクトが出来上がる)
```
gradle init
```

- サンプルのJavaクラス実行
```
./gradlew run
```
  - app/build.propertiesにて「application」として定義されているクラスのMainクラスを実行してくれる。
    - 自分でコンパイル→実行する必要がなくてらく。

- ビルドする
```
./gradlew build
```
  - ビルドした結果できあがるもの
    ```
    app/build/distributions/app.tar
    app/build/distributions/app.zip
    app/build/libs/app.jar
    ```

- ビルドの過程を見れる。
  - 閲覧の流れ
    - `--scan`オプションをつけてビルドし、表示されたURLへアクセス。
      ```
      ./gradlew build --scan

      BUILD SUCCESSFUL in 6s
      7 actionable tasks: 7 up-to-date

      Publishing a build scan to scans.gradle.com requires accepting the Gradle Terms of Service defined at https://gradle.com/terms-of-service. Do you accept these terms? [yes, no] yes

      Gradle Terms of Service accepted.

      Publishing build scan...
      https://gradle.com/s/(ハッシュ値のURL)
      ```

    - URLアクセス後、メールアドレスを入力する画面が出てくるので、メールアドレス入力。

    - メールアドレス入力後、来たメールのリンクを押下。

  - タスクの詳細。ビルドする前にテストしてくれるので、内容が想定した動作ではない場合も検知できる。らくちん！
    ```
    :app:compileJavaUP-TO-DATE	0.027s
    :app:testUP-TO-DATE	0.011s
    :app:compileTestJavaUP-TO-DATE	0.010s
    :app:startScriptsUP-TO-DATE	0.006s
    :app:distTarUP-TO-DATE	0.005s
    :app:distZipUP-TO-DATE	0.004s	    
    ```

# おまけ
## GradleWrapper(gradlewなど)
- https://docs.gradle.org/7.0/userguide/gradle_wrapper.html
