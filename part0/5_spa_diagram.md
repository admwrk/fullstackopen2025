```mermaid
    participant browser
    participant server

    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/spa
    server activated
    server-->>browser: HMTL document
    server deactivated

    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/main.css
    server activated
    server-->>browser: css file
    server deactivated

    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/spa.js
    server activated
    server-->>browser: js file
    server deactivated
    
    Note right of browser: the JS file executes in the browser and initiates an HTTP GET to retrieve the data.json file with the notes

    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/data.json
    server activated
    server-->>browser: json file with notes
    server deactivated

    Note right of browser: The notes are received and rendered by the browser 
```
