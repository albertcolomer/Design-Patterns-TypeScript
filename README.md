# Design Patterns TypeScript

## Creation

#### Singleton

- Caso:

	* Crear una clase para inicializar los parametros de configuracion de nuestro proyecto.


- Pruebas unitarias:

	* La instancia obtenida tiene q ser distinta de null
	* Llamar 2veces getinstance() asignales distintas variables y comprobar que son el mismo objeto
	* Comprobar que se leyeron los parametros correctamente

#### Factory

- Caso: 

	* Procesar ordenes de compra y calcular el costo segun el metodo de pago (PayPal 6%, Visa 5%, MasterCard 4%)
	

- Pruebas unitarias para cada metodo de pago:

	* Comprobar si coincide que el objeto sea del tipo correspondiente
	* Comprobar que la comision sea la correspondiente

#### Abstract Factory

- Caso:

	* Publicar un mensaje en distintas redes sociales.
	

- Pruebas unitarias:

	* Comprobar que el conector usado es el concreto.

## Structural
#### Adapter

- Caso:

	* Tenemos nuestro legacy code que permite publicar en nuestro fanpage de facebook. Queremos anadir otra red social, Slack que usa otro metodo y un parametro adicional.
	

- Pruebas unitarias:

	* Comprobar que las clases con las que trabaje hacen uso de la interfaz INotification.
	

#### Decorator  

- Caso:

	* Tenemos una tienda de musica y estamos en plena campaña, queremos ofrecer distintos descuentos
	

- Pruebas unitarias:

	* Comprobar que al cambiar customer aplica el descuento correcto

#### Proxy 

- Caso:

	* Queremos acceder a la playlist de un canal publicado en youtube(simulado).
	Los videos se muestran en nuestra pagina y se estima 1500 visitas/dia
	

- Pruebas unitarias:
	* Instancia de videoproxy para conectarse a los servidores simulados youtube
	* getPlaylist() muestra cuanto tiempo tarda en ejecutarse el mismo, el primero debe ser mayor de 3seg, el resto 0seg 



## Behavior
#### Command 

- Caso:

	* Un cliente hace un pago y tenemos varios proveedores de cobro
	

- Pruebas unitarias:

	* Creamos una tarjeta de credito y un pago de 300 unidades, inicializar paymentMethodHandler()
	providerName=Culqui denegacion, ordenamiento en cola

#### Observer  

- Caso:

	* Mandar un sms y email al usuario para confirmar su orden de compra
	

- Pruebas unitarias:

	* Instanciamos los observadores (sms , email) y el sujeto shopingCard
	Vemos como el sujeto notifica a los obervadores suscritos

#### Strategy  

- Caso:

	* Nuestro modulo de Checkout trabaja con PayPal pronto añadiran Visa y MasterCard
	

- Pruebas unitarias:

	* Instanciamos Checkout(), creamos un usuario, resolvemos que algoritmo usar