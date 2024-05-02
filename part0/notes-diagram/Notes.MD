sequenceDiagram
    participant user
    participant page
    participant server


    user->>page: New Note
    activate page
    page-->>server: New Note
    deactivate page
    activate server
    server-->>page: Notes HTML
    deactivate server
    activate page
    page->>user: HTML


    Note left of user: When the server send the html page renders again