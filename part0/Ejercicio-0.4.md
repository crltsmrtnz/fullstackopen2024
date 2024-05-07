0.4: Nuevo diagrama de nota.

En el capítulo Cargando una página que contiene JavaScript - revisión la cadena de eventos causada al abrir la página https://studies.cs.helsinki.fi/exampleapp/notes se representa como un diagrama de secuencia


```mermaid
    sequenceDiagram
        Browser->>+Server: HTTP GET fullstackopen.com/notes
        Server-->>-Browser: HTML code
        Browser->>+Server: HTTP GET fullstackopen.com/main.css
        Server-->>-Browser: main.css
        Browser->>+Server: HTTP GET fullstackopen.com/main.js
        Server-->>-Browser: main.js
        Browser->>+Server: HTTP GET fullstackopen.com/data.json
        Server-->>-Browser: data JSON 

        Browser->>+Server: POST /new_note (form summit,send the data to server)
        Server-->>-Browser: HTTP 302, Redirect to /notes

        Browser->>+Server:  HTTP GET fullstackopen.com/notes
        Server-->>-Browser: Response /note HTML code
        Browser->>+Server: HTTP GET fullstackopen.com/main.css
        Server-->>-Browser: main.css
        Browser->>+Server: HTTP GET fullstackopen.com/main.js
        Server-->>-Browser: main.js
        Browser->>+Server: HTTP GET fullstackopen.com/data.json
        Server-->>-Browser: data JSON 
        Browser->>Browser: Actualiza la lista

```

https://fullstackopen.com/es/part0/fundamentos_de_las_aplicaciones_web#ejercicios-0-1-0-6