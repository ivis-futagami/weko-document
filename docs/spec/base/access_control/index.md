# アクセスコントロール

## 目次

- [アクセスコントロール](#アクセスコントロール)
  - [目次](#目次)
  - [アイテム](#アイテム)
    - [アイテム閲覧](#アイテム閲覧)
    - [アイテム編集](#アイテム編集)
    - [アイテム削除](#アイテム削除)
    - [公開ステータス変更](#公開ステータス変更)
    - [リクエストメール](#リクエストメール)
    - [エクスポート](#エクスポート)
    - [OAI-PMH](#oai-pmh)
    - [Other Formats](#other-formats)
  - [インデックス](#インデックス)
    - [インデックス閲覧](#インデックス閲覧)
    - [インデックス編集](#インデックス編集)
    - [インデックス削除](#インデックス削除)
  - [ファイル](#ファイル)
      - [ファイルダウンロード](#ファイルダウンロード)
      - [ファイル情報](#ファイル情報)
    - [制限公開用のコンテンツファイル](#制限公開用のコンテンツファイル)
      - [利用申請機能](#利用申請機能)
  - [ワークフロー](#ワークフロー)
    - [新規アクティビティ](#新規アクティビティ)
  - [コニュニティ画面](#コニュニティ画面)
  - [アカウント設定画面](#アカウント設定画面)
    - [プロフィール](#プロフィール)
    - [secrity](#secrity)
    - [通知](#通知)
    - [アプリケーション](#アプリケーション)
    - [Groups](#groups)
    - [セッション](#セッション)
    - [Administration](#administration)
    - [Workspace](#workspace)
  - [ワークスペース画面](#ワークスペース画面)
  - [管理画面](#管理画面)
    - [アイテムタイプ管理](#アイテムタイプ管理)
    - [アイテム管理](#アイテム管理)
      - [インデックスツリー管理](#インデックスツリー管理)
    - [ウェブデザイン管理](#ウェブデザイン管理)
    - [著者DB管理](#著者db管理)
    - [統計](#統計)
    - [ワークフロー管理](#ワークフロー管理)
    - [コミュニティ管理](#コミュニティ管理)
    - [OAI-PMH](#oai-pmh-1)
    - [Resource Sync](#resource-sync)
    - [SWORD API](#sword-api)
    - [ファイル管理](#ファイル管理)
    - [レコード管理](#レコード管理)
    - [ユーザー管理](#ユーザー管理)
    - [設定](#設定)
    - [ログ管理](#ログ管理)
    - [メンテナンス](#メンテナンス)
  - [APIへのアクセス](#apiへのアクセス)
    - [アイテム](#アイテム-1)
    - [ファイル](#ファイル-1)
    - [インデックス](#インデックス-1)
      - [APIを利用可能なロール](#apiを利用可能なロール)
      - [アクセストークンに必要なスコープ](#アクセストークンに必要なスコープ)
    - [アクティビティ](#アクティビティ)
    - [Opensearch](#opensearch)
    - [著者](#著者)
    - [リクエストメール](#リクエストメール-1)
    - [ログイン](#ログイン)
    - [OAステータス](#oaステータス)
    - [SWORD API](#sword-api-1)
    - [制限公開機能](#制限公開機能)

## アイテム

### アイテム閲覧

### アイテム編集

### アイテム削除

### 公開ステータス変更

### リクエストメール

### エクスポート

### OAI-PMH

エンドポイント: `/oai`

### Other Formats

エンドポイント: `/records/<アイテムID>/export/<フォーマット>`

## インデックス



### インデックス閲覧

親インデックス閲覧可否(※1)<br>インデックス公開状態(※2)<br>閲覧権限の有無(※3)| システム<br>管理者 | リポジトリ<br>管理者 | コミュニティ<br>管理者 | 登録ユーザー | 一般ユーザー | ゲスト(未ログイン) |
| --- | :-----------:  | :------------: |:------------: |:------------: |:------------: |:------------: |
| 親インデックス: 閲覧可  <br> インデックス: 公開  <br>閲覧権限: あり  | ○ | ○ | ○ | ○ | ○ | ○ |
| 親インデックス: 閲覧可  <br> インデックス: 公開 <br>閲覧権限: なし   | ○ | ○ | △(※4) | ✕ | ✕ | ✕ |
| 親インデックス: 閲覧可  <br> インデックス: 非公開  <br>閲覧権限: あり| ○ | ○ | △(※4) | ✕ | ✕ | ✕ |
| 親インデックス: 閲覧可  <br> インデックス: 非公開 <br>閲覧権限: なし | ○ | ○ | △(※4) | ✕ | ✕ | ✕ |
| 親インデックス: 閲覧不可<br> インデックス: 公開  <br>閲覧権限: あり  | ○ | ○ | △(※4) | ✕ | ✕ | ✕ |
| 親インデックス: 閲覧不可<br> インデックス: 公開<br>閲覧権限: なし    | ○ | ○ | △(※4) | ✕ | ✕ | ✕ |
| 親インデックス: 閲覧不可<br> インデックス: 非公開<br>閲覧権限: あり  | ○ | ○ | △(※4) | ✕ | ✕ | ✕ |
| 親インデックス: 閲覧不可<br> インデックス: 非公開<br>閲覧権限: なし  | ○ | ○ | △(※4) | ✕ | ✕ | ✕ |

※1「親インデックス:閲覧可」とは、親インデックスがRoot Indexである、またはユーザが親インデックスを閲覧可の状態を指します。  

※2「インデックス:公開」とは、管理画面の「インデックスツリー管理 > ツリー編集 > インデックス編集 > 公開」で「公開」にチェックがあり、「公開日」が空または過去の日付に設定されている状態を指します。  

※3「閲覧権限あり」とは、管理画面の「インデックスツリー管理 > ツリー編集 > インデックス編集 > 閲覧権限」でユーザの持つロールまたはグループが「権限あり」に設定されている状態を指します。  

※4

### インデックス編集

### インデックス削除


## ファイル

#### ファイルダウンロード

エンドポイント: `/record/<アイテムID>/files/<ファイル名>`

#### ファイル情報

エンドポイント: `/records/<アイテムID>/file_details/<ファイル名>`

### 制限公開用のコンテンツファイル

#### 利用申請機能

利用申請ワークフロー


## ワークフロー

エンドポイント: `/workflow`

### 新規アクティビティ

エンドポイント: `/workflow/activity/new`

## コニュニティ画面

エンドポイント: `/c`

## アカウント設定画面

エンドポイント: `/account/settings`

### プロフィール

### secrity

### 通知

### アプリケーション

### Groups

### セッション

### Administration
 
`管理画面`に記載します。

### Workspace

`ワークスペース画面`に記載します。

## ワークスペース画面

エンドポイント: `/workspace`

## 管理画面

エンドポイント: `/admin`

### アイテムタイプ管理

### アイテム管理

#### インデックスツリー管理

### ウェブデザイン管理

### 著者DB管理

### 統計

### ワークフロー管理

### コミュニティ管理

### OAI-PMH

### Resource Sync

### SWORD API

### ファイル管理

### レコード管理

### ユーザー管理

### 設定

### ログ管理

### メンテナンス


## APIへのアクセス

各APIを使用するために必要なロールおよびトークンについて記述します。

下記はAPIそのものへのアクセスコントロールであり、特記なき場合、アイテム、インデックス、ファイル等へのアクセスはそれぞれへのアクセスコントロールも適用されます。


### アイテム

APIを利用可能なロール

アクセストークンに必要なスコープ


`[GET] /api/\<version>/records`

`[GET] /api/\<version>/records/<pid_value>`

`[GET] /api/\<version>/records/<pid_value>/stats`

`[POST] /api/\<version>/records/list`

`[GET] /api/index/`

`[GET] /api/records/`

`[PUT] /api/records/`


### ファイル

`[GET] /api/\<version>/ranking/<pid_value>/files`

`[GET] /api/\<version>/records/<pid_value>/files/<filename>`

`[GET] /api/\<version>/records/<pid_value>/files/<filename>/stats`

`[GET] /api/\<version>/records/<pid_value>/files/all`

`[POST] /api/\<version>/records/<pid_value>/files/selected`

`[GET] /api/\<version>/ranking/<ranking_type>`


### インデックス

#### APIを利用可能なロール

| APIエンドポイント  | システム<br>管理者 | リポジトリ<br>管理者 |  コミュニティ<br>管理者 | 登録ユーザー | 一般ユーザー | ゲスト<br>(未ログイン) |
| -------------------- | ------------------ | -------------------- | ----------------------- | ------------ | ------------ | ------------ |
| [GET] /api/\<version>/tree | ○                  | ○                    |  ○                      | ○            | ○            | ✕ |
| [GET] /api/\<version>/tree/<index_id>         | ○                  | ○                    |  ○                      | ○           | ○           |✕ |
| [GET] /api/\<version>/tree/index/<index_id>/parent   | ○                  | ○                    |  ○                      | ○           | ○           |✕ |
| [GET] /api/\<version>/tree/index | ○                  | ○                    |  ○                      | ○            | ○            | ○ |
| [GET] /api/\<version>/tree/index/<index_id> | ○                  | ○                    |  ○                      | ○            | ○            | ○ |
| [POST] /api/\<version>/tree/index | ○                  | ○                    |  △(※1)                      | ✕            | ✕     | ✕ |
| [PUT] /api/\<version>/tree/index/<index_id> | ○                  | ○                    |  △(※1)                      | ✕            | ✕     |✕ |
| [DELETE] /api/\<version>/tree/index/<index_id> | ○                  | ○                    |  △(※1)                      | ✕            | ✕     |✕ |

※1: コミュニティ管理者は、所属するコミュニティのインデックスのみを操作可能です。

#### アクセストークンに必要なスコープ

| APIエンドポイント   | index: read | index:create |  index:update | index:delete |
| -------------------- | ------------------ | -------------------- | ----------------------- | ------------ | 
| [GET] /api/\<version>/tree | ○                  |     |      |    |
| [GET] /api/\<version>/tree/<index_id>      |  ○ |    |   |   |
| [GET] /api/\<version>/tree/index/<index_id>/parent  | ○ |   |  |
| [GET] /api/\<version>/tree/index |  ○ |    |    |    |
| [GET] /api/\<version>/tree/index/<index_id> |  ○  |   |    |   |
| [POST] /api/\<version>/tree/index |     |   ○  |     |   |
| [PUT] /api/\<version>/tree/index/<index_id> |   |    |    ○ |    |
| [DELETE] /api/\<version>/tree/index/<index_id> |  |    |   | ○  |

### アクティビティ

`[POST] /api/depositactivity`

`[GET] /api/depositactivity/<activity_id>`

`[DELETE] /api/depositactivity/<activity_id>`

### Opensearch

`[GET] /api/opensearch/description.xml`

`[GET] /api/opensearch/search`

`[POST] /api/opensearch/search`

### 著者

`[GET] /api/\<version>/authors`

`[POST] /api/\<version>/authors`

`[DELETE] /api/\<version>/authors/<identifier>`

`[GET] /api/\<version>/authors/count`

### リクエストメール

`[GET] /api/\<version>/captcha/image`

`[GET] /api/\<version>/captcha/validate`

`[POST] /api/\<version>/records/<pid_value>/request-mail`

### ログイン

`[POST] /api/\<version>/login`

`[POST] /api/\<version>/logout`

### OAステータス

`[POST] /api/\<version>/oa_status/callback`

### SWORD API

`[DELETE] /api/sword/deposit/<recid>`

`[GET] /api/sword/deposit/<recid>`

`[PUT] /api/sword/deposit/<recid>`

`[GET] /api/sword/service-document`

`[POST] /api/sword/service-document`

### 制限公開機能

`[GET] /api/\<version>/workflow/activities`

`[POST] /api/\<version>/workflow/activities/{activity_id}/approve`

`[POST] /api/\<version>/workflow/activities/{activity_id}/throw-out`

`[GET] /api/\<version>/records/{pid}/files/{filename}/terms`

`[POST] /api/\<version>/records/{pid}/files/{filename}/application`

`[POST] /api/\<version>/workflow/activities/{activity_id}/application`

`[GET] /api/\<version>/records/{pid}/need-restricted-access`
