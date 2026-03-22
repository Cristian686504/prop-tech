# Historias de Usuarios

# EP01 - Gestión de Usuarios

## HU001 - Registro de Arrendador

### Definition of Ready
- [ ] HU redactada en formato Como / Quiero / Para
- [ ] Valor de negocio claro
- [ ] Criterios de Aceptación definidos (mín. 2–3)
- [ ] Dependencias externas resueltas
- [ ] HU estimada por el equipo técnico

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

### Story Points: 3
### Definition of Done
- [ ] Código en repo — PR aprobado por al menos 1 par
- [ ] Cobertura de pruebas unitarias > 80%
- [ ] Pruebas funcionales de QA pasadas
- [ ] Sin bugs críticos o bloqueantes abiertos
- [ ] Todos los Criterios de Aceptación cumplidos


---
## HU002 - Registro de Arrendatario

### Definition of Ready
- [ ] HU redactada en formato Como / Quiero / Para
- [ ] Valor de negocio claro
- [ ] Criterios de Aceptación definidos (mín. 2–3)
- [ ] Dependencias externas resueltas
- [ ] HU estimada por el equipo técnico

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

### Story Points: 3

### Definition of Done
- [ ] Código en repo — PR aprobado por al menos 1 par
- [ ] Cobertura de pruebas unitarias > 80%
- [ ] Pruebas funcionales de QA pasadas
- [ ] Sin bugs críticos o bloqueantes abiertos
- [ ] Todos los Criterios de Aceptación cumplidos

---

## HU003 - Inicio de Sesión
### Definition of Ready
- [ ] HU redactada en formato Como / Quiero / Para
- [ ] Valor de negocio claro
- [ ] Criterios de Aceptación definidos (mín. 2–3)
- [ ] Dependencias externas resueltas
- [ ] HU estimada por el equipo técnico

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

#### CA003 Escenario: Inicio de sesión con credenciales invalidas

**Dado** que el usuario ingresa un correo electrónico y/o contraseña inválidos
**Cuando** envía el formulario de inicio de sesión  
**Entonces** se deniega el acceso con un mensaje que diga que las credenciales son inválidas

### Story Points: 5
### Definition of Done
- [ ] Código en repo — PR aprobado por al menos 1 par
- [ ] Cobertura de pruebas unitarias > 80%
- [ ] Pruebas funcionales de QA pasadas
- [ ] Sin bugs críticos o bloqueantes abiertos
- [ ] Todos los Criterios de Aceptación cumplidos
---
# EP02 - Gestión de Propiedades

## HU004 - Publicar Propiedad
### Definition of Ready
- [ ] HU redactada en formato Como / Quiero / Para
- [ ] Valor de negocio claro
- [ ] Criterios de Aceptación definidos (mín. 2–3)
- [ ] Dependencias externas resueltas
- [ ] HU estimada por el equipo técnico

**Como** arrendador(propietario)
**Quiero** publicar una propiedad en la plataforma con detalles como título, dirección, descripción, precio de alquiler e imágenes
**Para** que los arrendatarios puedan visualizarla y aplicar para alquilarla.

### Criterios de aceptación

#### CA001 Escenario: Publicación exitosa de la propiedad

**Dado** que el arrendador ingresa todos los detalles requeridos de la propiedad de manera válida  
**Cuando** envía el formulario de publicación  
**Entonces** se crea la propiedad y se muestra un mensaje de confirmación de publicación exitosa

#### CA002 Escenario: Publicación con campos vacíos

**Dado** que el arrendador no ingresa algun detalle requerido de la propiedad 
**Cuando** envía el formulario de publicación  
**Entonces** no se crea la propiedad y se muestra un mensaje que indique que los campos no pueden ser vacíos

#### CA003 Escenario: Publicación con un conjunto de imágenes que pesan más de 250MB

**Dado** que el arrendador sube un conjunto de imágenes que pesan más de 250MB
**Cuando** envía el formulario de publicación  
**Entonces** no se crea la propiedad y se muestra un mensaje que indique que el conjunto de imágenes no puede pesar más de 250MB

#### CA004 Escenario: Publicación con un título mayor a 255 carácteres

**Dado** que el arrendador ingresa un título con más de 255 carácteres
**Cuando** envía el formulario de publicación  
**Entonces** no se crea la propiedad y se muestra un mensaje que indique que el título no puede ser mayor a 255 carácteres

#### CA005 Escenario: Publicación con un dirección mayor a 255 carácteres

**Dado** que el arrendador ingresa una dirección con más de 255 carácteres
**Cuando** envía el formulario de publicación  
**Entonces** no se crea la propiedad y se muestra un mensaje que indique que la dirección no puede ser mayor a 255 carácteres

#### CA006 Escenario: Publicación con un descripción mayor a 2000 carácteres

