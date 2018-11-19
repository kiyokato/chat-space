# README

## messagesテーブル

|Column|Type|Options|
|--------|-------|-------------|
|body|text|null: false|
|image|string||
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user


## groupsテーブル
|Column|Type|Options|
|--------|-------|-------------|
|name|string|null: false|
|message_id|integer|null: false, foreign_key: true|
|member_id|integer|null: false, foreign_key: true|


## membersテーブル
|Column|Type|Options|
|--------|-------|-------------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|


## usersテーブル
|Column|Type|Options|
|--------|-------|-------------|
|name|string|null: false, unique: true|
|email|string|null: false, unique: true, index: true|
|password|string|null: false|
|member_id|integer|foreign_key: true|

