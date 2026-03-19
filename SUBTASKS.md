# Tasking

## HU001 - Registro de Arrendador

### Perspectiva Dev

#### DEV-F (Desarrollo Funcional)
| id | Descripción de tarea |
|----|----------------------|
| TD001 | Crear tabla usuarios en BD con campos: id, nombre, correo, contraseña(Hash), teléfono, rol, fecha de creación |
| TD002 | Crear modelo/entidad Usuario y DTOs |
| TD003 | Implementar endpoint POST /api/register |
| TD004 | Implementar validaciones de datos y manejo de errores en el endpoint de registro |

#### DEV-NF (Desarrollo No Funcional)
| id | Descripción de tarea |
|----|----------------------|
| TD005 | Implementar validaciones de entrada(formato de correo, longitud mínima de contraseña, formato de teléfono, campos requeridos) |
| TD006 | Implementar manejo de errores código HTTP y mensajes de error claros |
| TD007 | Implementar hashing de contraseña para almacenamiento seguro |

### Perspectiva QA
#### QA-F (QA Funcional)
| id | Descripción de tarea |
|----|----------------------|
| TQA001 | Caso de prueba: verificar que el endpoint /api/register con el método POST crea el usuario con todos sus campos  |
| TQA002 | Caso de prueba: verificar que no pueden existir dos correos iguales |
| TQA003 | Caso de prueba: verificar que el rol con el que se crea el usuario es arrendador |
| TQA004 | Caso de prueba: verificar que al envíar campos vacíos no se registre el usuario y se muestre un mensaje de error |

#### QA-NF (QA No Funcional)
| id | Descripción de tarea |
|----|----------------------|
| TQA005 | Caso de prueba: verificar que el endpoint /api/register con el método POST al crera el usuario con todos sus campos devuelva un código 201 con los datos y el fromato correspondiente |
| TQA006 | Caso de prueba: verificar que el endpoint /api/register con el método POST al crera el usuario con campos inválidos devuelva un mensaje y código de error|
| TQA007 | Caso de prueba: verificar que el endpoint /api/register con el método POST al crera el usuario con campos vacíos devuelva un mensaje y código de error|

## HU002 - Registro de Arrendatario
### Perspectiva Dev
#### DEV-F (Desarrollo Funcional)
| id | Descripción de tarea |
|----|----------------------|
| TD008 | Verificar que ya existe o Crear tabla usuarios en BD con campos: id, nombre, correo, contraseña(Hash), teléfono, rol, fecha de creación |
| TD009 | Verificar que ya existe o Crear modelo/entidad Usuario y DTOs |
| TD010 | Implementar endpoint POST /api/register |
| TD011 | Implementar validaciones de datos y manejo de errores en el endpoint de registro |

#### DEV-NF (Desarrollo No Funcional)
| id | Descripción de tarea |
|----|----------------------|
| TD012 | Implementar validaciones de entrada(formato de correo, longitud mínima de contraseña, formato de teléfono, campos requeridos) |
| TD013 | Implementar manejo de errores código HTTP y mensajes de error claros |
| TD014 | Implementar hashing de contraseña para almacenamiento seguro |

### Perspectiva QA
#### QA-F (QA Funcional)
| id | Descripción de tarea |
|----|----------------------|
| TQA008 | Caso de prueba: verificar que el endpoint /api/register con el método POST crea el usuario con todos sus campos  |
| TQA009 | Caso de prueba: verificar que no pueden existir dos correos iguales |
| TQA010 | Caso de prueba: verificar que el rol con el que se crea el usuario es arrendatario |
| TQA011 | Caso de prueba: verificar que al envíar campos vacíos no se registre el usuario y se muestre un mensaje de error |

#### QA-NF (QA No Funcional)
| id | Descripción de tarea |
|----|----------------------|
| TQA012 | Caso de prueba: verificar que el endpoint /api/register con el método POST al crear el usuario con todos sus campos devuelva un código 201 con los datos y el fromato correspondiente |
| TQA013 | Caso de prueba: verificar que el endpoint /api/register con el método POST al crear el usuario con campos inválidos devuelva un mensaje y código de error|
| TQA014 | Caso de prueba: verificar que el endpoint /api/register con el método POST al crear el usuario con campos vacíos devuelva un mensaje y código de error|

## HU003 - Inicio de Sesión
### Perspectiva Dev
#### DEV-F (Desarrollo Funcional)
| id | Descripción de tarea |
|----|----------------------|
| TD015 | Implementar endpoint POST /api/login con validación de credenciales |
| TD016 | Implementar generación de token JWT para autenticación |
| TD017 | Implementar redirección con datos de usuario y rol |

