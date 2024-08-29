```mermaid
erDiagram
    users {
        int id PK "ID"
        string name "名前"
        string tell "電話番号"
        string password "パスワード"
        string email "メールアドレス"
        string date_of_birth "誕生日"
        timestamp create_at "作成日"
        timestamp update_at "更新日"
    }

    medical_history{
        int id PK "ID"
        int user_id FK "ユーザーID"
        text content "診察内容"
        text memo "患者さんへのメモ"
        text doctor_memo "お医者さん専用メモ"
        timestamp create_at "作成日"
        timestamp examination_date "診察日"
        timestamp update_at "更新日"
        timestamp deleted_at "削除日"
    }

    admin_users{
        int id PK "ID"
        string name "名前"
        string password "パスワード"
        string email "メールアドレス"
         timestamp create_at "作成日"
        timestamp update_at "更新日" 
    }

    users ||--o{ medical_history: ""
```
