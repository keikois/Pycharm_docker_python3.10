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
