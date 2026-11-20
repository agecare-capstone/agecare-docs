# Evidencias de documentación

| Archivo | Qué contiene |
|---|---|
| `backlog-jira.xlsx` | Export del tablero Jira (proyecto DAC05): todas las épicas, historias y subtareas con estado, responsable, sprint y puntos. Incluye las hojas **Resumen por sprint** y **Por integrante**. |
| `pull-requests.xlsx` | Pull requests integrados a `main` en el repositorio de la app, con fecha, autor y rama (clave de Jira). |
| `actas-sprints.md` | Índice de las actas de Sprint Planning, Sprint Review y Sprint Retrospective de los 5 sprints, con enlaces a Confluence. |
| `integracion-continua.md` | Pipelines de GitHub Actions (análisis estático, pruebas, builds y despliegue en Vercel) y flujo de trabajo Jira → rama → PR → CI. |

**Otras fuentes del proyecto**

- **Especificación de Endpoints Backend v1 (Alloxentric):** contrato de 82 endpoints que implementa el backend y consume la app.
- **Arquitectura del sistema:** app Flutter, Core API (FastAPI) en Azure, PostgreSQL y Blob Storage. Ver el README de [agecare-backend](https://github.com/agecare-capstone/agecare-backend).
- **Modelo de datos:** ver [Base de datos](../Evidencias%20de%20sistema/Base%20de%20datos/).
- **Tablero Jira:** `capstoneagecare.atlassian.net`.

En los archivos exportados, el integrante que dejó el equipo en octubre aparece como "Ex integrante".
