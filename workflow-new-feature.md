# Workflow - Proyecto Existente + Nueva Feature por Definir

## CASO A: PROYECTO EXISTENTE + NUEVA FEATURE POR DEFINIR

```text
┌──────────────────────────────────────────┐
│ 1. NUEVO CHAT / PÉRDIDA DE CONTEXTO      │
└────────────────────┬─────────────────────┘
                     ▼
┌──────────────────────────────────────────┐
│ 2. JORGE CARGA HERMES MASTER             │
│                                          │
│ Prompt:                                  │
│                                          │
│ "Lee hermes-master.md.                   │
│                                          │
│ Inicializa el proyecto.                  │
│                                          │
│ Verifica acceso a:                       │
│ - código                                │
│ - terminal                              │
│ - git                                   │
│ - Playwright                            │
│ - Chrome                                │
│ - logs                                  │
│                                          │
│ Revisa Git y resume el proyecto.         │
│ No implementes nada todavía."            │
└────────────────────┬─────────────────────┘
                     ▼
┌──────────────────────────────────────────┐
│ 3. HERMES INICIALIZA                     │
│                                          │
│ Lee hermes-master.md                     │
│ Revisa Git                               │
│ Verifica accesos                         │
│ Resume:                                  │
│ - proyecto                               │
│ - stack                                  │
│ - estado actual                          │
│ - funcionalidades existentes             │
│ - estado Git actual                      │
└────────────────────┬─────────────────────┘
                     ▼
┌──────────────────────────────────────────┐
│ 4. JORGE EXPLICA LA NECESIDAD            │
│                                          │
│ Prompt:                                  │
│                                          │
│ "Esto es lo que quiero/necesito hacer:   │
│                                          │
│ [descripción libre]                      │
│                                          │
│ Hazme las preguntas necesarias para      │
│ comprender completamente la necesidad.   │
│                                          │
│ Si crees que ya tienes información       │
│ suficiente, solicita autorización para   │
│ generar el resumen funcional.            │
│                                          │
│ El objetivo NO es programar.             │
│ El objetivo NO es crear OpenSpec aún.    │
│                                          │
│ El objetivo es construir un resumen      │
│ funcional validado que posteriormente     │
│ servirá como input para generar          │
│ OpenSpec.                                │
│                                          │
│ No implementes nada todavía."            │
└────────────────────┬─────────────────────┘
                     ▼
┌──────────────────────────────────────────┐
│ 5. HERMES ACTÚA COMO ANALISTA            │
│                                          │
│ Analiza:                                 │
│ - necesidad                              │
│ - contexto proyecto                      │
│ - arquitectura actual                    │
│ - impacto funcional                      │
│ - impacto técnico                        │
│ - riesgos                                │
│                                          │
│ Objetivo: descubrir requisitos.          │
│                                          │
│ NO programa.                             │
│ NO crea OpenSpec.                        │
│ NO implementa.                           │
└────────────────────┬─────────────────────┘
                     ▼
          ┌────────────────────────┐
          │ ¿Falta información?    │
          └──────────┬─────────────┘
                     │
          ┌──────────┴──────────┐
          │                     │
         SÍ                    NO
          │                     │
          ▼                     ▼
┌──────────────────────────┐  ┌──────────────────────────────┐
│ 6A. HERMES HACE          │  │ 6B. HERMES CREE TENER        │
│ PREGUNTAS                │  │ INFORMACIÓN SUFICIENTE       │
│ Jorge responde.          │  └──────────────┬───────────────┘
└─────────────┬────────────┘                 ▼
              │               ┌──────────────────────────────┐
              │               │ 7. HERMES SOLICITA           │
              │               │ AUTORIZACIÓN                 │
              │               │                              │
              │               │ "Creo tener información      │
              │               │ suficiente para definir la   │
              │               │ feature.                     │
              │               │                              │
              │               │ ¿Deseas que genere el        │
              │               │ resumen funcional que        │
              │               │ servirá como base para       │
              │               │ OpenSpec?"                   │
              │               └──────────────┬───────────────┘
              │                              ▼
              │               ┌──────────────────────────────┐
              │               │ 8. JORGE AUTORIZA            │
              │               │ GENERAR RESUMEN              │
              │               │                              │
              │               │ "Sí. Genera el resumen       │
              │               │ funcional."                 │
              │               └──────────────┬───────────────┘
              │                              ▼
              └────────── vuelve a 5 ◄───────┐
                                             │
                                             ▼
┌──────────────────────────────────────────┐
│ 9. HERMES GENERA RESUMEN FUNCIONAL       │
│                                          │
│ Entregable:                              │
│                                          │
│ - problema a resolver                    │
│ - objetivo de negocio                    │
│ - usuarios involucrados                 │
│ - flujo propuesto                       │
│ - reglas principales                    │
│ - supuestos                             │
│ - riesgos                               │
│ - dudas pendientes                      │
│                                          │
│ Base para OpenSpec.                      │
└────────────────────┬─────────────────────┘
                     ▼
┌──────────────────────────────────────────┐
│ 10. JORGE REVISA EL RESUMEN              │
│                                          │
│ ¿Hermes entendió correctamente           │
│ la necesidad?                            │
└────────────────────┬─────────────────────┘
                     ▼
           ┌───────────────────────┐
           │ ¿Resumen aprobado?    │
           └──────────┬────────────┘
                      │
           ┌──────────┴──────────┐
           │                     │
          NO                    SÍ
           │                     │
           ▼                     ▼
┌──────────────────────────┐   ┌──────────────────────────────┐
│ 11A. JORGE CORRIGE       │   │ 11B. JORGE APRUEBA          │
│ O ACLARA                 │   │ EL RESUMEN FUNCIONAL        │
└─────────────┬────────────┘   └──────────────┬───────────────┘
              │                               ▼
              └────────── vuelve a 5 ┌──────────────────────────────┐
                                     │ 12. HERMES PROPONE Y CREA RAMA GIT       │
                                     │                                          │
                                     │ A partir del resumen funcional aprobado, │
                                     │ Hermes debe proponer un nombre de rama.  │
                                     │                                          │
                                     │ Ejemplos:                                │
                                     │                                          │
                                     │ feature/propinas                         │
                                     │ feature/reservas-online                  │
                                     │ bugfix/error-login                       │
                                     │ hotfix/facturacion-produccion            │
                                     │ refactor/simplifica-checkout             │
                                     │                                          │
                                     │ Hermes debe mostrar:                     │
                                     │                                          │
                                     │ "Nombre de rama propuesto:               │
                                     │ feature/[nombre-feature]                 │
                                     │                                          │
                                     │ ¿Confirmas que cree esta rama?"          │
                                     └────────────────────┬─────────────────────┘
                                                          ▼
                                                ┌──────────────────────┐
                                                │ ¿Jorge aprueba rama? │
                                                └──────────┬───────────┘
                                                           │
                                                ┌──────────┴──────────┐
                                                │                     │
                                               NO                    SÍ
                                                │                     │
                                                ▼                     ▼
                                     ┌──────────────────────────┐   ┌──────────────────────────────┐
                                     │ JORGE AJUSTA NOMBRE      │   │ HERMES CREA RAMA             │
                                     │                          │   │                              │
                                     │ Ejemplo:                 │   │ git status                   │
                                     │ "Mejor usa:              │   │ git checkout -b              │
                                     │ feature/cierre-propinas" │   │ feature/[nombre-feature]     │
                                     └─────────────┬────────────┘   └──────────────┬───────────────┘
                                                   │                               ▼
                                                   └──────── vuelve a proponer     Continúa a OpenSpec
                                                    ▼
┌──────────────────────────────────────────┐
│ 14. HERMES CREA OPENSPEC                 │
│                                          │
│ Archivo:                                 │
│ openspec/features/[feature].md           │
│                                          │
│ Contenido:                               │
│                                          │
│ - Objetivo                               │
│ - Flujo usuario                          │
│ - Reglas negocio                         │
│ - Casos borde                            │
│ - Criterios aceptación                   │
│ - Impacto técnico                        │
└────────────────────┬─────────────────────┘
                     ▼
┌──────────────────────────────────────────┐
│ 15. HERMES PRESENTA OPENSPEC             │
│                                          │
│ Resume especificación y muestra          │
│ contenido del archivo generado.          │
└────────────────────┬─────────────────────┘
                     ▼
┌──────────────────────────────────────────┐
│ 16. JORGE REVISA OPENSPEC                │
│                                          │
│ Evalúa:                                  │
│ - alcance                                │
│ - experiencia usuario                    │
│ - reglas negocio                         │
│ - casos borde                            │
│ - criterios aceptación                   │
└────────────────────┬─────────────────────┘
                     ▼
           ┌───────────────────────┐
           │ ¿OpenSpec aprobado?   │
           └──────────┬────────────┘
                      │
           ┌──────────┴──────────┐
           │                     │
          NO                    SÍ
           │                     │
           ▼                     ▼
┌──────────────────────────┐   ┌──────────────────────────────┐
│ 17A. JORGE PIDE AJUSTES  │   │ 17B. FEATURE APROBADA        │
│                          │   │                              │
│ Hermes modifica          │   │ OpenSpec es la fuente        │
│ OpenSpec                 │   │ oficial de requerimientos.   │
└─────────────┬────────────┘   └──────────────┬───────────────┘
              │                               ▼
              └────────────► vuelve a 15
                              
┌──────────────────────────────────────────┐
│ 18. JORGE AUTORIZA IMPLEMENTACIÓN        │
│                                          │
│ Prompt:                                  │
│                                          │
│ "OK. Implementa la feature definida      │
│ en OpenSpec usando la rama creada."      │
└────────────────────┬─────────────────────┘
                     ▼
┌──────────────────────────────────────────┐
│ 19. CAMBIO A CASO B                      │
│                                          │
│ Implementación                           │
│ Validación técnica                       │
│ Logs                                     │
│ Consola                                  │
│ Network                                  │
│ Playwright                               │
│ Evidencia técnica                        │
│ Validación funcional usuario             │
│ Commit Git                               │
└──────────────────────────────────────────┘
```
