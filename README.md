```mermaid
erDiagram
    USERS ||--o{ SUBSCRIPTIONS : has
    USERS ||--o{ TRANSACTIONS : makes
    USERS ||--o{ SEARCH : makes
    BOOKS ||--o{ TRANSACTIONS : involved_in
    ADMIN ||--|| USERS : manages
    USERS {
        UserID PK
        Name
        Email
        Password
        OtherDetails
    }
    BOOKS {
        BookID PK
        Title
        Author
        ISBN
        Description
        Cost
        Popularity
    }
    SUBSCRIPTIONS {
        SubscriptionID PK
        UserID FK
        StartDate
        EndDate
        Status
    }
    TRANSACTIONS {
        TransactionID PK
        UserID FK
        BookID FK
        Date
        PaymentMethod
    }
    ADMIN {
        AdminID PK
        Name
        Email
        Password
    }
    SEARCH {
        SearchID PK
        UserID FK
        Query
        Date
    }
```
