参考　https://github.com/sighingnow/jekyll-gitbook


- テスト実行用のコンテナはビルド済

    参考：https://alpha3166.github.io/blog/20190413.html


- テスト実行時以下動かす
    ```
    docker run --rm -it -v "$PWD:/srv/src" -p 4000:4000 gh-pages
    ```
