<!-- Portada del perfil de GitHub: repo Riay/Riay -->

<p align="center">
  <img src="./assets/banner.svg" alt="Yair Silva Mendoza — Gerente de Desarrollo · Full-Stack" width="100%"/>
</p>

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=500&size=18&duration=2800&pause=900&color=FF6B2C&center=true&vCenter=true&width=860&lines=Lidero+el+desarrollo+de+una+plataforma+multi-marca+en+producci%C3%B3n;Django+%C2%B7+SQL+Server+%C2%B7+Vue+%C2%B7+React+%C2%B7+.NET+%C2%B7+Windows+Server;Integraciones%2C+datos+consolidados+y+despliegue+automatizado;De+la+arquitectura+al+code+review+y+la+operaci%C3%B3n" alt="Resumen animado"/>
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/TU-USUARIO-LINKEDIN"><img src="https://img.shields.io/badge/LinkedIn-Yair_Silva_Mendoza-0B0D10?style=for-the-badge&logo=linkedin&logoColor=FF6B2C&labelColor=11151A" alt="LinkedIn"/></a>
  <a href="mailto:TU-CORREO@dominio.com"><img src="https://img.shields.io/badge/Email-Contacto-0B0D10?style=for-the-badge&logo=gmail&logoColor=FF6B2C&labelColor=11151A" alt="Email"/></a>
  <img src="https://img.shields.io/badge/Ubicación-México-0B0D10?style=for-the-badge&logo=googlemaps&logoColor=FF6B2C&labelColor=11151A" alt="México"/>
  <img src="https://img.shields.io/badge/Estado-Abierto_a_oportunidades-FF6B2C?style=for-the-badge&labelColor=11151A" alt="Abierto a oportunidades"/>
</p>

---

## `$ whoami`

Gerente de Desarrollo en **Capnet Solutions**. Dirijo el desarrollo y la operación de **SeguimientoLite**, la plataforma de postventa que usan agencias de **Nissan, Hyundai, Stellantis, Mazda y Toyota** en **México y Colombia**: seguimiento de órdenes de servicio, cotizaciones, inspecciones, evidencias y comunicación con el cliente.

Mi trabajo va de punta a punta: defino arquitectura, planeo integraciones con proveedores, reviso código, priorizo backlog y me aseguro de que lo que sale a producción funcione en servidores Windows de cada agencia.

```yaml
rol:          Gerente de Desarrollo · Full-Stack
experiencia:  9+ años desarrollando software (laborando desde los 17)
dominio:      Postventa automotriz · DMS · multi-tenant · datos multi-sede
enfoque:      Arquitectura · Integraciones · DevOps on-premise · Liderazgo técnico
```

---

## Impacto

<table>
  <tr>
    <td width="50%" valign="top">

**Plataforma multi-marca en producción**<br/>
Una sola base Django desplegada por cliente, con configuración por tenant (prefijos, rutas, vistas SQL por esquema) para 5 marcas en 2 países.

  </td>
    <td width="50%" valign="top">

**Datos de 22 agencias en un solo lugar**<br/>
Base de KPIs consolidada para la red Nissan Colombia: vistas `UNION` sobre ~22 BD con esquemas distintos, productividad por asesor y envíos por sede.

  </td>
  </tr>
  <tr>
    <td valign="top">

**Despliegue y monitoreo automatizados**<br/>
`capnet_tools` (setup/update con merge de configuración, migraciones y fallback de dependencias) y **Capnet Monitor**: panel central con agentes Windows para disparar y auditar actualizaciones.

  </td>
    <td valign="top">

**Estabilidad en producción**<br/>
Logs ASGI bajados de **800k+ líneas/hora** a solo advertencias reales. Cifrado unificado en **AES-GCM** en API y generación de PDF.

  </td>
  </tr>
  <tr>
    <td valign="top">

**Integraciones con terceros**<br/>
APIs de citas de armadoras y proveedores (5 endpoints, auth Bearer): plan de 3 semanas, colección Postman con token automático y entrega al equipo.

  </td>
    <td valign="top">

**Gestión del equipo y backlog**<br/>
Clasificación de incidencias por dependencia (desarrollo, bloqueo externo, QA, cierre) y carga por persona y cliente. Además, recordatorios automáticos y escalamiento de tickets estancados desde Capnet Agenda.

  </td>
  </tr>
</table>

---

## Proyecto insignia

<p align="center">
  <img src="./assets/agenda.svg" alt="Capnet Agenda — 19k líneas de Python, 341 pruebas, 42 modelos, integrada a Slack, Zoom, Redmine, correo e iCal, con API REST v1" width="100%"/>
</p>

**Capnet Agenda** es la agenda, el control de ausencias y la coordinación diaria de todo el equipo de Capnet en México y Colombia. La diseñé y construí de punta a punta.

