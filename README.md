# lightnovel-labels

有名・一般ライトノベルレーベル、一部の新文芸レーベル、その他ライトノベル周辺ジャンルを多く刊行するレーベルの検索用リストです。

ライトノベルとそれ以外が混在しており刊行数におけるライトノベルの割合が低いレーベル、成人・女性・中高生向け専門レーベル、児童向けレーベル、BL専門レーベルなどは収録していません。

人力で収集しているため、すべてのレーベルは網羅していません。プルリクエストにて、条件に当てはまるにもかかわらず収録されていないレーベルの追加や、登録の誤りの修正等を歓迎しています。

## 活用例

blueskyで稼働している[新刊ラノベbot](https://bsky.app/profile/did:plc:jleb6zbvkqkl5c7c2kpm2vny)にて、全新刊書籍からのライトノベルの絞り込みに使用しています。

## 仕様

[`labels.json`](https://github.com/Hyz-sui/lightnovel-labels/blob/main/data/labels.json)にデータがあります。  
目grepのために概ねABCDあいうえお順で並べていますが、保証しません。

- `name`: 文字列。レーベルの名称。必須。  
    NDLやOpenBD等のデータで表記されている名称を優先的に使用しています。
- `alternatives`: 文字列の配列。レーベルの別名、表記ゆれ等のリスト。

[`labels.schema.json`](https://github.com/Hyz-sui/lightnovel-labels/blob/main/schema/labels.schema.json)にスキーマがあります。  
利用の際の型生成、`labels.json`の編集作業等に利用してください。

## Contributing

### データの追加・修正

`data/labels.json`を直接編集し、プルリクエストを送ってください。  

順番はABCDあいうえお順になるようにしてください。ひらがなとカタカナを区別せず、漢字やギリシャ文字等を含む場合は読み仮名で並べてください。

編集の際は、スキーマを登録するとエディタの入力候補等が利用でき、便利です。  
参考として、VSCodeの設定手順を示します。

1. ルートから見て`.vscode/settings.json`を作成します。
2. ファイルを編集して、以下の内容で保存します。

    ```json
    {
      "json.schemas": [
        {
          "fileMatch": ["labels.json"],
          "url": "./schema/labels.schema.json"
        }
      ]
    }
    ```

3. `labels.json`を開き、入力候補やプロパティの説明等が表示されることを確認します。

## License

MITライセンスです。
