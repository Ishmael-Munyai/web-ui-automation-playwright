```mermaid
flowchart LR
    DB[(Database)]
    Bot[RPA Bot]
    ERP[Enterprise System (ERP/CRM/Core Banking)]
    User([Business User])

    User -->|Trigger / Schedule| Bot
    Bot -->|Read / Write| DB
    Bot -->|UI Automation / API| ERP
    ERP -->|Confirmation / Status| Bot
    Bot -->|Logs / Reports| DB
    Bot -->|Output to Excel / Email| User
