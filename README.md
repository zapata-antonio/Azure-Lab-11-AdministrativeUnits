# Azure-Lab-11-AdministrativeUnits
## Objetivo
Delegar soporte local (por sede o región) sin dar visibilidad ni control global sobre el tenant.

## Contexto
En empresas grandes suele haber equipos por zonas. Si a un técnico le das un rol global (por ejemplo, Administrador de usuarios), puede tocar usuarios de toda la compañía. Con Unidades Administrativas (Administrative Units) se puede delegar el soporte por región limitando el alcance del rol, aplicando el principio de mínimo privilegio.

## Qué se ha hecho en este laboratorio
1. Se ha creado una Unidad Administrativa llamada UA_Malaga.
2. Se han añadido usuarios a esa unidad.
3. Se ha asignado un rol a un administrador local con alcance limitado a la UA (scope por unidad).
4. Se ha verificado que el administrador local solo puede gestionar usuarios dentro de su UA.

## Evidencias
- Usuarios en UA: images/01-ua-users.png
- Rol con scope UA: images/02-ua-scope.png

## Checklist de verificación
- [X] El admin local solo gestiona usuarios dentro de su UA
- [X] No puede administrar usuarios fuera de la UA

## Qué le diría al cliente / entrevista
“Con Unidades Administrativas puedo delegar soporte por sedes o áreas sin dar permisos globales. El técnico local puede hacer resets y cambios básicos solo dentro de su ámbito, reduciendo riesgos y manteniendo control.”
