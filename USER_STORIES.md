# Historias de Usuarios

# EP01 - Gestión de Usuarios

## HU001 - Registro de Arrendador

**Como** arrendador(propietario)
**Quiero** registrarme en la plataforma con mis datos personales(nombre, correo electrónico, contraseña, teléfono)
**Para** poder publicar mis propiedades y gestionar el flujo de alquiler

### Criterios de aceptación

#### CA001 Escenario: Registro exitoso del arrendador

**Dado** que el arrendador ingresa sus datos personales válidos en el formulario de registro  
**Cuando** envía el formulario de registro  
**Entonces** se crea la cuenta con rol *arrendador* y muestra un mensaje de confirmación de registro exitoso


---
#### CA002 Escenario: Registro fallido por correo electrónico ya registrado

**Dado** que el arrendador ingresa un correo electrónico que ya está registrado en el sistema  
**Cuando** envía el formulario de registro  
**Entonces** muestra un mensaje de error indicando que el correo electrónico ya está en uso y no se crea la cuenta


---
#### CA003 Escenario: Registro fallido por datos inválidos

**Dado** que el arrendador ingresa datos personales inválidos en el formulario de registro o deja campos vacíos  
**Cuando** envía el formulario de registro  
**Entonces** muestra un mensaje de error indicando que los datos ingresados son inválidos y no se crea la cuenta

### Story Points: Fibonacci

---
## HU002 - Registro de Arrendatario

**Como** arrendatario(inquilino)
**Quiero** registrarme en la plataforma con mis datos personales(nombre, correo electrónico, contraseña, teléfono)
**Para** poder buscar y alquilar propiedades disponibles en la plataforma

### Criterios de aceptación

#### CA001 Escenario: Registro exitoso del arrendatario

**Dado** que el arrendatario ingresa sus datos personales válidos en el formulario de registro  
**Cuando** envía el formulario de registro  
**Entonces** se crea la cuenta con rol *arrendatario* y muestra un mensaje de confirmación de registro exitoso

---
#### CA002 Escenario: Registro fallido por correo electrónico ya registrado

**Dado** que el arrendatario ingresa un correo electrónico que ya está registrado en el sistema  
**Cuando** envía el formulario de registro  
**Entonces** muestra un mensaje de error indicando que el correo electrónico ya está en uso y no se crea la cuenta


---
#### CA003 Escenario: Registro fallido por datos inválidos

**Dado** que el arrendatario ingresa datos personales inválidos en el formulario de registro o deja campos vacíos  
**Cuando** envía el formulario de registro  
**Entonces** muestra un mensaje de error indicando que los datos ingresados son inválidos y no se crea la cuenta

### Story Points: Fibonacci
---

## HU003 - Inicio de Sesión

**Como** usuario(arrendador o arrendatario)
**Quiero** iniciar sesión en la plataforma con mi correo electrónico y contraseña
**Para** poder acceder a las funcionalidades de la plataforma correspondientes según mi rol

### Criterios de aceptación

#### CA001 Escenario: Inicio de sesión exitoso

**Dado** que el usuario ingresa un correo electrónico y contraseña válidos registrados en el sistema  
**Cuando** envía el formulario de inicio de sesión  
**Entonces** se permite el acceso y dirige al usuario a la pantalla principal

#### CA002 Escenario: Inicio de sesión con campos vacíos

**Dado** que el usuario ingresa un correo electrónico y/o contraseña vacíos
**Cuando** envía el formulario de inicio de sesión  
**Entonces** se deniega el acceso con un mensaje que diga que los campos no pueden ser vacíos

#### CA003 Escenario: Inicio de sesión con campos invalidos

**Dado** que el usuario ingresa un correo electrónico y/o contraseña inválidos
**Cuando** envía el formulario de inicio de sesión  
**Entonces** se deniega el acceso con un mensaje que diga que las credenciales son inválidas

### Story Points: Fibonacci

---
# EP02 - Gestión de Propiedades

## HU004 - Publicar Propiedad

**Como** arrendador(propietario)
**Quiero** publicar una propiedad en la plataforma con detalles como título, dirección, descripción, precio de alquiler e imágenes
**Para** que los arrendatarios puedan visualizarla y aplicar para alquilarla.

### Criterios de aceptación

#### CA001 Escenario: Publicación exitosa de la propiedad

**Dado** que el arrendador ingresa todos los detalles requeridos de la propiedad de manera válida  
**Cuando** envía el formulario de publicación  
**Entonces** se crea la propiedad y se muestra un mensaje de confirmación de publicación exitosa