**Dado** que el arrendador ingresa una descripción con más de 2000 carácteres
**Cuando** envía el formulario de publicación  
**Entonces** no se crea la propiedad y se muestra un mensaje que indique que la descripción no puede ser mayor a 2000 carácteres

#### CA007 Escenario: Publicación con un precio que no sea un número

**Dado** que el arrendador ingresa en el precio un valor distinto a un número
**Cuando** envía el formulario de publicación  
**Entonces** no se crea la propiedad y se muestra un mensaje que indique que el precio debe ser un valor numérico

#### CA008 Escenario: Usuario no autenticado intenta crear una publicación

**Dado** un usuario no autenticado
**Cuando** envía el formulario de publicación  
**Entonces** no se crea la propiedad y redirige al usuario a la pagina de inicio de sesión

#### CA009 Escenario: Usuario con un rol distinto a arrendador intenta crear una publicación

**Dado** un usuario con un rol distinto a arrendador
**Cuando** envía el formulario de publicación  
**Entonces** no se crea la propiedad y se muestra un mensaje que indique que no tiene autorización

### Story Points: 5

### Definition of Done
- [ ] Código en repo — PR aprobado por al menos 1 par
- [ ] Cobertura de pruebas unitarias > 80%
- [ ] Pruebas funcionales de QA pasadas
- [ ] Sin bugs críticos o bloqueantes abiertos
- [ ] Todos los Criterios de Aceptación cumplidos

---
## HU005 - Visualizar Propiedades Disponibles

### Definition of Ready
- [ ] HU redactada en formato Como / Quiero / Para
- [ ] Valor de negocio claro
- [ ] Criterios de Aceptación definidos (mín. 2–3)
- [ ] Dependencias externas resueltas
- [ ] HU estimada por el equipo técnico

**Como** arrendatario(inquilino)
**Quiero** visualizar las propiedades disponibles para alquilar en la plataforma con sus detalles como título, dirección, descripción, precio de alquiler e imágenes.
**Para** poder elegir una propiedad que se ajuste a mis necesidades y aplicar para alquilarla.

### Criterios de aceptación

#### CA001 Escenario: Visualización de propiedades disponibles

**Dado** que existen propiedades publicadas en la plataforma  
**Cuando** el arrendatario accede a la sección de propiedades disponibles  
**Entonces** se muestran las propiedades con sus detalles correspondientes

#### CA002 Escenario: No hay propiedades disponibles para visualizar

**Dado** que no existen propiedades publicadas en la plataforma  
**Cuando** el arrendatario accede a la sección de propiedades disponibles  
**Entonces** se muestra un mensaje de que actualmente no hay propiedades disponibles

#### CA003 Escenario: Usuario no autenticado quiere ver las propiedades disponibles

**Dado** un usuario no autenticado
**Cuando** accede a la sección de propiedades disponibles  
**Entonces** se le redirige a la página de inicio de sesión

### Story Points: 2

### Definition of Done
- [ ] Código en repo — PR aprobado por al menos 1 par
- [ ] Cobertura de pruebas unitarias > 80%
- [ ] Pruebas funcionales de QA pasadas
- [ ] Sin bugs críticos o bloqueantes abiertos
- [ ] Todos los Criterios de Aceptación cumplidos

---
## HU006 - Aplicar para Alquilar Propiedad

### Definition of Ready
- [ ] HU redactada en formato Como / Quiero / Para
- [ ] Valor de negocio claro
- [ ] Criterios de Aceptación definidos (mín. 2–3)
- [ ] Dependencias externas resueltas
- [ ] HU estimada por el equipo técnico


**Como** arrendatario(inquilino)
**Quiero** solicitar el alquiler de una propiedad disponible en la plataforma
**Para** iniciar el proceso de evaluación financiera y poder alquilar la propiedad.

### Criterios de aceptación
#### CA001 Escenario: Aplicación exitosa para alquilar propiedad

**Dado** que el arrendatario ha seleccionado una propiedad disponible  
**Cuando** envía la solicitud para alquilar la propiedad  
**Entonces** se registra la solicitud con estado *pendiente* y se muestra un mensaje de confirmación de aplicación exitosa

#### CA002 Escenario: El usuario envía la solicitud a una propiedad no disponible

**Dado** que el arrendatario ha seleccionado una propiedad no disponible  
**Cuando** envía la solicitud para alquilar la propiedad  
**Entonces** no se registra la solicitud y se muestra un mensaje que dice que la propiedad no está disponible

#### CA003 Escenario: Un usuario no autenticado envía la solicitud a una propiedad

**Dado** que el arrendatario ha seleccionado una propiedad
**Cuando** envía la solicitud para alquilar la propiedad  
**Entonces** no se registra la solicitud y se le redirige a la página de inicio de sesión
### Story Points: 3

