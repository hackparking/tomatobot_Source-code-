# Discord Bot

## 使い方

### 1. セットアップ
```sh
git clone https://github.com/あなたのGitHubユーザー名/discord-bot.git
cd discord-bot
pip install -r requirements.txt
```

## Renderにアクセス アカウント作成

https://render.com/

無料枠でok

Start Commandの欄に
```
python bot.py
```
に設定

トークンを入力

一度起動

## GASに登録
Google Apps scriptを検索

コードは
```
function keepBotAlive() {
    var url = "あなたのbot URL（Render）"; 
    var options = {
        "method": "get",
        "muteHttpExceptions": true
    };
    
    try {
        var response = UrlFetchApp.fetch(url, options);
        Logger.log("Ping sent: " + response.getResponseCode());
```
