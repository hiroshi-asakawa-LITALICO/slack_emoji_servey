# slack_emoji_servey
絵文字使用率調査スクリプト(ruby)

### How to Use
- slackAppを作成して適切なpermissionを付与する
- slackAPIのtokenを取得する
- .envファイルを作成してtokenの値と投稿先チャンネル名を追記
- スクリプトを実行

### slackApp permission list
#### channels:history
View messages and other content in the user’s public channels

#### channels:read
View basic information about public channels in the workspace

#### chat:write
Send messages on the user’s behalf

#### emoji:read
View custom emoji in the workspace

#### reactions:read
View emoji reactions in the user’s channels and conversations and their associated content

#### users:read
View people in the workspace

### Settings
dotenvを導入してるので、.envファイルを作成して各々の環境に応じた値を追記してください

SLACK_API_TOKEN = your_token

POST_CHANNNEL_NAME = channel_name

### Run
$ ruby servey_emoji_ranking_bot.rb

### Please enter user or channnel
$ user

### Please enter user_name
$ hiroshi.asakawa

### Result
調査対象ユーザー or チャンネルにおける直近1000件の反応データを取得し、
絵文字使用率ランキング１~10位を算出して通知対象チャンネルに投稿する。



