🌎 Mundial 2026 – Modelo de Datos

👥 Integrantes
Franco Riva – francoriva72@gmail.com
Federico Rio – fedeerp01@gmail.com

📌 Temática
Sistema web informativo sobre el Mundial de Fútbol 2026.

📝 Descripción
Este proyecto consiste en el diseño de una base de datos para un sitio web dinámico (Server Side Rendering) que permite consultar y administrar información relacionada con el Mundial de Fútbol 2026.

El sistema permite:

- Visualizar las selecciones participantes
- Consultar los grupos del torneo
- Ver los partidos programados
- Registrar y visualizar resultados
- Identificar el estadio donde se juega cada partido

El ítem principal administrado por el sistema es el partido, sobre el cual el usuario administrador puede realizar operaciones de creación, modificación y eliminación.

🗂️ Modelo de Datos

Entidades principales

- Grupo
- Selección
- Partido
- Estadio
- Usuario (administrador)

Relaciones

- Un grupo contiene muchas selecciones (relación 1 a N)
- Una selección pertenece a un único grupo
- Un partido enfrenta a dos selecciones (local y visitante)
- Un partido se juega en un único estadio
- Un estadio puede albergar muchos partidos (relación 1 a N)
- Un usuario administrador puede gestionar los partidos del sistema

🔑 Claves

Cada entidad posee una clave primaria (id)

Las relaciones se implementan mediante claves foráneas:

- seleccion.id_grupo → grupo.id_grupo
- partido.id_estadio → estadio.id_estadio
- partido.id_local → seleccion.id_seleccion
- partido.id_visitante → seleccion.id_seleccion

📊 Diagrama Entidad-Relación (DER)

El diagrama entidad-relación del sistema se encuentra incluido en el repositorio en formato imagen/PDF.
