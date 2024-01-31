## nginxの設定ファイル
設定ファイルは/etc/nginx/conf.dディレクトリの中にある
デフォルトではその中にdafault.confファイルがある


default.confの中身
server {
    location / {
        root /usr/share/nginx/html  //ここがviewファイルの格納場所
        index index.html index.html //このindexファイルがデフォルトで表示される設定になっている　index.htmlが第一希望 index.htmlが第二希望だと思われる　二つ指定しないとエラーがでる
    }
}

## コマンド
`docker build -t イメージ名 .` .はどこのDockerfileを参照するのかを表す
`docker run -d --name コンテナ名 -p 80:80 nginx` 左の80はlocalhost:の後の番号
