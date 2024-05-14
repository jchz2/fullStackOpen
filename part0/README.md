# Note Diagram

sequenceDiagram
    participant browser
    participant server

    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/notes
    activate server
    server-->>browser: HTML document
    deactivate server

    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/main.css
    activate server
    server-->>browser: the css file
    deactivate server

    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/main.js
    activate server
    server-->>browser: the JavaScript file
    deactivate server

    Note right of browser: The browser starts executing the JavaScript code that fetches the JSON from the server

    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/data.json
    activate server
    server-->>browser: [{ "content": "HTML is easy", "date": "2023-1-1" }, ... ]
    deactivate server

    Note right of browser: The browser executes the callback function that renders the notes
---
## [General Info](https://fullstackopen.com/en/part0/general_info)
- Prerequisites
- Course material
- Taking the course
- Course channel in Discord and Telegram
- How to get help in Discord/Telegram
- Parts and completion
- Studying the course in a nutshell
- Submitting exercises
- The course exam
- How to get your credits
- Where do I get my University of Helsinki Student number
- Course certificate
- Request a transcript of studies
- No more yearly versions
- Expanding on a previously completed course
- Full stack project
- Interview promise
- Before you start
- Typos in the material
---
## [Fundamentals of Web apps](https://fullstackopen.com/en/part0/fundamentals_of_web_apps)
- HTTP GET
- Traditional web applications
- Running application logic in the browser
- Event handlers and Callback functions
- Document Object Model or DOM
- Manipulating the document object from console
- CSS
- Loading a page containing JavaScript - review
- Forms and HTTP POST
- AJAX
- Single page app
- JavaScript-libraries
- Full-stack web development
- JavaScript fatigue
