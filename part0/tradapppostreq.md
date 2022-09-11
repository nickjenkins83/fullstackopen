title Post Note (traditional app)

browser->server: HTTP POST https://studies.cs.helsinki.fi/exampleapp/new_note
server-->browser: 302 REDIRECT
note over browser:
browser executes js to append input to the JSON data 
via html <li> element
and sends a 302 Redirect for /exampleapp/notes
end note
browser->server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/main.css
server-->browser: main.css
browser->server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/main.js
server-->browser: main.js

note over browser:
browser starts executing js-code
that requests JSON data from server 
end note

browser->server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/data.json
server-->browser: [{ content: "world hello", date: "2022-09-11" }, ...]

note over browser:
browser executes the event handler
that renders notes to display
end note
