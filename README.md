# CivicIA: Smart City Reporting

# CREA UNA APLICACIÓN COMPLETA LLAMADA CIVICIA

Quiero que construyas una aplicación web móvil profesional, responsive e instalable como PWA llamada:

# CivicIA

Nombre académico del proyecto:

**“Sistema inteligente para el reporte, clasificación, priorización y seguimiento de incidencias urbanas mediante inteligencia artificial”.**

La aplicación estará orientada inicialmente a ciudadanos y municipalidades del Perú.

Debe diseñarse principalmente para TELÉFONOS MÓVILES, pero también debe funcionar correctamente en tablet y escritorio.

No quiero solamente un mockup ni una página visual.

Quiero una aplicación funcional con:

- frontend;
- base de datos;
- autenticación;
- almacenamiento de fotografías;
- mapas;
- geolocalización;
- roles;
- inteligencia artificial;
- dashboard administrativo;
- historial;
- seguridad;
- diseño responsive.

---

# 1. PROBLEMA QUE DEBE RESOLVER

Actualmente los ciudadanos pueden encontrar problemas urbanos como:

- postes de alumbrado averiados;
- baches;
- pistas deterioradas;
- acumulación de basura;
- fugas de agua;
- problemas de desagüe;
- semáforos dañados;
- señalización deficiente;
- veredas deterioradas;
- parques dañados;
- obstrucciones de vía;
- infraestructura pública deteriorada;
- riesgos eléctricos.

Muchas veces el ciudadano no sabe:

- dónde reportarlo;
- qué área municipal es responsable;
- qué ocurrió con su denuncia;
- cuánto demorará;
- si alguien ya reportó el mismo problema.

Además, una municipalidad puede recibir numerosos reportes sin disponer de un mecanismo adecuado para clasificarlos y priorizarlos.

CivicIA debe solucionar ambos problemas.

---

# 2. IDEA PRINCIPAL

El ciudadano podrá:

1. abrir la aplicación;
2. tomar o seleccionar una fotografía;
3. permitir detectar su ubicación;
4. escribir una descripción;
5. enviar la incidencia.

Posteriormente una IA analizará el reporte.

La IA deberá sugerir:

- categoría;
- nivel de gravedad;
- riesgo para personas;
- impacto en movilidad;
- elementos detectados;
- resumen;
- posible prioridad.

Después, un algoritmo basado en reglas calculará la prioridad final.

El ciudadano podrá seguir el estado del reporte.

Ejemplo:

REPORTADO

↓

VALIDANDO

↓

APROBADO

↓

ASIGNADO

↓

EN PROCESO

↓

RESUELTO

↓

CERRADO

---

# 3. TECNOLOGÍAS

Utiliza el stack recomendado y compatible con Lovable.

Frontend:

- React;
- TypeScript;
- arquitectura por componentes;
- diseño mobile-first;
- sistema de componentes consistente.

Backend:

## Supabase

Utilizar:

- PostgreSQL;
- Supabase Authentication;
- Supabase Storage;
- Supabase Realtime;
- Row Level Security;
- Edge Functions.

No construir datos importantes solamente como mocks.

Los datos reales deben persistirse en Supabase.

---

# 4. PWA

Quiero que CivicIA pueda instalarse desde el navegador en la pantalla de inicio del teléfono.

Configura el proyecto como Progressive Web App cuando sea posible.

Debe tener:

- nombre de aplicación;
- icono;
- manifest;
- comportamiento responsive;
- pantalla completa al instalarse;
- experiencia mobile-first.

La aplicación debe sentirse como una app móvil, no como una página web tradicional.

---

# 5. TIPOS DE USUARIO

Existirán inicialmente dos roles:

## CIUDADANO

Puede:

- registrarse;
- iniciar sesión;
- recuperar contraseña;
- completar perfil;
- crear reportes;
- tomar fotografía;
- seleccionar fotografía;
- obtener ubicación;
- seleccionar punto manualmente;
- escribir descripción;
- ver análisis de IA;
- confirmar reporte;
- consultar sus incidencias;
- consultar incidencias públicas cercanas;
- apoyar una incidencia existente;
- ver estado;
- ver historial;
- recibir notificaciones internas;
- indicar si considera solucionado el problema.

