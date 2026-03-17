# Historias de Usuarios

# EP01 - Gestión de Usuarios

## HU001 - Registro de Arrendador

***Como*** arrendador(propietario)
***Quiero*** registrarme en la plataforma con mis datos personales(nombre, correo electrónico, contraseña, teléfono)
***Para*** poder publicar mis propiedades y gestionar el flujo de alquiler

### Criterios de aceptación

#### CA001 Escenario: Registro exitoso del arrendador

***Dado*** que el arrendador ingresa sus datos personales válidos en el formulario de registro  
***Cuando*** envía el formulario de registro  
***Entonces*** se crea la cuenta con rol *arrendador* y muestra un mensaje de confirmación de registro exitoso


---
#### CA002 Escenario: Registro fallido por correo electrónico ya registrado

***Dado*** que el arrendador ingresa un correo electrónico que ya está registrado en el sistema  
***Cuando*** envía el formulario de registro  
***Entonces*** muestra un mensaje de error indicando que el correo electrónico ya está en uso y no se crea la cuenta


---
#### CA003 Escenario: Registro fallido por datos inválidos

***Dado*** que el arrendador ingresa datos personales inválidos en el formulario de registro o deja campos vacíos  
***Cuando*** envía el formulario de registro  
***Entonces*** muestra un mensaje de error indicando que los datos ingresados son inválidos y no se crea la cuenta

### Story Points: Fibonacci

---
## HU002 - Registro de Arrendatario

***Como*** arrendatario(inquilino)
***Quiero*** registrarme en la plataforma con mis datos personales(nombre, correo electrónico, contraseña, teléfono)
***Para*** poder buscar y alquilar propiedades disponibles en la plataforma

### Criterios de aceptación

#### CA001 Escenario: Registro exitoso del arrendatario

***Dado*** que el arrendatario ingresa sus datos personales válidos en el formulario de registro  
***Cuando*** envía el formulario de registro  
***Entonces*** se crea la cuenta con rol *arrendatario* y muestra un mensaje de confirmación de registro exitoso

---
#### CA002 Escenario: Registro fallido por correo electrónico ya registrado

***Dado*** que el arrendatario ingresa un correo electrónico que ya está registrado en el sistema  
***Cuando*** envía el formulario de registro  
***Entonces*** muestra un mensaje de error indicando que el correo electrónico ya está en uso y no se crea la cuenta


---
#### CA003 Escenario: Registro fallido por datos inválidos

***Dado*** que el arrendatario ingresa datos personales inválidos en el formulario de registro o deja campos vacíos  
***Cuando*** envía el formulario de registro  
***Entonces*** muestra un mensaje de error indicando que los datos ingresados son inválidos y no se crea la cuenta

### Story Points: Fibonacci
---

## HU003 - Inicio de Sesión

***Como*** usuario(arrendador o arrendatario)
***Quiero*** iniciar sesión en la plataforma con mi correo electrónico y contraseña
***Para*** poder acceder a las funcionalidades de la plataforma correspondientes según mi rol

### Criterios de aceptación

#### CA001 Escenario: Inicio de sesión exitoso

***Dado*** que el usuario ingresa un correo electrónico y contraseña válidos registrados en el sistema  
***Cuando*** envía el formulario de inicio de sesión  
***Entonces*** se permite el acceso y dirige al usuario a la pantalla principal

### Story Points: Fibonacci


# EP02 - Gestión de Propiedades

## HU004 - Publicar Propiedad

***Como*** arrendador(propietario)
***Quiero*** publicar una propiedad en la plataforma con detalles como título, dirección, descripción, precio de alquiler, imágenes y características.
***Para*** que los arrendatarios puedan visualizarla y aplicar para alquilarla.

### Criterios de aceptación

#### CA001 Escenario: Publicación exitosa de la propiedad

***Dado*** que el arrendador ingresa todos los detalles requeridos de la propiedad de manera válida  
***Cuando*** envía el formulario de publicación
***Entonces*** se crea la propiedad y se muestra un mensaje de confirmación de publicación exitosa