### Definition of Done
- [ ] Código en repo — PR aprobado por al menos 1 par
- [ ] Cobertura de pruebas unitarias > 80%
- [ ] Pruebas funcionales de QA pasadas
- [ ] Sin bugs críticos o bloqueantes abiertos
- [ ] Todos los Criterios de Aceptación cumplidos
- [ ] Desplegada en ambiente de Staging
---

# EP03 - Evaluación Financiera y Contratación

## HU007 - Evaluar Perfil Financiero del Arrendatario

### Definition of Ready
- [ ] HU redactada en formato Como / Quiero / Para
- [ ] Valor de negocio claro
- [ ] Definir lógica de negocio para evaluar el perfil financiero del arrendatario
- [ ] Criterios de Aceptación definidos (mín. 2–3)
- [ ] Dependencias externas resueltas
- [ ] HU estimada por el equipo técnico

|Score crediticio|Ingresos mensuales vs Alquiler|Nivel de riesgo|
|----------------|------------------|---------------|
|>= 700          |>= 2x |Bajo |
|>= 700          |< 2x |Medio |
|>=500 y < 700   |>= 3x |Bajo |
|>=500 y < 700   |>= 2x y < 3x |Medio |
|>=500 y < 700   |< 2x |Alto |
|< 500          |>= 3x |Medio |
|< 500          |< 3x |Alto |


---
**Como** arrendador(propietario)
**Quiero** que el sistema evalúe automáticamente el perfil financiero del arrendatario(score crediticio, ingresos mensuales y situación laboral) al recibir una solicitud de alquiler
**Para** conocer el nivel de riesgo del inquilino y tomar decisiones informadas sobre el alquiler de mi propiedad.

### Criterios de aceptación
#### CA001 Escenario: Perfil financiero con riesgo bajo

**Dado** que el arrendatario ha enviado una solicitud para alquilar una propiedad  
**Y**  tiene un score crediticio >= 700, ingresos mensuales >= 2 veces el precio de alquiler  
**Cuando** el sistema evalúa el perfil financiero del arrendatario
**Entonces** el perfil se clasifica como riesgo *bajo*

#### CA002 Escenario: Perfil financiero con riesgo bajo

**Dado** que el arrendatario ha enviado una solicitud para alquilar una propiedad  
**Y**  tiene un score crediticio >=500 y < 700, ingresos mensuales >= 3 veces el precio de alquiler  
**Cuando** el sistema evalúa el perfil financiero del arrendatario
**Entonces** el perfil se clasifica como riesgo *bajo*

#### CA003 Escenario: Perfil financiero con riesgo medio

**Dado** que el arrendatario ha enviado una solicitud para alquilar una propiedad  
**Y**  tiene un score crediticio >= 700, ingresos mensuales < 2 veces el precio de alquiler  
**Cuando** el sistema evalúa el perfil financiero del arrendatario
**Entonces** el perfil se clasifica como riesgo *medio*

#### CA004 Escenario: Perfil financiero con riesgo medio

**Dado** que el arrendatario ha enviado una solicitud para alquilar una propiedad  
**Y**  tiene un score crediticio >=500 y < 700, ingresos mensuales >= 2x y < 3x veces el precio de alquiler  
**Cuando** el sistema evalúa el perfil financiero del arrendatario
**Entonces** el perfil se clasifica como riesgo *medio*

#### CA005 Escenario: Perfil financiero con riesgo medio

**Dado** que el arrendatario ha enviado una solicitud para alquilar una propiedad  
**Y**  tiene un score crediticio >=500 y < 700, ingresos mensuales >= 2x y < 3x veces el precio de alquiler  
**Cuando** el sistema evalúa el perfil financiero del arrendatario
**Entonces** el perfil se clasifica como riesgo *medio*

#### CA006 Escenario: Perfil financiero con riesgo medio

**Dado** que el arrendatario ha enviado una solicitud para alquilar una propiedad  
**Y**  tiene un score crediticio < 500, ingresos mensuales >= 3x veces el precio de alquiler  
**Cuando** el sistema evalúa el perfil financiero del arrendatario
**Entonces** el perfil se clasifica como riesgo *medio*

#### CA007 Escenario: Perfil financiero con riesgo alto

**Dado** que el arrendatario ha enviado una solicitud para alquilar una propiedad  
**Y**  tiene un score crediticio >=500 y < 700, ingresos mensuales < 2x veces el precio de alquiler  
**Cuando** el sistema evalúa el perfil financiero del arrendatario
**Entonces** el perfil se clasifica como riesgo *alto*

#### CA008 Escenario: Perfil financiero con riesgo alto

**Dado** que el arrendatario ha enviado una solicitud para alquilar una propiedad  
**Y**  tiene un score crediticio < 500, ingresos mensuales < 3x veces el precio de alquiler  
**Cuando** el sistema evalúa el perfil financiero del arrendatario
**Entonces** el perfil se clasifica como riesgo *alto*

