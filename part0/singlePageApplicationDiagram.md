sequenceDiagram
    participant browser
    participant server

    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/spa
    activate server
    server-->>browser: HTML document
    deactivate server
    
    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/main.css
    activate server
    server-->>browser: the css file
    deactivate server

    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/spa.js
    activate server
    server-->>browser: the JavaScript file
    deactivate server

    Note right of browser: The browser starts executing the JavaScript code that fetches the JSON from the server

    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/data.json
    activate server
    server-->>browser: [{ "content": "HTML is easy", "date": "2024-5-22" }, ... ]
    deactivate server
    
    browser-->>server: GET chrome-extension://cofdbpoegempjloogbagkncekinflcnj/build/content.css
    activate server
    server-->>browser: the css file
    deactivate server
    
    browser-->>server: GET chrome-extension://cofdbpoegempjloogbagkncekinflcnj/fonts/OpenSans_VariableFont_wdth_wght.ttf
    activate server
    server-->>browser: the ttf file
    deactivate server

    Note right of browser: The browser executes the callback function that renders the notes
