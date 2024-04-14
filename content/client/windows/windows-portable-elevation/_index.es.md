---
title: Windows Portable Elevation
weight: 4
---

Los programas portables de Windows no tienen privilegios de administrador, esto puede causar los siguientes problemas:

- La pantalla no puede ser transmitida mientras se muestra la pantalla de UAC (User Account Control).
- cuando alguna ventana de alguna aplicación ejecutada con derechos de administrador esta abierta, el puntero no responderá al control remoto.

Mediante la elevación de privilegios, RustDesk puede crear un proceso con privilegios de administrador al iniciar el equipo o al sesión de usuario de esta manera evita los problemas antes mencionados.

### Elevación al encendido del equipo

Mediante estos métodos, los usuarios remotos no necesitan pedir la elevación de permisos cuando se conectan

* Método 1: Agrega esta linea `-qs-` al nombre del ejecutable portable (las versiones 1.2.0, 1.2.1, 1.2.2 terminan con `qs.exe`). Ejecuta el archivo y da en `Aceptar` en la ventana de UAC

* Método 2: Click secundario y ejecutar como administrador


### Elevar en el lado controlado

El lado controlado puede hacer click en `Aceptar y Elevar` cuando se este conectando o hacer click en `Elevate` una vez este conectado.

| Conectando | Conectado |
| :---: | :---: |
| ![](images/cm_unauth.jpg) | ![](images/cm_auth.jpg) |

### Pide la elevación de permisos del lado controlador

Después de seleccionar en el menu de acción `Solicitar Elevación`, la siguiente ventana va a aparecer. si elegís `Preguntar al remoto por autenticación`, no necesitaras ingresar un usuario y contraseña, pero el usuario remoto deberá tener permisos de administrador. si seleccionas `Transmitir el nombre de usuario y contraseña del administrador`, el usuario remoto solo debe aceptar la petición del UAC. Después de enviar la petición, espera a que el usuario remoto confirme el dialogo del UAC. Una vez confirmado, un mensaje de éxito aparecerá. Ten en cuenta que **ambos métodos necesitan a alguien en la maquina controlada para confirmar el dialogo UAC**. Por lo tanto si no hay nadie en el lado controlado, la elevación no debe pedirse desde el lado de control.   

| Menu | Dialogo |
| :---: | :---: |
| ![](images/menu.png) | ![](images/dialog.png) |
| **Wait** | **Success** |
| ![](images/wait.png) | ![](images/success.png) |

### How to Choose

| Situación | Método |
| :---: | :---: |
| No elevación requerida | Instala el programa |
| Usuario no disponible en el lado controlado | Renombra<br/>*o*<br/> Ejecuta como administrador |
| Usuario disponible en el lado controlado<br/>*and*<br/> Elevación inmediata en la conexión<br/>*y*<br/> Aceptar conexión mediante click | Hace click en `Aceptar y elevar` Cuando recibas la conexión del lado controlador |
| Usuario disponible en el lado controlador<br/>*y*<br/> Elevación Es necesaria | Hace click en `Elevar` en la ventana de control de la conexión en el lado controlado<br/>*o*<br/> Pide la elevación en el lado controlador |
