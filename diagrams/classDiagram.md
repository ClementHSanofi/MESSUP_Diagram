```mermaid
classDiagram
    class User {
        +id: int
        +sanofi_id: string
        +username: string
        +role: string
    }
    User : +login()

    class Ticket {
        +id: int
        +title: string
        +description: text
        +status: enum
        +desired_date: date
        +estimated_time: int
        +real_time: int
        +is_priority: bool
        +is_reject: bool
        +created_at: timestamp
        +checked_at: timestamp
        +closed_at: timestamp
    }
    Ticket: +update()
    Ticket: +create()
    Ticket: +assignTo()
    Ticket: +createAnalysis()
    Ticket: +changeStatus()
    Ticket: +addComment()

    class Analysis {
        +id: int
        +mes_impact: enum
        +load: enum
        +impact_modif: enum
        +change_origin: enum
        +quality_issue: enum
        +gxp_ref: string
    }

    class Delivery {
        +id: int
        +version: int
        +status: status_delivery
        +object_modification: text
        +estimated_delivery: datetime
        +delivery_date: datetime
        +created_at: datetime
    }
    Delivery: +create()
    Delivery: +addTickets()
    Delivery:  +changeStatus()

    class Object {
        +id: int
        +name: string
        +commentary: text
    }
    Object: +create()

    class Comment {
        +id: int
        +content: text
        +created_at: timestamp
        +type: comment_type
    }

    User "1" --> "*" Ticket : created_by
    User "1" --> "*" Ticket : assigned_to
    Ticket "1" --> "1" Analysis
    Ticket "1" --> "*" Comment
    Delivery "1" --> "*" Ticket
    Delivery "1" --> "1" Object
    Ticket "1" --> "1" Object