## ADMINISTRADOR MUNICIPAL

Puede:

- iniciar sesión;
- acceder al panel administrativo;
- consultar incidencias;
- ver incidencias en mapa;
- filtrar reportes;
- modificar categoría;
- revisar el análisis realizado por IA;
- cambiar prioridad;
- cambiar estado;
- asignar responsable;
- escribir observaciones;
- cerrar incidencias;
- consultar estadísticas.

IMPORTANTE:

No implementar seguridad solamente ocultando botones.

Aplicar permisos mediante:

- roles;
- consultas autorizadas;
- Row Level Security.

---

# 6. DISEÑO DE LA APLICACIÓN

Quiero una interfaz:

- moderna;
- profesional;
- minimalista;
- institucional;
- accesible;
- limpia;
- intuitiva;
- mobile-first.

No utilizar un diseño infantil.

Utilizar:

- tarjetas;
- sombras suaves;
- bordes redondeados moderados;
- buena jerarquía visual;
- iconos modernos;
- espacios consistentes;
- tipografía clara.

Crear una identidad visual relacionada con:

- ciudadanía;
- tecnología;
- ciudad;
- transparencia;
- inteligencia artificial.

---

# 7. NAVEGACIÓN MÓVIL

Para ciudadano utilizar una barra inferior.

Debe contener aproximadamente:

Inicio

Mapa

Reportar

Mis reportes

Perfil

El botón:

REPORTAR

debe ser visualmente destacado.

---

# 8. PANTALLA DE INICIO

Crear un dashboard ciudadano.

Parte superior:

“Hola, [nombre]”

debajo:

“¿Encontraste un problema en tu ciudad?”

Botón principal grande:

+ REPORTAR INCIDENCIA

Mostrar tarjetas:

Reportes activos

En proceso

Resueltos

Mostrar sección:

“Incidencias cerca de ti”

y acceso:

“Ver mapa”

Mostrar también últimos reportes realizados por el usuario.

---

# 9. CREAR INCIDENCIA

No mostrar un formulario gigante.

Crear un flujo moderno dividido en pasos.

## PASO 1 — EVIDENCIA

Título:

“¿Qué está ocurriendo?”

Permitir:

Tomar fotografía

o

Elegir de galería

Mostrar preview.

Permitir eliminar/cambiar imagen.

---

## PASO 2 — UBICACIÓN

Solicitar geolocalización mediante las funciones disponibles en navegador.

Mostrar mapa.

Mostrar marcador.

Permitir mover manualmente el marcador.

Mostrar:

Latitud

Longitud

y dirección aproximada cuando esté disponible.

Si el usuario rechaza GPS:

permitir seleccionar ubicación manualmente.

---

## PASO 3 — DESCRIPCIÓN

Campo:

“Describe brevemente el problema”

Placeholder:

“Ejemplo: existe un bache profundo que ocupa parte de la vía y dificulta el tránsito.”

Permitir seleccionar categoría manualmente si se desea.

---

## PASO 4 — ANÁLISIS CON IA

Mostrar animación:

“CivicIA está analizando tu reporte…”

Después mostrar:

Categoría detectada

Gravedad

Riesgo

Impacto

Prioridad sugerida

Resumen

Ejemplo:

Categoría:
Bache / pista dañada

Gravedad:
Alta

Riesgo para personas:
Medio

Impacto vial:
Alto

Prioridad sugerida:
ALTA

Mostrar claramente:

“Esta clasificación es una recomendación generada automáticamente y será revisada cuando corresponda.”

---

## PASO 5 — CONFIRMAR

Mostrar:

Fotografía

Ubicación

Descripción

Categoría

Prioridad

Botón:

ENVIAR REPORTE

Después mostrar:

“¡Reporte enviado correctamente!”

y generar un código similar a:

