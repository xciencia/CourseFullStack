```mermaid
sequenceDiagram
box Acceder a SPA
    actor usuario as usuario
    participant browser as browser
    participant server as server
end
usuario->>browser: Write: https://studies.cs.helsinki.fi/exampleapp/spa

browser->>server: GET: https://studies.cs.helsinki.fi/exampleapp/spa
server->>browser: Html document

browser->>server: GET: https://studies.cs.helsinki.fi/exampleapp/main.css
server->>browser: file css

browser->>server: GET: https://studies.cs.helsinki.fi/exampleapp/spa.js
server->>browser: file js

browser->>server: GET: https://studies.cs.helsinki.fi/exampleapp/data.json
server->>browser: file json

note over browser: redrawNotes, write note in Tag <ul>

browser->>server: GET: https://studies.cs.helsinki.fi/favicon.ico
server->>browser: 404 Not found

