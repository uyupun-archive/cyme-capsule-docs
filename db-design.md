# DB設計

### users
ユーザ情報を格納したテーブル.

|カラム名|型|属性|説明|
|:--|:--|:--|:--|
|id|bigIncrements|-|数値のID. ユーザによる変更が不可|
|user_id|text|unique|ユーザID. 半角英数字のみ|
|password|text|-|ハッシュ化されたパスワード|
|access_token|text|-|アクセストークン|
|created_at|timestamps|-|作成された日付. Laravelによってデフォルトで生成される|
|updated_at|timestamps|-|更新された日付. Laravelによってデフォルトで生成される|

### time_capsules
タイムカプセル情報を格納したテーブル.

|カラム名|型|属性|説明|
|:--|:--|:--|:--|
|id|bigIncrements|-|ID|
|capsule_name|text|-|タイムカプセルの名前|
|buried_user_id|unsignedBigInteger|-|埋めた人のユーザID. usersテーブルのidカラムと紐付いている|
|user_name|text|-|タイムカプセルを埋めた人の名前|
|message|text|-|タイムカプセルのメッセージ|
|longitude|double|-|経度|
|latitude|double|-|緯度|
|dug_user_id|unsignedBigInteger|nullable|掘り出した人のユーザID. usersテーブルのidカラムと紐付いている|
|dug_at|timestamp|nullable|掘り出された日付|
|created_at|timestamps|-|作成された日付. Laravelによってデフォルトで生成される|
|updated_at|timestamps|-|更新された日付. Laravelによってデフォルトで生成される|