### Story Points: 2

### Definition of Done
- [ ] Código en repo — PR aprobado por al menos 1 par
- [ ] Cobertura de pruebas unitarias > 80%
- [ ] Pruebas funcionales de QA pasadas
- [ ] Sin bugs críticos o bloqueantes abiertos
- [ ] Todos los Criterios de Aceptación cumplidos
- [ ] Desplegada en ambiente de Staging
---

 ## HU008 - Cálculo Dinámico del Depósito de Garantía

### Definition of Ready
- [ ] HU redactada en formato Como / Quiero / Para
- [ ] Valor de negocio claro
- [ ] Criterios de Aceptación definidos (mín. 2–3)
- [ ] Dependencias externas resueltas
- [ ] HU estimada por el equipo técnico

**Como** arrendador(propietario)
**Quiero** que el sistema calcule dinámicamente el depósito de garantía (1 a 3 meses) en base al nivel de riesgo evaluado del arrendatario cuando aplique para alquilar mi propiedad 
**Para** proteger mi propiedad y reducir el riesgo financiero del inquilino.

### Criterios de aceptación

#### CA001 Escenario: Cálculo de depósito de garantía para perfil de riesgo bajo

**Dado** que el arrendatario tiene un nivel de riesgo **bajo** según la evaluación financiera realizada por el sistema
**Cuando** el sistema calcula el depósito de garantía para una solicitud de alquiler  
**Entonces** el depósito de garantía se establece en 1 mes de alquiler 

#### CA002 Escenario: Cálculo de depósito de garantía para perfil de riesgo medio

**Dado** que el arrendatario tiene un nivel de riesgo **medio** según la evaluación financiera realizada por el sistema
**Cuando** el sistema calcula el depósito de garantía para una solicitud de alquiler  
**Entonces** el depósito de garantía se establece en 2 meses de alquiler  

#### CA003 Escenario: Cálculo de depósito de garantía para perfil de riesgo alto

**Dado** que el arrendatario tiene un nivel de riesgo **alto** según la evaluación financiera realizada por el sistema
**Cuando** el sistema calcula el depósito de garantía para una solicitud de alquiler  
**Entonces** el depósito de garantía se establece en 3 meses de alquiler  

### Story Points: 2

### Definition of Done
- [ ] Código en repo — PR aprobado por al menos 1 par
- [ ] Cobertura de pruebas unitarias > 80%
- [ ] Pruebas funcionales de QA pasadas
- [ ] Sin bugs críticos o bloqueantes abiertos
- [ ] Todos los Criterios de Aceptación cumplidos
- [ ] Desplegada en ambiente de Staging
---

## HU009 - Generación de Contrato de Arrendamiento

### Definition of Ready
- [ ] HU redactada en formato Como / Quiero / Para
- [ ] Valor de negocio claro
- [ ] Criterios de Aceptación definidos (mín. 2–3)
- [ ] Dependencias externas resueltas
- [ ] HU estimada por el equipo técnico

**Como** arrendador(propietario)
**Quiero** que el sistema genere automáticamente un contrato de arrendamiento en formato PDF con los datos del arrendatario, la propiedad, el depósito de garantía y el estado del contrato.
**Para** formalizar el acuerdo de alquiler de forma rápida y automatizada.

### Criterios de aceptación
#### CA001 Escenario: Generación exitosa de contrato de arrendamiento
**Dado** que la evaluación financiera del arrendatario y el cálculo del depósito se completaron exitosamente.  
**Cuando** el sistema genera el contrato de arrendamiento  
**Entonces** se crea un archivo PDF con los detalles del contrato y se muestra un mensaje de confirmación de generación exitosa.

#### CA002 Escenario: La evaluación financiera no se completó
**Dado** que la evaluación financiera del arrendatario no se completó  
**Cuando** el sistema genera el contrato de arrendamiento  
**Entonces** no se crea un archivo PDF con los detalles del contrato y se muestra un mensaje que dice que la evaluación financiera no se completó

#### CA003 Escenario: El calculo del depósito no se completó
**Dado** que el calculo del depósito no se completó  
**Cuando** el sistema genera el contrato de arrendamiento  
**Entonces** no se crea un archivo PDF con los detalles del contrato y se muestra un mensaje que dice que el calculo del depósito no se completó

### Story Points: 3

### Definition of Done
- [ ] Código en repo — PR aprobado por al menos 1 par
- [ ] Cobertura de pruebas unitarias > 80%
- [ ] Pruebas funcionales de QA pasadas
- [ ] Sin bugs críticos o bloqueantes abiertos
- [ ] Todos los Criterios de Aceptación cumplidos
- [ ] Desplegada en ambiente de Staging
---