CIV-2026-000124

---

# 10. CATEGORÍAS

Crear categorías en base de datos.

Inicialmente:

- Alumbrado público
- Baches o pistas dañadas
- Veredas dañadas
- Acumulación de basura
- Agua y desagüe
- Semáforos
- Señalización vial
- Parques y áreas verdes
- Infraestructura pública
- Obstrucción de vía
- Riesgo eléctrico
- Otro

No distribuir categorías como strings repetidos por toda la aplicación.

---

# 11. ESTADOS

Utilizar:

REPORTADO

VALIDANDO

APROBADO

ASIGNADO

EN_PROCESO

RESUELTO

RECHAZADO

CERRADO

Mostrar los nombres al usuario de forma amigable:

Reportado

Validando

Aprobado

Asignado

En proceso

Resuelto

Rechazado

Cerrado

---

# 12. HISTORIAL

Cada reporte debe tener timeline.

Ejemplo:

10:32 a. m.
Reporte enviado

10:33 a. m.
Análisis automático realizado

11:05 a. m.
Reporte validado

12:20 p. m.
Asignado a mantenimiento

3:45 p. m.
Trabajo iniciado

5:30 p. m.
Problema solucionado

Nunca reemplazar eventos antiguos.

Crear historial auditable.

---

# 13. PRIORIDADES

Crear cuatro niveles:

BAJA

MEDIA

ALTA

CRÍTICA

Visualmente pueden diferenciarse mediante colores.

Pero NO depender exclusivamente del color.

Mostrar también:

icono;

texto;

etiqueta.

---

# 14. ALGORITMO DE PRIORIZACIÓN

La IA NO decidirá por sí sola la prioridad final.

Crear sistema mediante puntaje de 0 a 100.

Variables:

gravedad: máximo 30

riesgo para personas: máximo 25

impacto en movilidad: máximo 15

cantidad aproximada de afectados: máximo 10

proximidad a zona sensible: máximo 10

antigüedad del reporte: máximo 10

TOTAL = 100

Clasificación inicial:

0-24
BAJA

25-49
MEDIA

50-74
ALTA

75-100
CRÍTICA

Crear la función de scoring separada y reutilizable.

No colocar números mágicos repetidos por diferentes componentes.

---

# 15. INTELIGENCIA ARTIFICIAL

Integrar un proveedor de IA desde backend.

Preferentemente Gemini.

NO colocar claves privadas en el frontend.

Crear una Supabase Edge Function:

analyze-incident

La función recibirá:

description

imageUrl

latitude

longitude

La IA deberá devolver JSON estructurado similar a:

{
  "suggestedCategory": "Baches o pistas dañadas",
  "confidence": 0.94,
  "severity": 25,
  "riskToPeople": 18,
  "mobilityImpact": 13,
  "affectedPeopleLevel": "MEDIUM",
  "detectedElements": [
    "bache",
    "vía",
    "vehículos"
  ],
  "summary": "Bache de considerable tamaño ubicado en una vía vehicular.",
  "requiresHumanReview": false
}

Validar siempre esta respuesta antes de guardarla.

Si la IA falla:

NO impedir que el ciudadano reporte.

Permitir continuar manualmente.

---

# 16. BASE DE DATOS

Diseña un esquema PostgreSQL profesional.

Crear aproximadamente:

profiles

municipalities

municipal_departments

incident_categories

incidents

incident_images

incident_ai_analysis

incident_status_history

incident_assignments

incident_comments

incident_supports

notifications

app_settings

ai_analysis_logs

Si encuentras una estructura mejor, aplícala.

---

# 17. INCIDENTS

La entidad principal debe considerar:

id

public_code

citizen_id

municipality_id

category_id

title

description

latitude

longitude

address

priority_score

priority_level

status

is_public

ai_analyzed

created_at

updated_at

resolved_at

closed_at

Diseña correctamente:

primary keys;

foreign keys;

constraints;

índices.

---

# 18. FOTOGRAFÍAS

Utilizar Supabase Storage.

Crear bucket apropiado para evidencias.

