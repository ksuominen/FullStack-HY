```mermaid
sequenceDiagram
participant browser
participant server

    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server

    Note right of browser: The browser sends the content of the note to /new_note_spa

    server-->>browser: response 201 created
    deactivate server

    Note right of browser: The browser does not redirect to /spa.<br/>Instead, the JavaScript code generates an eventhandler which<br/>gets the content of the form and adds the new note to the list.
```
