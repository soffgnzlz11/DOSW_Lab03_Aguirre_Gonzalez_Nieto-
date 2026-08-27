# 📄 Requerimientos del Sistema

## 1. Lista general de requerimientos

El sistema de **TechCup** tiene los siguientes requerimientos (descripción a alto nivel):



### 1.1 Requerimientos funcionales

El sistema de TechCup debe tener la capacidad de:

1. Autenticar usuarios mediante usuario y contraseña.
2. Crear y administrar torneos.
3. Crear y actualizar equipos.
4. Registrar equipos en el torneo activo y realizar el pago de inscripción mediante PSE.
5. Consultar pagos, aprobar registros y generar reportes de equipos e ingresos.

### 1.2 Requerimientos no funcionales

El sistema de TechCup debe tener:

1. Seguridad en la autenticación de los usuarios.
2. Una interfaz sencilla y fácil de utilizar.
3. Validación de las reglas de negocio durante el registro de equipos.
4. Protección de la información de equipos y pagos.
5. Disponibilidad y rapidez en las consultas realizadas por los usuarios.

---

## 2. Diagramas de caso de uso


### 2.1 Requerimiento Funcional 3

| Campo                        | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| ---------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **ID**                       | RF-03                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **Nombre del requerimiento** | Registrar equipo y pagar inscripción (PSE)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| **Descripción**              | El sistema debe permitir al capitán crear o seleccionar un equipo, registrarlo en el torneo activo y realizar el pago de la inscripción mediante PSE.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **Precondiciones**           | Para que el sistema cumpla con este requerimiento, el capitán debe estar autenticado, debe existir un torneo en estado **Active** y el equipo debe cumplir las condiciones establecidas para la inscripción.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **Actor**                    | Capitán                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| **Flujo principal**          | 1. El actor ingresa al módulo de equipos.<br>2. El actor crea un equipo o selecciona un equipo previamente registrado.<br>3. El sistema verifica que exista un torneo activo.<br>4. El sistema muestra la información del torneo y el valor de la inscripción.<br>5. El actor solicita registrar el equipo en el torneo.<br>6. El sistema verifica que el equipo pueda registrarse en el torneo activo.<br>7. El sistema solicita realizar el pago de la inscripción.<br>8. El actor selecciona PSE y realiza el pago.<br>9. El sistema procesa y registra la información del pago.<br>10. El sistema registra la solicitud de inscripción del equipo.<br>11. El organizador puede revisar y validar el pago para aprobar la inscripción. |
| **Diagrama de caso de uso**  | *https://www.figma.com/design/sPneiN277qPumPLp93VDQk/Registrar-equipo-y-pagar-inscripción--PSE-?node-id=1-4253&p=f&t=MoctisQ6T4821Ldh-0*                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Poscondiciones**           | El pago queda registrado y el equipo queda asociado al torneo activo. La inscripción podrá ser aprobada por el organizador después de verificar el pago.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |

## 3. Preguntas

### Preguntas relacionadas con el requerimiento RF-03

1. ¿El capitán debe crear el equipo antes de iniciar el proceso de inscripción al torneo?
2. ¿Qué información debe ingresar el capitán para crear un equipo?
3. ¿Un equipo puede registrarse en más de un torneo?
4. ¿El sistema debe impedir que un equipo se registre cuando no existe un torneo en estado **Active**?
5. ¿Qué información debe mostrar el sistema antes de realizar el pago?
6. ¿El pago mediante PSE debe ser obligatorio para completar la inscripción?