Las imágenes deben relacionarse con:

incident_id

uploader_id

created_at

No guardar imágenes convertidas en Base64 dentro de PostgreSQL.

Mostrar preview antes de enviar.

Comprimir/redimensionar imágenes cuando sea conveniente.

---

# 19. MAPA

Crear pantalla:

“Mapa de incidencias”

Utilizar una solución de mapas compatible con Lovable.

Preferentemente Google Maps si la integración disponible resulta adecuada.

Mostrar marcadores.

Cada marcador deberá representar una incidencia.

Al seleccionarlo mostrar:

categoría;

prioridad;

estado;

fecha;

foto miniatura;

botón:

“Ver reporte”

Filtros:

Categoría

Prioridad

Estado

Distancia

---

# 20. GEOLOCALIZACIÓN

Utilizar las capacidades de geolocalización del navegador.

Solicitar autorización.

Nunca asumir que el usuario aceptará.

Si rechaza:

permitir seleccionar manualmente la ubicación.

No bloquear toda la aplicación por no tener permisos de GPS.

---

# 21. DETECCIÓN DE DUPLICADOS

Cuando el ciudadano crea un reporte:

buscar incidencias abiertas aproximadamente dentro de:

50 metros.

Considerar:

ubicación;

categoría;

fecha;

estado.

Si existen coincidencias mostrar:

“Encontramos un reporte parecido cerca de esta ubicación.”

Mostrar posibles incidencias.

Botones:

APOYAR REPORTE EXISTENTE

CREAR NUEVO REPORTE

Si selecciona apoyar:

registrar el apoyo en:

incident_supports.

---

# 22. MAPA DE CALOR

En el dashboard administrativo agregar posteriormente un mapa de calor.

Debe permitir visualizar lugares con alta concentración de:

basura;

baches;

alumbrado;

otros problemas.

Preparar la arquitectura aunque inicialmente pueda mostrarse mediante marcadores agrupados.

---

# 23. ADMINISTRADOR MUNICIPAL

Crear interfaz administrativa responsive.

En escritorio utilizar sidebar.

Secciones:

Dashboard

Incidencias

Mapa

Asignaciones

Estadísticas

Configuración

---

# 24. DASHBOARD ADMINISTRATIVO

Mostrar KPIs:

Total reportados

Pendientes

En proceso

Resueltos

Incidencias críticas

Tiempo promedio de resolución

Mostrar gráficos:

Reportes por categoría

Reportes por estado

Reportes por prioridad

Evolución por fechas

Mostrar:

Incidencias urgentes

Últimos reportes

Mapa

---

# 25. GESTIÓN DE UNA INCIDENCIA

Pantalla administrativa con:

Fotografía grande

Código

Ciudadano anonimizado

Fecha

Ubicación

Mapa

Descripción

Categoría

Estado

Prioridad

Puntaje

Análisis IA

Permitir:

Cambiar categoría

Cambiar prioridad

Cambiar estado

Asignar departamento

Asignar responsable

Agregar comentario

Marcar como resuelto

Cerrar caso

---

# 26. REVISIÓN HUMANA

Toda recomendación de IA debe poder ser modificada por un administrador autorizado.

Guardar:

resultado original IA;

resultado definitivo;

quién realizó modificación;

fecha.

Esto permitirá posteriormente estudiar:

precisión de la IA.

---

# 27. NOTIFICACIONES

Crear centro de notificaciones interno.

Ejemplos:

“Tu reporte CIV-2026-000124 fue recibido.”

“Tu reporte fue validado.”

“Personal municipal está atendiendo tu incidencia.”

“Tu incidencia fue marcada como resuelta.”

Permitir:

marcar como leído.

Preparar arquitectura para notificaciones push futuras.

---

# 28. REPORTES PÚBLICOS

Permitir visualizar incidencias públicas.

NO mostrar:

correo del ciudadano;

número telefónico;

identificador interno;

información privada.

Mostrar solamente:

categoría;

foto permitida;

ubicación aproximada cuando corresponda;

