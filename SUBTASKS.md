# Tasking

## HU001 - Registro de Arrendador

### Perspectiva Dev

#### DEV-F (Desarrollo Funcional)
| id | Descripción de tarea |
|----|----------------------|
| T001 | Crear tabla usuarios en BD con campos: id, nombre, correo, contraseña(Hash), teléfono, rol, fecha de creación |
| T002 | Crear modelo/entidad Usuario y DTOs |
| T003 | Implementar endpoint POST /api/register |
| T004 | Implementar validaciones de datos y manejo de errores en el endpoint de registro |

#### DEV-NF (Desarrollo No Funcional)
| id | Descripción de tarea |
|----|----------------------|
| T005 | Implementar validaciones de entrada(formato de correo, longitud mínima de contraseña, formato de teléfono, campos requeridos) |
| T006 | Implementar manejo de errores código HTTP y mensajes de error claros |
| T007 | Implementar hashing de contraseña para almacenamiento seguro |

### Perspectiva QA
#### QA-F (QA Funcional)
| id | Descripción de tarea |
|----|----------------------|
| T001 | Caso de prueba: verificar que el endpoint /api/register con el método POST crea el usuario con todos sus campos  |
| T002 | Caso de prueba: verificar que no pueden existir dos correos iguales |
| T003 | Caso de prueba: verificar que el rol con el que se crea el usuario es arrendador |

#### QA-NF (QA No Funcional)
| id | Descripción de tarea |
|----|----------------------|
| T004 | Caso de prueba: verificar que el endpoint /api/register con el método POST al crera el usuario con todos sus campos devuelva un código 201 con los datos y el fromato correspondiente |
| T005 | Caso de prueba: verificar que el endpoint /api/register con el método POST al crera el usuario con campos inválidos devuelva un mensaje y código de error|
| T006 | Caso de prueba: verificar que el endpoint /api/register con el método POST al crera el usuario con campos vacíos devuelva un mensaje y código de error|

## HU002 - Registro de Arrendatario
### Perspectiva Dev
#### DEV-F (Desarrollo Funcional)
| id | Descripción de tarea |
|----|----------------------|
| T001 | Crear tabla usuarios en BD con campos: id, nombre, correo, contraseña(Hash), teléfono, rol, fecha de creación |
| T002 | Crear modelo/entidad Usuario y DTOs |
| T003 | Implementar endpoint POST /api/register |
| T004 | Implementar validaciones de datos y manejo de errores en el endpoint de registro |

#### DEV-NF (Desarrollo No Funcional)
| id | Descripción de tarea |
|----|----------------------|
| T005 | Implementar validaciones de entrada(formato de correo, longitud mínima de contraseña, formato de teléfono, campos requeridos) |
| T006 | Implementar manejo de errores código HTTP y mensajes de error claros |
| T007 | Implementar hashing de contraseña para almacenamiento seguro |

### Perspectiva QA
#### QA-F (QA Funcional)
| id | Descripción de tarea |
|----|----------------------|
| T001 | Caso de prueba: verificar que el endpoint /api/register con el método POST crea el usuario con todos sus campos  |
| T002 | Caso de prueba: verificar que no pueden existir dos correos iguales |
| T003 | Caso de prueba: verificar que el rol con el que se crea el usuario es arrendatario |

#### QA-NF (QA No Funcional)
| id | Descripción de tarea |
|----|----------------------|
| T004 | Caso de prueba: verificar que el endpoint /api/register con el método POST al crear el usuario con todos sus campos devuelva un código 201 con los datos y el fromato correspondiente |
| T005 | Caso de prueba: verificar que el endpoint /api/register con el método POST al crear el usuario con campos inválidos devuelva un mensaje y código de error|
| T006 | Caso de prueba: verificar que el endpoint /api/register con el método POST al crear el usuario con campos vacíos devuelva un mensaje y código de error|

## HU003 - Inicio de Sesión
### Perspectiva Dev
#### DEV-F (Desarrollo Funcional)
| id | Descripción de tarea |
|----|----------------------|
| T001 | Implementar endpoint POST /api/login con validación de credenciales |
| T002 | Implementar generación de token JWT para autenticación |
| T003 | Implementar redirección con datos de usuario y rol |

#### DEV-NF (Desarrollo No Funcional)
| id | Descripción de tarea |
|----|----------------------|
| T004 | Implementar manejo de errores código HTTP y mensajes de error claros |
| T005 | Implementar comparación de contraseñas con hashing |

### Perspectiva QA
#### QA-F (QA Funcional)
| id | Descripción de tarea |
|----|----------------------|
| T001 | Caso de prueba: verificar que el endpoint /api/login con el método POST valide las credenciales |
| T002 | Caso de prueba: verificar la generación de token JWT para autenticación |
| T003 | Caso de prueba: verificar que si el token está malformado o ha expirado que deniegue el acceso al sistema |
| T004 | Caso de prueba: verificar que las redirecciones están funcionando correctamente dependiendo del usuario y el rol |
| T005 | Caso de prueba: verificar que el endpoint /api/login con el método POST al poner credenciales inválidas no de acceso al sistema |

