sequenceDiagram
    participant user
    participant client
    participant server


    user->>client: New Note
    activate client
    client->>user:appends new note to list
    client->>server: POST New Note
    server->>client: Ok Created