estado;

fecha;

cantidad de apoyos.

---

# 29. PRIVACIDAD

Antes de cargar una fotografía mostrar:

“Evita fotografiar rostros, documentos, matrículas u otros datos personales cuando no sean necesarios para reportar la incidencia.”

Preparar el sistema para incorporar posteriormente:

detección de rostros;

difuminado automático;

detección de matrículas.

No es obligatorio para el MVP.

---

# 30. EMERGENCIAS

CivicIA NO debe presentarse como aplicación de emergencias.

Si el análisis identifica posible:

incendio;

accidente grave;

persona herida;

violencia;

riesgo inmediato para la vida;

mostrar:

“Esta situación podría requerir atención inmediata. Utiliza los canales oficiales de emergencia correspondientes.”

Los números/contactos deben provenir de configuración.

No inventar números dentro del código.

---

# 31. PERFIL

Mostrar:

foto/avatar;

nombre;

distrito;

fecha de registro;

cantidad de reportes;

reportes solucionados.

Opciones:

Editar perfil

Notificaciones

Privacidad

Acerca de CivicIA

Cerrar sesión

---

# 32. MIS REPORTES

Crear tabs/filtros:

Todos

Activos

En proceso

Resueltos

Cada tarjeta muestra:

fotografía;

categoría;

código;

fecha;

estado;

prioridad.

---

# 33. DETALLE DEL REPORTE

Mostrar:

Código

Fotografía

Mapa

Dirección

Descripción

Categoría

Prioridad

Estado actual

Timeline

Comentarios oficiales

Cantidad de apoyos

---

# 34. REALTIME

Cuando un administrador cambie el estado:

el ciudadano debe poder ver la actualización sin necesidad de recargar manualmente cuando sea viable.

Utilizar Supabase Realtime.

---

# 35. AUTENTICACIÓN

Crear:

Login

Registro

Recuperar contraseña

Cerrar sesión

Sesión persistente

Protección de rutas

Separación de roles.

En registro ciudadano solicitar solamente información necesaria.

---

# 36. SEGURIDAD

Configurar Row Level Security.

Ciudadano:

puede crear sus propios reportes;

consultar sus reportes;

consultar incidencias públicas;

apoyar incidencias;

NO puede cambiar prioridad;

NO puede marcar arbitrariamente reportes como resueltos;

NO puede acceder a panel administrativo.

Administrador:

solo puede administrar información correspondiente a su municipalidad.

No utilizar service role key en frontend.

No exponer API keys privadas.

---

# 37. DISEÑO RESPONSIVE

Móvil:

bottom navigation.

Desktop administrativo:

sidebar.

Tablet:

adaptación automática.

Probar como mínimo:

375 px

390 px

430 px

768 px

1440 px

Evitar horizontal overflow.

---

# 38. ACCESIBILIDAD

Implementar:

labels;

contraste apropiado;

focus states;

navegación clara;

botones grandes;

textos legibles;

aria-label cuando corresponda.

No depender exclusivamente de color para mostrar estados.

---

# 39. ESTADOS DE INTERFAZ

Toda pantalla que consulte datos debe soportar:

loading;

success;

empty;

error.

Ejemplo:

si no existen reportes:

“No tienes reportes todavía.”

Botón:

“Reportar una incidencia”

---

# 40. MODO DEMOSTRACIÓN

Este proyecto será presentado en una exposición universitaria.

Crear un modo demo.

Debe existir una configuración equivalente a:

VITE_DEMO_MODE=true

Cuando esté activo:

usar ejemplos preconfigurados cuando algún servicio externo no esté disponible.

Debe ser posible demostrar:

clasificación IA;

mapa;

dashboard;

historial;

cambios de estado.

No mezclar datos demo con producción.

---

# 41. DATOS DE DEMOSTRACIÓN

Crear datos ficticios:

Bache profundo en avenida

Poste de alumbrado apagado

Acumulación de basura

Semáforo averiado

Fuga de agua

Vereda deteriorada

Distribuirlos entre:

BAJA

MEDIA

ALTA

CRÍTICA

y diferentes estados.

Utilizar coordenadas ficticias o apropiadas para demostración.

No presentar datos demo como incidencias reales.

---

# 42. ANALÍTICAS

Preparar estadísticas para:

reportes por categoría;

reportes por prioridad;

reportes por estado;

incidencias por zona;

incidencias por fecha;

tiempo promedio de solución;

porcentaje resuelto;

categoría más frecuente;

reportes duplicados;

apoyos ciudadanos.

---

# 43. INDICADORES DE INVESTIGACIÓN

La aplicación será utilizada también como proyecto universitario.

Por eso quiero poder medir posteriormente:

Precisión de clasificación de IA.

Porcentaje de categorías de IA corregidas por administradores.

Precisión de prioridad sugerida.

Tiempo promedio de clasificación manual vs IA.

Tiempo promedio de atención.

Tiempo promedio de resolución.

Cantidad de reportes duplicados evitados.

Nivel de satisfacción del ciudadano.

Porcentaje de incidencias solucionadas.

Diseña el modelo de datos pensando también en obtener estas métricas.

---

# 44. COMPONENTES REUTILIZABLES

Crear componentes similares a:

IncidentCard

StatusBadge

PriorityBadge

PhotoUploader

LocationPicker

MapView

IncidentTimeline

AIAnalysisCard

StatCard

EmptyState

LoadingState

ErrorState

ConfirmDialog

BottomNavigation

AdminSidebar

No repetir grandes cantidades de código.

---

# 45. EXPERIENCIA VISUAL

La pantalla inicial debería sentirse aproximadamente así:

--------------------------------

CivicIA

Hola, Bruno 👋

¿Encontraste un problema
en tu ciudad?

[ + REPORTAR INCIDENCIA ]

Tus reportes

3 Activos
2 En proceso
8 Resueltos

Incidencias cerca de ti

[ MAPA ]

Inicio | Mapa | + | Reportes | Perfil

--------------------------------

No copies literalmente este diseño si puedes producir uno mejor.

---

# 46. FLUJO DEL SISTEMA

La arquitectura conceptual debe ser:

CIUDADANO

↓

FOTOGRAFÍA + DESCRIPCIÓN + GPS

↓

SUPABASE

↓

EDGE FUNCTION

↓

INTELIGENCIA ARTIFICIAL

↓

CLASIFICACIÓN

↓

ALGORITMO DE PRIORIDAD

↓

INCIDENCIA

↓

PANEL MUNICIPAL

↓

ASIGNACIÓN

↓

ATENCIÓN

↓

RESOLUCIÓN

↓

NOTIFICACIÓN AL CIUDADANO

---

# 47. ALCANCE MVP

Construir primero:

1. Landing/login.
2. Registro.
3. Roles.
4. Dashboard ciudadano.
5. Crear reporte.
6. Subir fotografía.
7. Geolocalización.
8. Seleccionar ubicación.
9. Guardar incidencia.
10. Análisis IA.
11. Cálculo de prioridad.
12. Mis reportes.
13. Detalle.
14. Mapa.
15. Historial.
16. Panel administrativo.
17. Cambio de estados.
18. Estadísticas básicas.
19. RLS.
20. Modo demo.
21. PWA.

---

# 48. NO IMPLEMENTAR TODAVÍA

Dejar preparados pero NO priorizar inicialmente:

visión computacional entrenada desde cero;

predicción futura de incidencias;

IoT;

rutas de vehículos municipales;

machine learning propio;

chatbot;

blockchain;

gamificación;

reconocimiento facial;

sistemas complejos innecesarios.

Quiero primero un MVP excelente y funcional.

---

# 49. MUY IMPORTANTE: FORMA DE CONSTRUIR

No intentes crear una aplicación gigantesca e inestable en una sola pasada.

Trabaja progresivamente.

Sin embargo, crea desde la primera generación una estructura visual suficientemente completa para que pueda navegar por el producto y evaluar el diseño.

Primero prioriza:

1. arquitectura;
2. diseño;
3. navegación;
4. base de datos;
5. autenticación;
6. ciudadano;
7. creación de reporte;
8. administrador;
9. IA;
10. seguridad.

Antes de modificar funcionalidades que ya funcionan:

revisa su implementación.

No destruyas funcionalidades existentes innecesariamente.

---

# 50. NO HACER

NO crear solamente una landing page.

NO crear únicamente pantallas estáticas.

NO llenar toda la aplicación de datos hardcodeados.

NO exponer claves API.

NO permitir acceso administrativo por simple manipulación del navegador.

NO permitir que la IA ejecute acciones administrativas.

NO utilizar IA como única fuente para determinar prioridad.

NO utilizar `any` innecesariamente en TypeScript.

NO duplicar lógica.

NO generar interfaces visualmente inconsistentes.

NO sustituir funcionalidad importante por comentarios TODO sin razón.

---

# 51. PRIMER RESULTADO QUE QUIERO DE LOVABLE

Comienza creando la primera versión funcional y visual de CivicIA.

Necesito que inicialmente puedas mostrar:

## Ciudadano

- Login
- Registro
- Inicio
- Crear reporte
- Cargar/tomar fotografía
- Ubicación
- Descripción
- Resultado de análisis IA simulado inicialmente si todavía no conectamos Gemini
- Confirmación
- Mis reportes
- Detalle
- Mapa
- Perfil

## Administrador

- Dashboard
- Lista de incidencias
- Detalle
- Mapa
- Estadísticas

Usa datos demo inicialmente cuando todavía no exista información real.

Después conecta progresivamente Supabase.

---

# 52. BASE DE DATOS

Cuando llegue el momento de conectar Supabase:

muéstrame claramente qué tablas vas a crear.

Configura:

foreign keys;

constraints;

indexes;

RLS;

storage;

auth.

No cambies estructuras existentes de forma destructiva sin explicarlo.

---

# 53. INTELIGENCIA ARTIFICIAL

Después de que el flujo principal funcione:

implementa Gemini a través de una función backend.

Nunca directamente desde el navegador.

La IA debe analizar descripción y, cuando sea técnicamente viable, imagen.

La aplicación debe seguir funcionando aunque la IA temporalmente no esté disponible.

---

# 54. OBJETIVO FINAL

El producto final debe permitir demostrar en una exposición:

1. un ciudadano encuentra un problema;
2. abre CivicIA;
3. toma una fotografía;
4. obtiene ubicación;
5. escribe descripción;
6. IA analiza la incidencia;
7. sistema calcula prioridad;
8. ciudadano envía reporte;
9. reporte aparece en panel municipal;
10. administrador lo revisa;
11. administrador lo asigna;
12. cambia a “En proceso”;
13. ciudadano visualiza actualización;
14. administrador lo marca como resuelto;
15. ciudadano visualiza resolución;
16. dashboard actualiza estadísticas.

Quiero que toda la experiencia parezca un producto real y no simplemente una tarea universitaria.

Empieza ahora creando la estructura inicial de CivicIA, priorizando diseño mobile-first, navegación completa y una experiencia visual profesional. Luego iremos conectando progresivamente base de datos, autenticación e inteligencia artificial.

This project was built with [Lovable](https://lovable.dev).

**Live app**: https://town-aid-ai.lovable.app

## Build with Lovable

Continue developing this project in the [Lovable editor](https://lovable.dev/projects/5cb81581-ee6b-45ed-bc70-eefe2136a6a6).

- **Ship faster**: describe what you want to build and Lovable handles the code.
- **Stay in sync**: every change made in Lovable is committed straight to this repository.
- **Full ownership**: this code is yours. Push to `main` on GitHub and your changes sync back into Lovable, ready for your next prompt.

## Development

Prefer working locally? You need Node.js and npm — [install with nvm](https://github.com/nvm-sh/nvm#installing-and-updating).

```sh
git clone <this-repository-url>
cd <repository-name>
npm i
npm run dev
```
