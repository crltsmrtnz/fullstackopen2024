0.5: Diagrama de aplicación de una sola página.

Crea un diagrama que describa la situación en la que el usuario accede a la versión de aplicación de una sola página de la aplicación de notas en https://studies.cs.helsinki.fi/exampleapp/spa. 


```mermaid
    sequenceDiagram
        Browser->>+Server: HTTP GET fullstackopen.com/spa
        Server-->>-Browser: code HTML 
        
        Browser->>+Server: HTTP GET fullstackopen.com/main.css
        Server-->>-Browser: main.css
        
        Browser->>+Server: HTTP GET fullstackopen.com/spa.js
        Server-->>-Browser: spa.js
        
        Browser->>+Server: HTTP GET fullstackopen.com/data.json
        Server-->>-Browser: data JSON 
 

```

https://fullstackopen.com/es/part0/fundamentos_de_las_aplicaciones_web#ejercicios-0-1-0-6