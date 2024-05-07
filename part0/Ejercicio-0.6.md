0.6: Nueva nota en diagrama de aplicación de una sola pagina.

Crea un diagrama que represente la situación en la que el usuario crea una nueva nota utilizando la versión de una sola página de la aplicación.


``` mermaid
sequenceDiagram
    Browser->>Browser: Nueva nota y Guardar
    
    Browser->>Browser: Envío del formulario y evitamos el manejo por defecto del envío de formulario.
    
    Browser->>+Server: HTTP POST /new_note_spa como data JSON 
    
    Server-->>-Browser: Response HTTP 201 guardado
    
    Browser->>Browser: Actualiza la lista
```

https://fullstackopen.com/es/part0/fundamentos_de_las_aplicaciones_web#ejercicios-0-1-0-6