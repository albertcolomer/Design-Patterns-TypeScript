# Design Patterns TypeScript




### Introducción


### Creation
* Singleton  

    Caso: Crear una clase para inicializar los parametros de configuracion de nuestro proyecto

    Pruebas unitarias
        - La instancia obtenida tiene q ser distinta de null
        - Llamar 2veces getinstance() asignales distintas variables y comprobar que son el mismo objeto
        - Comprobar que se leyeron los parametros correctamente

* Factory

    Caso: Procesar ordenes de compra y clacular el costo segun el metodo de pago (PayPal 6%, Visa 5%, MasterCard 4%)

    Pruebas unitarias para cada metodo de pago:   
        - Comprobar si coincide que el objeto sea del tipo correspondiente
        - Comprobar que la comision sea la correspondiente
    
* Abstract Factory  

    Caso: Publicar un mensaje en distintas redes sociales

    Pruebas unitarias:
        - Comprobar que conector el conector usado es el concreto

### Structural
* Adapter  
* Decorator  
* Proxy 

### Behavior
* Command - 
* Observer - 
* Strategy - 