- **Reglas de negocio:** valida que nadie tenga dos sesiones a la misma hora (sesiones, comida, jornada por día, ausencias y festivos). En las series valida todas las fechas juntas, y un horario sin responder también se aparta.
- **Integración con Slack:** se entra con la cuenta de Slack (OAuth), hay comando `/agendar` con modal y pestaña Inicio. La tarjeta de cada sesión trae botones de asistencia y avisa 5 min antes. El estado cambia solo a "En sesión" o "Comiendo".
- **Correo e iCal:** manda invitaciones `.ics` que Outlook y Gmail muestran con botones Sí/No/Quizá, y lee las respuestas por IMAP. Las invitaciones externas reenviadas al buzón (Zoom, Teams, Meet, también recurrentes) se registran solas.
- **Recursos humanos:** solicitudes de vacaciones con aprobación de gerente, Dirección y Capital humano. Lleva el saldo conforme a la **LFT (art. 76)** y al **CST (art. 186)**, con festivos MX/CO y expedientes con versiones, vencimientos y bitácora.
- **Redmine:** muestra los tickets asignados a cada persona y permite apartar tiempo para atenderlos. Manda un recordatorio diario de peticiones sin movimiento y escala al gerente a los 2 días hábiles.
- **Portal de citas público:** el cliente entra con un código por correo y agenda con su consultor. Los prospectos van con el área comercial, y la reunión de Zoom se crea sola.
- **API REST v1:** llaves por aplicación, límite de 120 peticiones por minuto, bitácora y errores tipados (`409 horario_ocupado`), para que otros sistemas internos agenden con las mismas reglas.
- **Operación:** corre en Windows Server con Waitress, NSSM, SQL Server y TLS. Los tokens se guardan cifrados, los envíos a Slack pasan por una cola con reintentos y la interfaz se actualiza casi en tiempo real.

---

## Arquitectura que lidero

<p align="center">
  <img src="./assets/ecosistema.svg" alt="Ecosistema: fuentes DMS y APIs → CapnetBridge → SeguimientoLite y CapnetRI → PDF, WhatsApp/Email y KPIs; operación con Capnet Monitor" width="100%"/>
</p>

---

## Proyectos destacados

> Son sistemas de cliente en repositorios privados. Puedo mostrar arquitectura, decisiones y demos en entrevista.

| Proyecto | Qué resuelve | Stack | Mi rol |
|---|---|---|---|
| **SeguimientoLite** | Seguimiento de la orden de servicio: asesor, técnico, refacciones, mano de obra, cotización y health check en PDF | Django · DRF · SQL Server · jQuery · S3 | Líder técnico y arquitectura |
| **CapnetRI** | Recepción e inspección del vehículo en piso de taller, desde tablet | Vue.js · .NET | Revisión y corrección de flujo crítico |
| **CapnetBridge** | Normaliza datos del DMS (Intelisis) en vistas SQL listas para la plataforma | SQL Server · T-SQL | Diseño de vistas e integración |
| **KPIs Nissan Colombia** | Indicadores consolidados de ~22 agencias en una sola base | SQL Server | Modelo de datos y vistas |
| **Capnet Agenda** | Agenda, ausencias, vacaciones y coordinación del equipo MX/CO con Slack, Zoom, Redmine y correo | Django 5 · SQL Server · Slack SDK · iCal · Zoom API | Arquitectura y desarrollo completo |
| **Reinvención de Tableros V4 · Hyundai** | Tableros de taller heredados (VB.NET) rehechos sobre SeguimientoLite para Hyundai México | Django · SQL Server · JS | Rediseño y migración |
| **Capnet Monitor** | Panel central que ve el estado de los servidores Windows de cada cliente, lanza actualizaciones con confirmación y muestra el log en vivo | Django · React · agentes Python con token | Diseño y desarrollo |
| **Crepas Jhonn Coffee · Bot de pedidos** | Pedidos por WhatsApp con menú web personalizado, monitor de cocina en tiempo real y comprobante PDF | Django 5 · WhatsApp Cloud API · Channels · Celery · Redis · PostgreSQL | Arquitectura y desarrollo completo |
| **capnet_tools** | Instalación y actualización reproducible en Windows Server | Python · Git · Playwright | Diseño y desarrollo |
| **Citas Web** | Agenda de citas integrada con APIs de armadoras | Django · REST | Planeación e integración |

### Fuera del automotriz: comercio por WhatsApp

**Crepas Jhonn Coffee:** bot de pedidos para una cafetería.

```text
WhatsApp ─▶ bot (Cloud API) ─▶ enlace personal al menú web ─▶ carrito y personalización
        ─▶ pago en efectivo ─▶ monitor de cocina por WebSocket ─▶ "tu pedido está listo" + ticket PDF
```

- **Monitor de cocina (KDS):** los pedidos llegan con sonido y pasan por Nuevos, Preparando, Listos y Entregado. Desde ahí se activan o desactivan los ingredientes del día, y lo que se acaba aparece como "Agotado" en el menú del cliente.
- **Bot:** saluda con promociones (máximo una vez cada 12 h por cliente), informa el estado del pedido y pasa la conversación a una persona cuando hace falta.
- **Seguridad:** valida la firma HMAC `X-Hub-Signature-256` de cada mensaje y no duplica pedidos si Meta reintenta (idempotencia por `message_id`). Bloquea cada conversación con `select_for_update` y recalcula los precios en el servidor. El WebSocket solo acepta personal y valida el Origin, y hay un límite de 5 pedidos cada 10 min por cliente.
- **Asíncrono y pruebas:** Celery con reintentos para confirmaciones, avisos y tickets. Tiene 51 pruebas automatizadas.

