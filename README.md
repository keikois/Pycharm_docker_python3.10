# Pycharm_docker_python3.10
PycharmとdockerでPython3.10開発環境を構築
```
Pycharm_docker_python3.10
├── docker 
│     ├ Dockerfile
│     └ docker-compose.yml
│ 
├── hello.py
│           
└── requirements.txt
```
## Pythonの起動方法
カレンとディレクトリを、Pycharm_docker_python3.10下のdockerに移動
```
cd Pycharm_docker_python3.10
cd docker
```
下記コマンドを実行すると、コンテナを生成します。

ビルドコンテキストは、Pycharm_docker_python3.10ディレクトリです。
```
docker-compose up -d --build
```
## 実行方法
下記コマンドで、コンテナに入ります。
```
docker exec -it python3.10 bash 
```
pythonファイルを実行します。
```
python hello.py
```
hello worldが表示されたら、実行できています。

# Pycharmの設定
コンテナを起動後、
pythonインタープリター（Pycharm右下）を

*Remote Python 3.10.5 Docker(python:3.10)*

に設定すると
dockerで作成したpythonでコードを実行できます。

## pycharmで、コンテナに入る方法
画面下、真ん中より少し右にある

- *サービス*

をクリック。

- Docker > Docker-compose: docker > app > python3.10

のpython3.10を右クリックする。

- Execを選択
- 作成と実行・・・を選択
- コマンド：に
```
/bin/bash
```
と入力すると、新しいタブに
- 実行：/bin/bash

が作成される。

このタブで、pythonファイルを実行できる。
