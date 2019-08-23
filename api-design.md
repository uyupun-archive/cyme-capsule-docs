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
{}
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
{}
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
    "name": "XXXX",
    "id": 1
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
    "name": "XXXX",
    "id": 1
  },
  ...
]
```

### カプセルを埋める

##### Endpoint

```text
POST /api/capsule/bury
```

##### Request

```json
{
  "name": "XXXX",
  "location": "XXXX",
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
  "location": "XXXX"
}
```

##### Response

```json
[
  {
    "name": "XXXX",
    "id": 1
  },
  ...
]
```

### カプセルを掘り起こす

##### Endpoint

```text
POST /api/capsule/dig
```

##### Request

```json

```

##### Response

```json

```