### Públicos

| Repo | Descripción | Stack |
|---|---|---|
| [Gestor-de-Tareas](https://github.com/Riay/Gestor-de-Tareas) | Gestión de tareas, avance de proyectos y carga de trabajo por desarrollador | JavaScript · Node.js · Express · SQLite |
| [Corpocloud](https://github.com/Riay/Corpocloud) | App Android de notas con almacenamiento local | Java · SQLite |
| [SaludInteligente_RIAYTECH](https://github.com/Riay/SaludInteligente_RIAYTECH) | Investigación y app móvil de salud (TECMILENIO) | Java · Android |

---

## Stack

<p align="center">
  <img src="https://skillicons.dev/icons?i=py,django,js,ts,vue,react,dotnet,cs&theme=dark" alt="Lenguajes y frameworks"/><br/>
  <img src="https://skillicons.dev/icons?i=nodejs,express,bootstrap,jquery,html,css,java,androidstudio&theme=dark" alt="Frontend y móvil"/><br/>
  <img src="https://skillicons.dev/icons?i=nginx,windows,linux,aws,redis,postgres,sqlite,git,github,postman&theme=dark" alt="Infraestructura y herramientas"/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/SQL_Server-11151A?style=flat-square&logo=microsoftsqlserver&logoColor=FF6B2C" alt="SQL Server"/>
  <img src="https://img.shields.io/badge/IIS-11151A?style=flat-square&logo=microsoft&logoColor=FF6B2C" alt="IIS"/>
  <img src="https://img.shields.io/badge/Daphne_/_ASGI-11151A?style=flat-square&logo=django&logoColor=FF6B2C" alt="Daphne"/>
  <img src="https://img.shields.io/badge/DRF-11151A?style=flat-square&logo=django&logoColor=FF6B2C" alt="Django REST Framework"/>
  <img src="https://img.shields.io/badge/Redmine-11151A?style=flat-square&logo=redmine&logoColor=FF6B2C" alt="Redmine"/>
  <img src="https://img.shields.io/badge/Slack_API-11151A?style=flat-square&logo=slack&logoColor=FF6B2C" alt="Slack API"/>
  <img src="https://img.shields.io/badge/Zoom_API-11151A?style=flat-square&logo=zoom&logoColor=FF6B2C" alt="Zoom API"/>
  <img src="https://img.shields.io/badge/iCalendar_/_IMAP-11151A?style=flat-square&logo=googlecalendar&logoColor=FF6B2C" alt="iCalendar"/>
  <img src="https://img.shields.io/badge/WhatsApp_Cloud_API-11151A?style=flat-square&logo=whatsapp&logoColor=FF6B2C" alt="WhatsApp Cloud API"/>
  <img src="https://img.shields.io/badge/Django_Channels-11151A?style=flat-square&logo=django&logoColor=FF6B2C" alt="Django Channels"/>
  <img src="https://img.shields.io/badge/Celery-11151A?style=flat-square&logo=celery&logoColor=FF6B2C" alt="Celery"/>
  <img src="https://img.shields.io/badge/Vue.js-11151A?style=flat-square&logo=vuedotjs&logoColor=FF6B2C" alt="Vue"/>
  <img src="https://img.shields.io/badge/ReportLab_/_PDF-11151A?style=flat-square&logo=adobeacrobatreader&logoColor=FF6B2C" alt="PDF"/>
</p>

---

## Trayectoria

```text
2012 ──●── Empiezo a trabajar a los 17 años
       │
2017 ──●── Desarrollador full-stack
       │   Web, móvil (Android/Java) y bases de datos
       │
 ...  ──●── Capnet Solutions
       │   Plataformas de postventa para agencias automotrices
       │
HOY  ──◉── Gerente de Desarrollo
           Arquitectura · Equipo · Integraciones · Operación en MX y CO
```

---

## Actividad

<p align="center">
  <img src="https://streak-stats.demolab.com?user=Riay&theme=dark&hide_border=true&background=0B0D10&ring=FF6B2C&fire=FF6B2C&currStreakLabel=FF6B2C&sideLabels=C9D1D9&dates=8B949E&sideNums=F0F3F6&currStreakNum=F0F3F6&stroke=21262D&locale=es" alt="Racha de contribuciones" width="49%"/>
</p>

<p align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=Riay&bg_color=0B0D10&color=C9D1D9&line=FF6B2C&point=F0F3F6&area=true&area_color=FF6B2C&hide_border=true&custom_title=Contribuciones%20(incluye%20repos%20privados)" alt="Gráfica de actividad" width="100%"/>
</p>

---

<p align="center">
  <sub>¿Buscas a alguien que lleve un producto de la arquitectura a producción y sostenga al equipo en el camino? Escríbeme.</sub>
</p>