#### DEV-NF (Desarrollo No Funcional)
| id | Descripción de tarea |
|----|----------------------|
| TD018 | Implementar manejo de errores código HTTP y mensajes de error claros |
| TD019 | Implementar comparación de contraseñas con hashing |

### Perspectiva QA
#### QA-F (QA Funcional)
| id | Descripción de tarea |
|----|----------------------|
| TQA015 | Caso de prueba: verificar que el endpoint /api/login con el método POST valide las credenciales |
| TQA016 | Caso de prueba: verificar la generación de token JWT para autenticación |
| TQA017 | Caso de prueba: verificar que si el token está malformado o ha expirado que deniegue el acceso al sistema |
| TQA018 | Caso de prueba: verificar que las redirecciones están funcionando correctamente dependiendo del usuario y el rol |
| TQA019 | Caso de prueba: verificar que el endpoint /api/login con el método POST al poner credenciales inválidas no de acceso al sistema |
| TQA020 | Caso de prueba: verificar que al envíar campos vacíos no se inice sesión al usuario y se muestre un mensaje de error |

#### QA-NF (QA No Funcional)
| id | Descripción de tarea |
|----|----------------------|
| TQA021 | Caso de prueba: Verificar manejo de errores código HTTP y mensajes de error claros |

## HU004 - Publicar Propiedad
### Perspectiva Dev
#### DEV-F (Desarrollo Funcional)
| id | Descripción de tarea |
|----|----------------------|
| TD020 | Crear tabla propiedades en BD con campos: id, titulo, direccion, descripcion, precio_alquiler, imagenes, fecha_publicacion, arrendador_id, fecha_actualizacion |
| TD021 | Crear modelo/entidad Propiedad y DTOs |
| TD022 | Implementar endpoint POST /api/properties para publicar una propiedad (solo accesible por arrendadores) |

#### DEV-NF (Desarrollo No Funcional)
| id | Descripción de tarea |
|----|----------------------|
| TD023 | Implementar validaciones de entrada(formato de datos, campos requeridos) |
| TD024 | Implementar manejo de errores código HTTP y mensajes de error claros |

### Perspectiva QA
#### QA-F (QA Funcional)
| id | Descripción de tarea |
|----|----------------------|
| TQA022 | Caso de prueba: Verificar que el endpoint POST /api/properties sea sólo accesible por arrendatarios |
| TQA023 | Caso de prueba: Verificar que el endpoint POST /api/properties cree la propiedad con sus datos |
| TQA024 | E2E: Inicio de sesión -> Creación de publicación |
| TQA025 | Caso de prueba: verificar que al envíar campos vacíos no se publique la propiedad y se muestre un mensaje de error |

#### QA-NF (QA No Funcional)
| id | Descripción de tarea |
|----|----------------------|
| TQA026 | Caso de prueba: Verificar que el endpoint POST /api/properties devuelva un código y mensaje de error y si no cumple con las restricciones de los datos |

## HU005 - Visualizar Propiedades Disponibles
### Perspectiva Dev
#### DEV-F (Desarrollo Funcional)
| id | Descripción de tarea |
|----|----------------------|
| TD025 | Implementar endpoint GET /api/properties para listar propiedades disponibles |
| TD026 | Componente frontend para mostrar lista de propiedades con detalles (titulo, direccion, descripcion, precio_alquiler, imagenes) |

#### DEV-NF (Desarrollo No Funcional)
| id | Descripción de tarea |
|----|----------------------|
| TD027 | Implementar manejo de errores código HTTP y mensajes de error claros |
| TD028 | Implementar paginación para la lista de propiedades |

### Perspectiva QA
#### QA-F (QA Funcional)
| id | Descripción de tarea |
|----|----------------------|
| TQA027 | Caso de prueba: Verificar que el endpoint GET /api/properties lista las propiedades disponibles |

#### QA-NF (QA No Funcional)
| id | Descripción de tarea |
|----|----------------------|
| TQA028 | Caso de prueba: Verificar que las propiedades se listan en base a la paginación |

## HU006 - Aplicar para alquilar propiedad
### Perspectiva Dev
#### DEV-F (Desarrollo Funcional)
| id | Descripción de tarea |
|----|----------------------|
| TD029 | Crear tabla aplicaciones en BD con campos: id, propiedad_id, arrendatario_id, fecha_aplicacion, estado (pendiente, aceptada, rechazada) |
| TD030 | Crear modelo/entidad Aplicacion y DTOs |
| TD031 | Implementar endpoint POST /api/apply para que arrendatarios apliquen a una propiedad |

