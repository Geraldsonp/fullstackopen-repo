sequenceDiagram
    participant user
    participant browser
    participant server


    user->>browser: https://studies.cs.helsinki.fi/exampleapp/spa
    activate browser
    browser-->>server: GET https://studies.cs.helsinki.fi/exampleapp/spa
    deactivate browser
    activate server
    server-->>browser: HTML
    deactivate server
    activate browser
    browser->>server: GET Spa.js
    deactivate browser
    activate server
    server->>browser: Spa.js
    deactivate server
    activate browser
    browser->>server: GET data.json
    deactivate browser
    activate server
    server->>browser: data.json
    deactivate server
    activate browser
    browser->>user: executes js and renders data