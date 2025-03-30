```mermaid
sequenceDiagram
    participant browser
    participant server

    browser->>server: POST /new-note-spa
    activate server
    server-->>browser: 201 created
    deactivate server

    Note right of browser: All the server does is acknowledge receipt of the note, the browser renders the new note itself
```