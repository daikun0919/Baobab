## BAO BAB DB設計

## usersテーブル
|Column|Type|Options|
|------|----|-------|
|name|string|null: false|
|email|string|null: false|
|address|string|null: false|
|phone_number|string|null: false|
|password|string|null: false|
|nickname|string|null: false|
### Association
- has_many :video  through :items_user
has_many :items_user

## user_accountテーブル
|Column|Type|Options|
|------|----|-------|
|card_name|string|null: false|
|expiration_date|string|null: false|
|security_cord|string|null: false|
|card_name|string|null: false|
### Association
- belongs_to :user

## videosテーブル
|Column|Type|Options|
|------|----|-------|
|text|text|null: false|
|user_id|integer|null: false, foreign_key: true|
### Association
- belongs_to :user

## orderテーブル
|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|goods_id|integer|null: false, foreign_key: true|
### Association
- belongs_to :goods
- belongs_to :user

