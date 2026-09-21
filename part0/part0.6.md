```mermaid
sequenceDiagram
    participant browser
    participant server

    Note left of browser: User clicks "save"
    Note left of browser: Event handler updates notes list, re-renders the DOM
    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server
    server-->>browser: 201 Created 
    deactivate server
```