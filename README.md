# Api delilah_resto

π§ Api Delilah Resto Acamica

Tercer Proyecto de la carrera Desarrollo Web Full Stack en Acamica.


βοΈ Procedimiento :

## 1 - InstalaciΓ³n π©

Clonar proyecto desde la consola :

β¨οΈ git clone https://github.com/dilan280394/delilah_resto

## 2 - InstalaciΓ³n de dependencias π©


β¨οΈ npm install

## 3 - Crear base de datos π©


Importar el Archivo delilah.sql desde el panel de Administracion
Recuerde Editar el archivo configuracion/configuracion.js con los datos de su entorno.

## 4 - Iniciar el servidor π©


Abrir el archivo servidor.js desde VisualStudio y ejecutar en terminal :

β¨οΈ nodemon servidor.js

## 5 - Ya podes Utitlizar el Sistema ! π©


πππππππππππππππππππππππππ

## 6 ENDPOINT

localhost:3000/v1

| Metodo |       Enpoint      |           Body	        	|           Header	        	|                  Descripcion                           |
|--------|--------------------|-----------------------------|-------------------------------|--------------------------------------------------------|
|  POST  | /login             |{usuario,contraseΓ±a}		    |                   		    | Devuelve el Token del Usuario                          |
|   GET  | /usuarios          |                   		    |           {token }    		| Devuelve Informacion de todos los usuarios             |
|   GET  | /usuarios          |{usuario}    				|           {token }    		| Devuelve informacion de un Usuario 					 |
|  POST  | /usuarios          |{ usuario, nombre, apellido, |                   		    | Crea un Usuario                                        |
|		 |					  |	email, contrasena, telefono,|                   		    |                                                        |
|		 |					  | domicilio  }          		|                   		    |					                                     |
|   PUT  | /usuarios          |{ usuario, nombre, apellido, |           {token }    		| Modifica un Usuario                   (Solo Admin)     |
|        | 				      |	email, contrasena, telefono,|                   		    |                                                        |
|		 |					  | domicilio}          		|                   		    |                                                        |
| DELETE | /usuarios          |{usuario}    				|           {token }    		| Elimina un usuario                    (Solo Admin)     |
|--------|--------------------|-----------------------------|-------------------------------|--------------------------------------------------------|
|   GET  | /productos         |                      	    |                        	    | Devuelve todos los productos                           |
|   GET  | /productos         | {nombre}               	    |                   		    | Devuelve los productos que contengan la palabra buscada|
|  POST  | /productos         |{ nombre, precio, imagen,    |           {token }    		| Crea un Producto                      (Solo Admin)     |
|		 |					  |	descripcion}                |                   		    |                                                        |
|  PUT   | /productos         |{ id, nombre, precio, imagen,|           {token }    		| Modifica un Producto                   (Solo Admin)    |
|		 |					  |	descripcion}                |                   		    |                                                        |
| DELETE | /productos         |{id}	                  	    |           {token }    		| Elimina un producto                   (Solo Admin)     |
|--------|--------------------|-----------------------------|-------------------------------|--------------------------------------------------------|
|  GET   | /pedidos           |                      	    |           {token }    		| Muestra pedidos (si es Admin muestra todos )		     |
|  POST  | /pedidos      	  |{total, id_usuario,          |           {token }    		| Crea un Pedido                                         |
|		 |					  | productos[                  |                   		    |                                                        |
|		 |					  |{id_producto,cantidad,       |                   		    |                                                        |
|		 |					  | nombre_producto,precio}]}   |                   		    |                                                        |
|		 |				 	  |             				|                   		    |                                                        |
|  PUT   | /pedidos			  |{ estado , id_pedido }       |           {token }    		| Permite editar el Estado del Pedido   (Solo Admin)     |
| DELETE | /pedidos           |{id ,token}	        	    |           {token }    		| Elimina un pedido                     (Solo Admin)     |
|--------|--------------------|-----------------------------|-------------------------------|--------------------------------------------------------|


