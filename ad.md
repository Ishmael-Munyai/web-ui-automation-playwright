```mermaid
flowchart LR
    Scan[Scanned Document / PDF] --> OCR[OCR Engine]
    OCR --> Clean[Data Validation & Cleaning]
    Clean --> DB[(Database)]
    DB --> Bot[RPA Bot]
    Bot --> ERP[Enterprise System ERP/CRM/Banking]
    ERP --> Confirm[Confirmation / Status]
    Confirm --> Report[Excel / Email Report]
    Report --> User([Business User])