#### DEV-NF (Desarrollo No Funcional)
| id | Descripción de tarea |
|----|----------------------|
| TD032 | Implementar validaciones (propiedad existe, arrendatario existe) |
| TD033 | Implementar manejo de errores código HTTP y mensajes de error claros |
| TD034 | Implementar lógica para evitar múltiples aplicaciones a la misma propiedad por el mismo arrendatario |

### Perspectiva QA
#### QA-F (QA Funcional)
| id | Descripción de tarea |
|----|----------------------|
| TQA029 | Caso de prueba: Verificar que el endpoint POST /api/apply sea sólo accesible por arrendatarios |
| TQA030 | Caso de prueba: Verificar que el endpoint POST /api/apply cree correctamente la aplicación con el código de estado pendiente |

#### QA-NF (QA No Funcional)
| id | Descripción de tarea |
|----|----------------------|
| TQA031 | Caso de prueba: Verificar que si la propiedad no existe que la aplicación no se cree |
| TQA032 | Caso de prueba: Verificar que los códigos de errores funcionan y que los mensajes son claros |
| TQA033 | Caso de prueba: Verificar que no se pueden hacer dos o más aplicaciones a la misma propiedad |

## HU007 - Evaluar perffil financiero del arrendatario
### Perspectiva Dev
#### DEV-F (Desarrollo Funcional)
| id | Descripción de tarea |
|----|----------------------|
| TD034 | Implementar servicio de evaluación financiera con las reglas de negocio (bajo, medio, alto) |
| TD035 | Integrar evaluación automática al recibir solicitud de alquiler |
| TD036 | Almacenar resultado de la evaluación en la solicitud |

#### DEV-NF (Desarrollo No Funcional)
| id | Descripción de tarea |
|----|----------------------|
| TD037 | Implementar manejo de errores código HTTP y mensajes de error claros |

### Perspectiva QA
#### QA-F (QA Funcional)
| id | Descripción de tarea |
|----|----------------------|
| TQA034 | Caso de prueba: Verificar que la evaluación automática se determine de forma correcta en base a las reglas de negocio |
| TQA035 | Caso de prueba: Verificar que el resutlado se almacene en la solicitud |

#### QA-NF (QA No Funcional)
| id | Descripción de tarea |
|----|----------------------|
| TQA036 | Caso de prueba: Verificar que los códigos de errores funcionan y que los mensajes son claros |

## HU008 - Cálculo Dinámico del Depósito de Garantía
### Perspectiva Dev
#### DEV-F (Desarrollo Funcional)
| id | Descripción de tarea |
|----|----------------------|
| TD038 | Implementar lógica para calcular depósito de garantía basado en el score financiero |
| TD039 | Integrar cálculo dinámico al proceso de solicitud para alquilar propiedad |
| TD040 | Mostrar monto del depósito de garantía en la solicitud |

#### DEV-NF (Desarrollo No Funcional)
| id | Descripción de tarea |
|----|----------------------|
| TD041 | Implementar manejo de errores código HTTP y mensajes de error claros |

### Perspectiva QA
#### QA-F (QA Funcional)
| id | Descripción de tarea |
|----|----------------------|
| TQA037 | x |

#### QA-NF (QA No Funcional)
| id | Descripción de tarea |
|----|----------------------|
| TQA038 | x |

## HU009 - Generación de Contrato de Arrendamiento
### Perspectiva Dev
#### DEV-F (Desarrollo Funcional)
| id | Descripción de tarea |
|----|----------------------|
| TD042 | Implementar generación automática de contrato de arrendamiento en formato PDF |
| TD043 | Crear tabla contratos con metadatos en BD con campos: id, propiedad_id, arrendatario_id, arrendador_id, fecha_inicio, fecha_fin, deposito_garantia, ruta_contrato_pdf , solicitud_id, estado |
| TD044 | Endpoint para generar contrato al aprobar solicitud de alquiler |

#### DEV-NF (Desarrollo No Funcional)
| id | Descripción de tarea |
|----|----------------------|
| TD045 | Implementar manejo de errores código HTTP y mensajes de error claros |
| TD046 | Implementar lógica para evitar generación de múltiples contratos para la misma solicitud |

### Perspectiva QA
#### QA-F (QA Funcional)
| id | Descripción de tarea |
|----|----------------------|
| T001 | x |

#### QA-NF (QA No Funcional)
| id | Descripción de tarea |
|----|----------------------|
| T002 | x |