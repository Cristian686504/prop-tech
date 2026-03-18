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
| T003 | Descripicón de tarea |

#### QA-NF (QA No Funcional)
| id | Descripción de tarea |
|----|----------------------|
| T004 | Descripicón de tarea |

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
| T003 | Descripicón de tarea |

#### QA-NF (QA No Funcional)
| id | Descripción de tarea |
|----|----------------------|
| T004 | Descripicón de tarea |

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
| T001 | Descripicón de tarea |

#### QA-NF (QA No Funcional)
| id | Descripción de tarea |
|----|----------------------|
| T002 | Descripicón de tarea |

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
| T001 | Descripicón de tarea |

#### QA-NF (QA No Funcional)
| id | Descripción de tarea |
|----|----------------------|
| T002 | Descripicón de tarea |

## HU005 - Visualizar Propiedades Disponibles
### Perspectiva Dev
#### DEV-F (Desarrollo Funcional)
| id | Descripción de tarea |
|----|----------------------|
| T001 | Implementar endpoint GET /api/properties para listar propiedades disponibles |
| T002 | Componente frontend para mostrar lista de propiedades con detalles (titulo, direccion, descripcion, precio_alquiler, imagenes) |