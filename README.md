# MySQL

DBを操作するための言語


## SQLの種類

DDL データ定義言語

DBオブジェクトの定義に使用

例

テーブル

インデックス

ファンクション

トリガー


DML データ操作言語

データの操作に使用

データの取得、更新、削除、挿入


## SQLの記法

セミコロンで区切る

大文字小文字は区別しない

コメント

/*区間コメント*/

-- 文末までのコメント


## 文法

### データベースの作成

create database データベース名;

### データベースの削除

drop database データベース名;

### テーブルの作成

create table データベース名.テーブル名 (
  カラム名 データ型 default デフォルト値 制約 comment 'コメント',
  表制約
)

### テーブルの作成

drop table データベース名.テーブル名;

### データ型

INT 整数値

FLOAT 浮動小数点

正の値に限定する場合はunsigned

DATETIME 日時

TIMESTAMP 日時

CHAR 固定長文字列

VARCHAR 可変長文字列

BLOB バイナリデータ（画像や音声、動画等）

### 制約

UNIQUE: 一意制約

NOT NULL: NOT NULL制約

CHECK: チェック制約

PRIMARY KEY: 主キー制約

FOREIGN KEY: 外部キー制約

### テーブル定義の確認

desc データベース名.テーブル名;

show full columns from データベース名.テーブル名;

show create table データベース名.テーブル名;

### アクティブなDBの切り替え

use データベース名.テーブル名;

### アクティブなDBの確認

select database();

### 自動IDの付与

auto_increment

### テーブル定義の変更

alter table データベース名.テーブル名
add column ... ;

after

first

modify column ... ;

drop column ... ;