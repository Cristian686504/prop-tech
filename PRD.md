# Visión

Para propietarios en Colombia
que buscan aumentar la cantidad de clientes, la velocidad y seguridad de alquiler de sus propiedades
el PropTech
es una plataforma de arrendamiento inteligente
que permite acceder, acelerar y proteger el flujo de alquiler evaluando inquilinos
a diferencia del modelo tradicional
nuestro producto automatiza la evaluación financiera permitiendo decisiones seguras y rápidas

# Objetivos

- Aumentar la cantidad de alquileres activos en un 20% reduciendo las fricciones en el flujo de contratación y la mejora de experiencia del usuario
- Disminuir el riesgo de incumplimiento de contrato en un 10%, haciendo una validación previa a la firma donde se calcule el depósitos de garantía de forma dinámica dependiendo del resultado de un análisis del score crediticio e ingresos mensuales
- El flujo de alquiler tendrá una duración de menos de 1 día, mediante la digitalización y automatización de las etapas clave del proceso como la validación de documentos, generación del contrato, firma electrónica y confirmación final

# Alcance del MVP

## IN SCOPE
 - Registro e inicio de sesión para usuarios con rol de arrendador y arrendatario
 - El arrendador(propietario) podrá publicar propiedades y el arrendatario (inquilino) podrá visualizar las propiedades disponibles para alquilar y solicitar el alquiler de una propiedad
 - Evaluación del perfil financiero del arrendatario(score crediticio e ingresos mensuales)
 - Cálculo dinámico del depósito de garantía(1 a 3 meses) en base al score crediticio del arrendatario
 - Generación de contrato de arrendamiento en PDF con estado(aprobado, rechazado, pendiente)
 
## OUT SCOPE
 - Firma digital de contrato
 - Gestión de pagos de alquiler
 - Usuario administrador
 - Integración con bancos reales
 - Notificaciones
 - Soporte a clientes
 - Filtro de propiedades

# Riesgos de Negocio (Proyecto)

| Descripción | Impacto | Probabilidad | Riesgo | Mitigación |
|------------|:---------:|:-----------:|:-------:|-----------|
| Escasez de personal: el equipo cuenta con 2 integrantes, 1QA y 1DEV    | 3   | 3 | 9 | Solicitar la integración de más personas antes del próximo sprint |
| Estimaciones inexactas: el equipo no cuenta con experienca en este tipo de proyecto  | 3  | 3  | 9 | Estimar en base a story points |
| Retrasos: los integrantes del equipo son de diferentes países y hay diferencia horaria     | 3    | 2  | 6  | Definir horarios de trabajo coincidientes y comunicación por chat |

# Riesgos Técnicos (Producto)

| Descripción | Impacto | Probabilidad | Riesgo | Mitigación |
|------------|:---------:|:-----------:|:-------:|-----------|
| El responsive puede romper la UI    | 2   | 2 | 4 | Probar la UI en distintas resoluciones |
| Dos usuarios arrendatarios alquilan la misma propiedad al mismo tiempo generando 2 contratos   | 3  | 3  | 9 | Agregar controles de acceso simultaneo en la base de datos  |
| Se podrían acceder a los contratos por URL sin verificar sesión    | 3    | 1  | 3  | Agregar restricción a la URL de los contratos  |