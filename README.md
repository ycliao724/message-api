# 留言 API

## 介紹
這是一個基於php開發的API，以laravel框架進行開發。
- 功能包括:
    - 顯示所有留言紀錄
    - 新增留言
    - 留言查詢
    - 修改留言
    - 刪除留言

## 使用說明

要開始使用留言 API，請按照以下步驟操作。

### 環境要求

- PHP
- Composer
- Laravel 9

### 安裝

1. 複製儲存庫
```sh 
git clone https://github.com/your-username/message-api.git
```

2. 安裝套件
```sh
composer install
```

3. 在 `.env` 檔案中設定資料庫配置
4. 執行資料庫遷移
```sh
php artisan migrate
```


5. 啟動開發伺服器
```sh
php artisan serve
```


## 使用方式

### 路由

- `GET /messages`：獲取所有留言。
- `POST /messages`：新增一則留言。
- `GET /messages/{id}`：透過 ID 取得特定留言。
- `PUT /messages/{id}`：透過 ID 更新特定留言。
- `DELETE /messages/{id}`：透過 ID 刪除特定留言。

### 範例請求

```http
POST /messages HTTP/1.1
Host: your-domain.com
Content-Type: application/json

{
    "title": "範例標題",
    "content": "這是一則範例留言。"
}
```
### 範例回應
```json
{
    "id": 1,
    "title": "範例標題",
    "content": "這是一則範例留言。",
    "created_at": "2023-10-21 08:51:51",
    "updated_at": "2023-10-21 08:51:51"
}
```