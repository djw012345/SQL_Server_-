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
    created_at DATETIME DEFAULT GETDATE()   --取得現在時間
);

```


## 插入資料測試




``` SQL
USE sql_tutorial;
GO

INSERT INTO dbo.customers (name, email, phone)
VALUES ('王小明', 'test@example.com', '0912345678');
```

說明
``` txt
USE 指定資料庫

customers 👉 指定的資料表
(name, email, phone) 👉 指定要插入的欄位
id 是 IDENTITY 👉 不用寫，SQL Server 會自動產生
created_at 有 DEFAULT GETDATE() 👉 不用寫
```

### 直接指定「資料庫.結構.資料表」（最精準）
```SQL
INSERT INTO YourDatabaseName.dbo.customers (name, email, phone)  --資料庫名(YourDatabaseName).結構名(dbo).資料表名(customers)
VALUES ('王小明', 'test2@example.com', '0987654321');
```








