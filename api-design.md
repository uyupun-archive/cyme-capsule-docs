# APIドキュメント

### ユーザ登録

##### Endpoint

```text
POST /api/user/register
```

##### Request

```json
{
  "user_id": "XXXX",
  "password": "XXXX"
}
```

##### Response

```json
{
  "access_token": "XXXX"
}
```

### ユーザログイン

##### Endpoint

```text
POST /api/user/login
```

##### Request

```json
{
  "user_id": "XXXX",
  "password": "XXXX"
}
```

##### Response

```json
{
  "access_token": "XXXX"
}
```

### ユーザログアウト

##### Endpoint

```text
POST /api/user/logout
```

##### Request

```json
{}
```

##### Response

```json
{}
```

### 埋めたカプセル一覧の取得

##### Endpoint

```text
GET /api/capsule/list/buried
```

##### Request

```json
{}
```

##### Response

```json
[
  {
    "id": 1,
    "capsule_name": "XXXX"
  },
  ...
]
```

### 掘り起こしたカプセル一覧の取得

##### Endpoint

```text
GET /api/capsule/list/dug
```

##### Request

```json
{}
```

##### Response

```json
[
  {
    "id": 1,
    "capsule_name": "XXXX"
  },
  ...
]
```

### カプセルを開く

##### Endpoint

```text
GET /api/capsule/open
```

##### Request

```json
{
  "id": 1
}
```

##### Response

```json
{
  "id": 1,
  "capsule_name": "XXXX",
  "longitude": 1.14514,
  "latitude": 1.919810,
  "burier": "XXXX",
  "message": "XXXXXXXXXX",
  "dug_at": "XXXX"
}
```

### カプセルを埋める

##### Endpoint

```text
POST /api/capsule/bury
```

##### Request

```json
{
  "capsule_name": "XXXX",
  "longitude": 1.14514,
  "latitude": 1.919810,
  "burier": "XXXX",
  "message": "XXXXXXXXXX"
}
```

##### Response

```json
{}
```

### カプセルを探す

##### Endpoint

```text
GET /api/capsule/search
```

##### Request

```json
{
  "longitude": 1.14514,
  "latitude": 1.919810
}
```

##### Response

```json
[
  {
    "id": 1,
    "capsule_name": "XXXX"
  },
  ...
]
```

### カプセルを掘り出す

##### Endpoint

```text
POST /api/capsule/dig
```

##### Request

```json
{
  "id": 1
}
```

##### Response

```json
{
  "id": 1,
  "capsule_name": "XXXX",
  "longitude": 1.14514,
  "latitude": 1.919810,
  "burier": "XXXX",
  "message": "XXXXXXXXXX",
  "dug_at": "XXXX"
}
```