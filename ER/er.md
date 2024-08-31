```mermaid
erDiagram
    users {
        int id PK "ID" %% auto increment
        string name "名前"
        string tell "電話番号"
        string email "メールアドレス"
        string password "パスワード"
        string date_of_birth "誕生日"
        timestamp create_at "作成日"
        timestamp update_at "更新日"
        timestamp last_hospital_visit_at "最新来院日"
    }

    medical_history{
        int id PK "ID" %% auto increment
        int user_id FK "ユーザーID"
        text content "診察内容"
        text condition "容態"
        text doctor_memo "お医者さん専用"
        timestamp create_at "作成日"
        timestamp examination_ar "診察日"
        timestamp update_at "更新日"
        timestamp deleted_flag "削除"
    }

    admin_users{
        int id PK "ID"  %% auto increment
        string name "名前"
        string password "パスワード"
        string email "メールアドレス"
        timestamp create_at "作成日"
        timestamp update_at "更新日" 
    }

    users ||--o{ medical_history: ""
```
