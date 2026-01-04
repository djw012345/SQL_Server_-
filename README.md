# SQL_Server_-


資料來源
https://www.fooish.com/sql/create-table.html

## 創建資料庫
``` SQL
CREATE DATABASE sql_tutorial;
```

## 刪除資料庫
SQL:
``` SQL
DROP DATABASE sql_tutorial;
```

``` txt
INT  --整數
DECIMAL(3,2) --有小數點的數 2.33
VARCHAR(n)     -- 字串
BLOB    -- (Binary Large Objet) 圖片 影片 檔案...
DATE    -- 'YYYYMMDD' 日期 2021-08-08
TIME    -- 'YYYY-MM-DD HH:MM:SS' 紀錄時間 
```


## 創建資料表 CREATE TABLE
SQL:
``` SQL
CREATE TABLE customers (
    id INT IDENTITY(1,1) PRIMARY KEY,
    name NVARCHAR(50) NOT NULL,  --NVARCHAR支援 Unicode
    email NVARCHAR(100) UNIQUE,
    phone NVARCHAR(20),
    created_at DATETIME DEFAULT GETDATE()
);

```





