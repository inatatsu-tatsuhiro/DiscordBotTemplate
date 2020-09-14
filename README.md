# DiscordBot Docker Template

# 使い方
exampleディレクトリは任意のディレクトリ名としてください。
```
$ mkdir example 
$ cd example 
$ git clone https://github.com/inatatsu-tatsuhiro/DiscordBotTemplate .
```
`./docker/Dockerfile`の環境変数`DISCORD_TOKEN`に取得したAPI Takenを入力し他のちにBuildする。

```
$ docker-compose build
```
`python`ディレクトリ以下にDiscordBot開発を行う

osモジュールをインポートし、`os.environ["DISCORD_TOKEN"]`でtokenへのアクセスが可能である。

ex) トークンの読み込み例
```
bot.run(os.environ["DISCORD_TOKEN"])
```