### Story Points: Fibonacci
---
## HU005 - Visualizar Propiedades Disponibles

**Como** arrendatario(inquilino)
**Quiero** visualizar las propiedades disponibles para alquilar en la plataforma con sus detalles como título, dirección, descripción, precio de alquiler e imágenes.
**Para** poder elegir una propiedad que se ajuste a mis necesidades y aplicar para alquilarla.

### Criterios de aceptación

#### CA001 Escenario: Visualización de propiedades disponibles

**Dado** que existen propiedades publicadas en la plataforma  
**Cuando** el arrendatario accede a la sección de propiedades disponibles  
**Entonces** se muestran las propiedades con sus detalles correspondientes

### Story Points: Fibonacci
---
## HU006 - Aplicar para Alquilar Propiedad
**Como** arrendatario(inquilino)
**Quiero** solicitar el alquiler de una propiedad disponible en la plataforma
**Para** iniciar el proceso de evaluación financiera y poder alquilar la propiedad.

### Criterios de aceptación
#### CA001 Escenario: Aplicación exitosa para alquilar propiedad

**Dado** que el arrendatario ha seleccionado una propiedad disponible  
**Cuando** envía la solicitud para alquilar la propiedad  
**Entonces** se registra la solicitud con estado *pendiente* y se muestra un mensaje de confirmación de aplicación exitosa

### Story Points: Fibonacci


---

# EP03 - Evaluación Financiera y Contratación

## HU007 - Evaluar Perfil Financiero del Arrendatario


**Supuestos**  
- **Nivel de riesgo bajo**: score crediticio >= 700, ingresos mensuales >= 3 veces el precio de alquiler y situación laboral empleado o independiente estable.  
- **Nivel de riesgo medio**: score crediticio entre 600 y 699, ingresos mensuales >= 2 veces el precio de alquiler y situación laboral empleado o independiente estable.  
- **Nivel de riesgo alto**: score crediticio < 600, ingresos mensuales < 2 veces el precio de alquiler o situación laboral desempleado o independiente inestable.    

---
**Como** arrendador(propietario)
**Quiero** que el sistema evalúe automáticamente el perfil financiero del arrendatario(score crediticio, ingresos mensuales y situación laboral) al recibir una solicitud de alquiler
**Para** conocer el nivel de riesgo del inquilino y tomar decisiones informadas sobre el alquiler de mi propiedad.

### Criterios de aceptación
#### CA001 Escenario: Perfil financiero con riesgo bajo

**Dado** que el arrendatario ha enviado una solicitud para alquilar una propiedad  
**Y**  tiene un score crediticio >= 700, ingresos mensuales >= 3 veces el precio de alquiler y situación laboral empleado o independiente estable.  
**Cuando** el sistema evalúa el perfil financiero del arrendatario
**Entonces** el perfil se clasifica como riesgo *bajo*

### Story Points: Fibonacci
---

 ## HU008 - Cálculo Dinámico del Depósito de Garantía

**Como** arrendador(propietario)
**Quiero** que el sistema calcule dinámicamente el depósito de garantía (1 a 3 meses) en base al score crediticio del arrendatario cuando aplique para alquilar mi propiedad 
**Para** proteger mi propiedad y reducir el riesgo financiero del inquilino.

### Criterios de aceptación

#### CA001 Escenario: Cálculo de depósito de garantía para perfil de riesgo bajo

**Dado** que el arrendatario tiene un score crediticio >= 700  
**Cuando** el sistema calcula el depósito de garantía para una solicitud de alquiler  
**Entonces** el depósito de garantía se establece en 1 mes de alquiler  

### Story Points: Fibonacci
---

## HU009 - Generación de Contrato de Arrendamiento

**Como** arrendador(propietario)
**Quiero** que el sistema genere automáticamente un contrato de arrendamiento en formato PDF con los datos del arrendatario, la propiedad, el depósito de garantía y el estado del contraro.
**Para** formalizar el acuerdo de alquiler de forma rápida y automatizada.

### Criterios de aceptación
#### CA001 Escenario: Generación exitosa de contrato de arrendamiento
**Dado** que la evaluación financiera del arrendatario y el cálculo del depósito se completaron exitosamente.  
**Cuando** el sistema genera el contrato de arrendamiento  
**Entonces** se crea un archivo PDF con los detalles del contrato y se muestra un mensaje de confirmación de generación exitosa.

### Story Points: Fibonacci
---