# テーブル設計

## usersテーブル

|email       |encrypted_password|name    |profile  |occupation|position |
|------------|------------------|--------|---------|----------|---------|
|string      |string            |string  |text     |text      |text     |  
|NOT NULL    |NOT NULL          |NOT NULL|NOT NULL |NOT NULL  |NOT NULL |
|ユニーク制約 |string            |        |         |          |         |

### commentsテーブル

|content     |prototype      |user   　　 |
|------------|-------------- |-------　　-|
|text      　|references型   |references型|
|NOT NULL    |NOT NULL       |NOT NULL    |
|email       |外部キー　　　　|外部キー    |


#### prototypesテーブル
|title       |chatch_copy      |concept  |user   　　 |
|------------|-----------------|---------|------------|
|string      |text型           |text型   |references型| 
|NOT NULL    |NOT NULL         |NOT NULL |NOT NULL    |
|            |        　　   　|         |外部キー     |     
