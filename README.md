# HackingLog

技術ブログやプログラミングの情報を共有するためのアプリ

# Description

pythonの使い方やマーケティング、<br>
などの情報を発信するブログです。

# 作成背景

# 本番環境
http://54.199.93.45

テストユーザー<br>
ID:test1@gmail.com<br>
パスワード:qazwsxe<br>

# Features
・メインページの表示<br>
・ユーザー登録<br>
・ユーザーログイン<br>
・ユーザーログアウト<br>
・記事一覧表示<br>
・カテゴリー別の表示<br>
・タグ別の表示<br>
・キーワード別で記事の検索<br>
・レスポンシブル対応<br>
・いいね、コメント機能<br>

## Dependency

| 種別       | 名称                         |
| -------- | -------------------------- |
| 開発言語     | Python(ver 3.7.7)            |
| フレームワーク  | Django(ver 3.1) |
| マークアップ   | HTML(Haml),CSS(Saas)       |
| フロントエンド  | Javascript(React)         |
| DB       | MYSQL                      |
| 本番環境     | AWS EC2                    |
| 画像アップロード | django-storages, AWS S3        |

## ER図
https://app.diagrams.net/?state=%7B%22folderId%22:%221ipSeMsnmdo2h9GrQx9VWau4VNBZIYyeB%22,%22action%22:%22create%22,%22userId%22:%22112328532593405325388%22%7D#G1HQJM-M4i9JAWvyWZ6qhb9tvBBUzw1Qit

## usersテーブル

| Column          | Type    | Options                             |
| --------------- | ------- | ----------------------------------- |
| nickname        | string  | null: false,limit: 20               |
| email           | string  | null: false, unique: true           |
| password        | strinfg | null: false, unique: true           |

### Association

- has_many :items, dependent: :destroy
- has_one  :address

