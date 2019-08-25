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
|user_id|unsignedBigInteger|ユーザID. usersテーブルのidカラムと紐付いている|
|user_name|text|-|タイムカプセルを埋めた人の名前|
|message|text|-|タイムカプセルのメッセージ|
|longitude|double|-|経度|
|latitude|double|-|緯度|
|created_at|timestamps|-|作成された日付. Laravelによってデフォルトで生成される|
|updated_at|timestamps|-|更新された日付. Laravelによってデフォルトで生成される|

### dug_time_capsules
掘り出したタイムカプセル情報を格納したテーブル.

|カラム名|型|属性|説明|
|:--|:--|:--|:--|
|id|bigIncrements|-|ID|
|capsule_id|unsignedBigInteger|-|掘り出したカプセルのID. time_capsulesテーブルのidカラムと紐付いている|
|user_id|unsignedBigInteger|-|掘り出したユーザのID. usersテーブルのidカラムと紐付いている|
|dug_at|timestamp|-|掘り出した日付|
|created_at|timestamps|-|作成された日付. Laravelによってデフォルトで生成される|
|updated_at|timestamps|-|更新された日付. Laravelによってデフォルトで生成される|