#### QA-NF (QA No Funcional)
| id | Descripción de tarea |
|----|----------------------|
| T006 | Caso de prueba: Verificar manejo de errores código HTTP y mensajes de error claros |

## HU004 - Publicar Propiedad
### Perspectiva Dev
#### DEV-F (Desarrollo Funcional)
| id | Descripción de tarea |
|----|----------------------|
| T001 | Crear tabla propiedades en BD con campos: id, titulo, direccion, descripcion, precio_alquiler, imagenes, fecha_publicacion, arrendador_id, fecha_actualizacion |
| T002 | Crear modelo/entidad Propiedad y DTOs |
| T003 | Implementar endpoint POST /api/properties para publicar una propiedad (solo accesible por arrendadores) |

#### DEV-NF (Desarrollo No Funcional)
| id | Descripción de tarea |
|----|----------------------|
| T004 | Implementar validaciones de entrada(formato de datos, campos requeridos) |
| T005 | Implementar manejo de errores código HTTP y mensajes de error claros |

### Perspectiva QA
#### QA-F (QA Funcional)
| id | Descripción de tarea |
|----|----------------------|
| T001 | Caso de prueba: Verificar que el endpoint POST /api/properties sea sólo accesible por arrendatarios |
| T002 | Caso de prueba: Verificar que el endpoint POST /api/properties cree la propiedad con sus datos |
| T003 | E2E: Inicio de sesión -> Creación de publicación |

#### QA-NF (QA No Funcional)
| id | Descripción de tarea |
|----|----------------------|
| T004 | Caso de prueba: Verificar que el endpoint POST /api/properties devuelva un código y mensaje de error y si no cumple con las restricciones de los datos |

## HU005 - Visualizar Propiedades Disponibles
### Perspectiva Dev
#### DEV-F (Desarrollo Funcional)
| id | Descripción de tarea |
|----|----------------------|
| T001 | Implementar endpoint GET /api/properties para listar propiedades disponibles |
| T002 | Componente frontend para mostrar lista de propiedades con detalles (titulo, direccion, descripcion, precio_alquiler, imagenes) |

#### DEV-NF (Desarrollo No Funcional)
| id | Descripción de tarea |
|----|----------------------|
| T003 | Implementar manejo de errores código HTTP y mensajes de error claros |
| T004 | Implementar paginación para la lista de propiedades |

### Perspectiva QA
#### QA-F (QA Funcional)
| id | Descripción de tarea |
|----|----------------------|
| T001 | Descripicón de tarea |

#### QA-NF (QA No Funcional)
| id | Descripción de tarea |
|----|----------------------|
| T002 | Descripicón de tarea |

## HU006 - Aplicar para alquilar propiedad
### Perspectiva Dev
#### DEV-F (Desarrollo Funcional)
| id | Descripción de tarea |
|----|----------------------|
| T001 | Crear tabla aplicaciones en BD con campos: id, propiedad_id, arrendatario_id, fecha_aplicacion, estado (pendiente, aceptada, rechazada) |
| T002 | Crear modelo/entidad Aplicacion y DTOs |
| T003 | Implementar endpoint POST /api/apply para que arrendatarios apliquen a una propiedad |

#### DEV-NF (Desarrollo No Funcional)
| id | Descripción de tarea |
|----|----------------------|
| T004 | Implementar validaciones (propiedad existe, arrendatario existe) |
| T005 | Implementar manejo de errores código HTTP y mensajes de error claros |
| T006 | Implementar lógica para evitar múltiples aplicaciones a la misma propiedad por el mismo arrendatario |

### Perspectiva QA
#### QA-F (QA Funcional)
| id | Descripción de tarea |
|----|----------------------|
| T001 | Descripicón de tarea |

#### QA-NF (QA No Funcional)
| id | Descripción de tarea |
|----|----------------------|
| T002 | Descripicón de tarea |

### HU007 - Evaluar perffil financiero del arrendatario
### Perspectiva Dev
#### DEV-F (Desarrollo Funcional)
| id | Descripción de tarea |
|----|----------------------|
| T001 | Implementar servicio de evaluación financiera con las reglas de negocio (bajo, medio, alto) |
| T002 | Integrar evaluación automática al recibir solicitud de alquiler |
| T003 | Almacenar resultado de la evaluación en la solicitud |

#### DEV-NF (Desarrollo No Funcional)
| id | Descripción de tarea |
|----|----------------------|
| T004 | Implementar manejo de errores código HTTP y mensajes de error claros |

### Perspectiva QA
#### QA-F (QA Funcional)
| id | Descripción de tarea |
|----|----------------------|
| T001 | Descripicón de tarea |

#### QA-NF (QA No Funcional)
| id | Descripción de tarea |
|----|----------------------|
| T002 | Descripicón de tarea |
