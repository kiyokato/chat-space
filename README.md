# README

## messagesテーブル

|Column|Type|Options|
|--------|-------|-------------|
|body|text|null: false|
|image|string||
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|


## groupsテーブル
|Column|Type|Options|
|--------|-------|-------------|
|name|string|null: false|
|message_id|integer|null: false, foreign_key: true|
|member_id|integer|null: false, foreign_key: true|


## membersテーブル


## usersテーブル
