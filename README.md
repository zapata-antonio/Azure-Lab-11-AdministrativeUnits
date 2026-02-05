# Azure-Lab-11-AdministrativeUnits
## Objetivo
Delegar soporte local sin dar visibilidad ni control global del tenant.

## Contexto
En organizaciones grandes es común delegar soporte por sedes o regiones. El problema es que si a un técnico se le asigna un rol global (por ejemplo, Administrador de usuarios), puede administrar usuarios de toda la compañía. Con Unidades Administrativas (Administrative Units) se puede limitar el alcance del rol a un conjunto concreto de usuarios, aplicando el principio de mínimo privilegio.

## Configuración usada en el laboratorio
- Unidad Administrativa: UA_Malaga
- Usuarios dentro de la UA: usuario_6, usuario_7
- Admin local delegado: usuario_8
- Usuario fuera de la UA (para prueba): usuario_9
- Rol delegado: Administrador de usuarios (scope limitado a UA_Malaga)

## Tareas realizadas
1. Creación de la Unidad Administrativa (UA_Malaga).
2. Alta de miembros dentro de la UA (usuario_6 y usuario_7).
3. Delegación del rol Administrador de usuarios al admin local (usuario_8) con alcance limitado a UA_Malaga.
4. Verificación:
   - El admin local puede gestionar usuarios dentro de su UA.
   - El admin local no puede gestionar usuarios fuera de su UA.

## Evidencias
- Usuarios en UA: images/01-ua-users.png
- Rol con scope UA: images/02-ua-scope.png
- Intento fuera de la UA (denegado): images/03-denied-outside-ua.png
- Intento con usuario_9 (denegado): images/04-denied-user9.png

Nota: si alguna captura muestra contraseñas temporales, conviene ocultarlas antes de subirlas al repositorio.

## Checklist de verificación
- [x] Admin local solo gestiona usuarios dentro de su UA
- [x] No puede administrar usuarios fuera de su UA
- [x] La delegación respeta el principio de mínimo privilegio

## Qué le diría al cliente / entrevista
“Con Unidades Administrativas puedo delegar soporte por sedes o áreas sin dar permisos globales. El técnico local puede hacer tareas dentro de su ámbito, pero no tiene visibilidad ni capacidad de administración sobre el resto del tenant, reduciendo riesgos y mejorando el control.”
