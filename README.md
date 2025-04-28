## paperdraft of table and relationships ##

## users ##

| Column             | Type   | Options                   |
| ------------------ | ------ | --------------------------|
| email              | string | null: false               |
| encrypted_password | string | null: false,unique: true  |
| name               | string | null: false               |
| profile            | text   | null:false                |
| occupation         | text   | null:false                |
| position           | text   | null:false                |

## association ##

- has_many: comments
- has_many: prototypes




## prototypes ##

| Column    | Type      | Options                       |
| ----------| --------- | ------------------------------|
| title     | string    | null: false                   |
| catch_copy| text      | null: false                   |
| concept   | text      | null: false                   |
| user      | references| null: false,foreign_key: true|

## association ##

- has_many: comments
- belongs_to: users




## comments table ##
| Column     | Type       | Options                         |
|------------|------------|---------------------------------|
| content    | text       | null: false                     |
| prototypes | references | null: false,foreign_key: true   |
| user       | references | null: false,foreign_key: true   |

## association ##

- belongs_to: users
- belongs_to: prototype






























































<!-- 
### Association

- has_many :room_users
- has_many :users, through: :room_users
- has_many :messages

## room_users テーブル

| Column | Type       | Options                        |
| ------ | ---------- | ------------------------------ |
| user   | references | null: false, foreign_key: true |
| room   | references | null: false, foreign_key: true |

### Association

- belongs_to :room
- belongs_to :user

## messages テーブル

| Column  | Type       | Options                        |
| ------- | ---------- | ------------------------------ |
| content | string     |                                |
| user    | references | null: false, foreign_key: true |
| room    | references | null: false, foreign_key: true |

### Association

- belongs_to :room
- belongs_to :user -->