# 最新論文をGPTで要約してDiscordに通知してくれるBot（Nature Water）

## 参考にさせていただいたサイト・Github(ほぼ変更してない)

[Qiita](https://qiita.com/para-yama/items/bc4de2b26416ea8b419b)
[Github](https://github.com/pkohei/autojournalsummarizer/tree/main)

## 対象ジャーナル
[Nature Water](https://www.nature.com/natwater/)

## Dockerを利用した使用方法

Dockerfileと同階層に `.env`ファイルを作成する

### .envファイル
- **.envファイルの作成**
```bash
touch .env
```
- 確認
```bash
ls -l
ls -a           （macOS）
```

- **.envファイルの編集**
- Nanoエディタ
```bash
nano .env
```
- 環境変数の追加
```sh
OPENAI_API_KEY={your-api-key}
DISCORD_URL={your-webhook-url}
```
- 確認
```bash
cat .env
```


ビルド＆ラン

```bash
docker compose build
docker compose -f docker-compose.yml run --rm journalgpt python main.py
```


