## 概要
`tracking_records`は、指定されたデータベース内の全テーブルに対して、指定された日時以降に作成されたレコードの数をカウントするPythonスクリプトです。  
このスクリプトは、データベースの監視や分析に役立ちます。

created_atカラムが存在しないテーブルはスキップされます。

### 利用例
```
$ python tracking_records.py count_records "2023-01-01 00:00:00"
users: 20レコード
orders: 100レコード
```

## ユースケース
- データベースの監視：定期的にスクリプトを実行し、新規レコードの数を確認することで、データベースの活動状況を監視できます。
- データ分析：特定の日時後にどのテーブルにどれだけのデータが追加されたかを分析する際に使用できます。

## セットアップ
1. ライブラリをインストールします
    ```
    pip install -r requirements.txt
    ```
2. `.env`ファイルにデータベースへの接続情報を記載します

## 使い方
以下のコマンドを実行して、スクリプトを起動します。  
`<datetime>`は、レコードカウントの基準となる日時を指定してください（例：`2023-01-01 00:00:00`）
```
python tracking_records.py count_records <datetime>
```
スクリプトが実行され、指定された日時以降に作成されたレコードの数が各テーブルごとに出力されます。