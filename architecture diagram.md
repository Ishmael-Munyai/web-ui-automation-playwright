```mermaid
flowchart TD
    Start([User Trigger / Scheduler]) --> Bot[RPA Bot]
    Bot --> Process[Automation Logic]
    Process --> DB[(Database)]
    DB --> Read[Read Data]
    DB --> Write[Write Data]
    Read --> Process
    Write --> Process
    Process --> Output[Generate Report / Action]
    Output --> End([Automated Result Delivered])

    classDef actor stroke:#4ade80,fill:#f0fdf4
    classDef system stroke:#818cf8,fill:#eef2ff
    classDef data stroke:#38bdf8,fill:#ecfeff
    classDef output stroke:#fb923c,fill:#fff7ed
    classDef endStyle stroke:#f87171,fill:#fef2f2

    class Start actor
    class Bot,Process system
    class DB,Read,Write data
    class Output output
    class End endStyle
