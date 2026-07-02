```Mermaid
flowchart TD
    Start([User Trigger / Scheduler]) --> Bot[RPA Bot]
    Bot --> Process[Business Process Automation]
    Process --> DB[(MySQL Database)]
    DB --> Query[Read/Write Data]
    Query --> Process
    Process --> Report[Generate Report]
    Report --> PPT[Export to PowerPoint]
    PPT --> End([Automated Output Delivered])

    classDef actor stroke:#4ade80,fill:#f0fdf4
    classDef system stroke:#818cf8,fill:#eef2ff
    classDef data stroke:#38bdf8,fill:#ecfeff
    classDef output stroke:#fb923c,fill:#fff7ed
    classDef endStyle stroke:#f87171,fill:#fef2f2

    class Start actor
    class Bot,Process system
    class DB,Query data
    class Report,PPT output
    class End endStyle
