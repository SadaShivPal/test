```mermaid
erDiagram
    USERS ||--o{ SUBSCRIPTIONS : has
    USERS ||--o{ TRANSACTIONS : makes
    USERS ||--o{ SEARCH : makes
    BOOKS ||--o{ TRANSACTIONS : involved_in
    ADMIN ||--|| USERS : manages
```
