sequenceDiagram
participant user
participant browser
participant server

    user->>browser: Fill form and submit

    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server
    Note right of server: Server adds new note to notes array
    server-->>browser: JSON of the created note
    deactivate server

    Note right of browser: Browser updates the UI without reloading the page
