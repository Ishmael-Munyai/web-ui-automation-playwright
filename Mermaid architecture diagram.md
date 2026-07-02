```mermaid
flowchart TD
    Start([User Trigger / Scheduler]) --> Bot[RPA Bot]
    Bot --> UI[UI Automation Layer]
    UI --> App1[Web Application]
    UI --> App2[Desktop Application]
    UI --> App3[Legacy System]

    Bot --> Process[Business Process Logic]
    Process --> DB[(MySQL Database)]
    DB --> Query[Read/Write Data]
    Query --> Process

    Process --> Report[Generate Report]
    Report --> PPT[Export to PowerPoint]
    Report --> BI[Power BI Metrics & Dashboards]

    BI --> KPI1[Operational KPIs]
    BI --> KPI2[Financial Metrics]
    BI --> KPI3[Process Efficiency]

    PPT --> End([Automated Output Delivered])
    BI --> End

    classDef actor stroke:#4ade80,fill:#f0fdf4
    classDef system stroke:#818cf8,fill:#eef2ff
    classDef ui stroke:#facc15,fill:#fefce8
    classDef data stroke:#38bdf8,fill:#ecfeff
    classDef output stroke:#fb923c,fill:#fff7ed
    classDef analytics stroke:#a855f7,fill:#f5f3ff
    classDef endStyle stroke:#f87171,fill:#fef2f2

    class Start actor
    class Bot,Process system
    class UI ui
    class DB,Query data
    class Report,PPT output
    class BI,KPI1,KPI2,KPI3 analytics
    class End endStyle
