# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...

# DB設計

users_table
|id        |integer|null :false|
|name      |integer|null :false|
|email     |text   |null :false|
|password  |text   |null :false|
|password_confirmation|null :false|

comments_table
|id        |integer|null :false|
|comment   |text   |null :false|
|post_id   |references|foreign_key: true|
|user_id   |references|foreign_key: true|

posts_table
|id        |integer|null :false|
| caption  |integer|null :false|
|user_id   |references|foreign_key: true|

likes_table
|id         |integer|null :false|
|post_id   |references|foreign_key: true|
|user_id   |references|foreign_key: true|

photos_table
|id   |integer        |null :false|
|image|               |null :false|
|post_id|references   |foreign_key :true|
