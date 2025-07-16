# APIへのアクセスコントロール

各 API を使用するために必要なロールおよびトークンについて記述します。

下記は API そのものへのアクセスコントロールであり、特記なき場合、アイテム、インデックス、ファイル等へのアクセスはそれぞれへのアクセスコントロールも適用されます。

## アイテム

API を利用可能なロール

アクセストークンに必要なスコープ

`[GET] /api/<version>/records`

`[GET] /api/<version>/records/<pid_value>`

`[GET] /api/<version>/records/<pid_value>/stats`

`[POST] /api/<version>/records/list`

`[GET] /api/index/`

`[GET] /api/records/`

`[PUT] /api/records/`

## ファイル

`[GET] /api/<version>/ranking/<pid_value>/files`

`[GET] /api/<version>/records/<pid_value>/files/<filename>`

`[GET] /api/<version>/records/<pid_value>/files/<filename>/stats`

`[GET] /api/<version>/records/<pid_value>/files/all`

`[POST] /api/<version>/records/<pid_value>/files/selected`

`[GET] /api/<version>/ranking/<ranking_type>`

## インデックス

### API を利用可能なロール

| API エンドポイント \ ロール                        | システム<br>管理者 | リポジトリ<br>管理者 | コミュニティ<br>管理者 | 登録ユーザ | 一般ユーザ | ゲスト<br>(未ログイン) |
| -------------------------------------------------- | ------------------ | -------------------- | ---------------------- | ------------ | ------------ | ---------------------- |
| [GET] /api/\<version>/tree                         | ○                  | ○                    | ○                      | ○            | ○            | ✕                      |
| [GET] /api/\<version>/tree/<index_id>              | ○                  | ○                    | ○                      | ○            | ○            | ✕                      |
| [GET] /api/\<version>/tree/index                   | ○                  | ○                    | ○                      | ○            | ○            | ○                      |
| [GET] /api/\<version>/tree/index/<index_id>        | ○                  | ○                    | ○                      | ○            | ○            | ○                      |
| [GET] /api/\<version>/tree/index/<index_id>/parent | ○                  | ○                    | ○                      | ○            | ○            | ○                      |
| [POST] /api/\<version>/tree/index                  | ○                  | ○                    | ○                      | ✕            | ✕            | ✕                      |
| [PUT] /api/\<version>/tree/index/<index_id>        | ○                  | ○                    | ○                      | ✕            | ✕            | ✕                      |
| [DELETE] /api/\<version>/tree/index/<index_id>     | ○                  | ○                    | ○                      | ✕            | ✕            | ✕                      |

### アクセストークンに必要なスコープ

| API エンドポイント \ スコープ                      | index: read | index:create | index:update | index:delete |
| -------------------------------------------------- | ----------- | ------------ | ------------ | ------------ |
| [GET] /api/\<version>/tree                         | ○           |              |              |              |
| [GET] /api/\<version>/tree/<index_id>              | ○           |              |              |              |
| [GET] /api/\<version>/tree/index/<index_id>/parent | ○           |              |              |
| [GET] /api/\<version>/tree/index                   | ○           |              |              |              |
| [GET] /api/\<version>/tree/index/<index_id>        | ○           |              |              |              |
| [POST] /api/\<version>/tree/index                  |             | ○            |              |              |
| [PUT] /api/\<version>/tree/index/<index_id>        |             |              | ○            |              |
| [DELETE] /api/\<version>/tree/index/<index_id>     |             |              |              | ○            |

## アクティビティ

`[POST] /api/depositactivity`

`[GET] /api/depositactivity/<activity_id>`

`[DELETE] /api/depositactivity/<activity_id>`

## Opensearch

`[GET] /api/opensearch/description.xml`

`[GET] /api/opensearch/search`

`[POST] /api/opensearch/search`

## 著者

`[GET] /api/<version>/authors`

`[POST] /api/<version>/authors`

`[DELETE] /api/<version>/authors/<identifier>`

`[GET] /api/<version>/authors/count`

## リクエストメール

`[GET] /api/<version>/captcha/image`

`[GET] /api/<version>/captcha/validate`

`[POST] /api/<version>/records/<pid_value>/request-mail`

## ログイン

`[POST] /api/<version>/login`

`[POST] /api/<version>/logout`

## OA ステータス

`[POST] /api/<version>/oa_status/callback`

## SWORD API

`[DELETE] /api/sword/deposit/<recid>`

`[GET] /api/sword/deposit/<recid>`

`[PUT] /api/sword/deposit/<recid>`

`[GET] /api/sword/service-document`

`[POST] /api/sword/service-document`

## 制限公開機能

`[GET] /api/<version>/workflow/activities`

`[POST] /api/<version>/workflow/activities/{activity_id}/approve`

`[POST] /api/<version>/workflow/activities/{activity_id}/throw-out`

`[GET] /api/<version>/records/{pid}/files/{filename}/terms`

`[POST] /api/<version>/records/{pid}/files/{filename}/application`

`[POST] /api/<version>/workflow/activities/{activity_id}/application`

`[GET] /api/<version>/records/{pid}/need-restricted-access`
