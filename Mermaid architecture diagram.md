```mermaid
flowchart TD
    subgraph UserInterface[UI System]
        UIForm[Claim Entry Form]
        UIDashboard[Claims Dashboard]
    end

    subgraph RPAWorkflow[RPA Bot Workflow]
        Trigger[Bot Trigger: Claim Received]
        Extract[Extract Claim Data]
        Validate[Validate Against Business Rules]
        Register[Register Claim in UI System]
        Exception[Exception Handling]
    end

    subgraph Database[Claims Database]
        DBWrite[Write Claim Record]
        DBUpdate[Update Claim Status]
    end

    subgraph Notifications[Communication Layer]
        NotifyOfficer[Notify Claims Officer]
        NotifyUser[Notify Claimant]
    end

    %% Connections
    UIForm --> Trigger
    Trigger --> Extract
    Extract --> Validate
    Validate -->|Valid| Register
    Validate -->|Invalid| Exception
    Register --> UIDashboard
    Register --> DBWrite
    DBWrite --> DBUpdate
    Exception --> NotifyOfficer
    Register --> NotifyUser
