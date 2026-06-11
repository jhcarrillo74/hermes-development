# Workflow - Proyecto Existente + Feature Definida v3

## Objetivo

Implementar una feature ya definida en OpenSpec, manteniendo el contexto con archivos `.md`, usando Git como historial de implementación, y exigiendo validación técnica con evidencia antes de pasar a validación funcional del usuario.

---

## Principio base

```text
OpenSpec = Qué queremos construir.
Git = Qué se hizo, cuándo y cómo cambió.
Hermes = Implementa y valida técnicamente.
Usuario = Aprueba funcionalmente.
```

---

## Prompt inicial

```text
Inicializa el proyecto.

Lee:
- ~/AI-Standards/hermes-master.md
- openspec/product.md
- openspec/architecture.md
- openspec/decisions.md
- openspec/features/[nombre-feature].md

Revisa Git:
- git status
- git branch
- git log reciente
- git diff si corresponde

Verifica acceso a:
- código
- terminal
- git
- Playwright
- Chrome
- logs

No implementes todavía.

Primero resume:
1. Proyecto
2. Stack
3. Feature a implementar
4. Criterios de aceptación
5. Riesgos
6. Archivos probables a modificar
7. Accesos disponibles
8. Estado Git actual
```

---

## Prompt de implementación

```text
OK, implementa la feature siguiendo OpenSpec.

Valida con Playwright/Chrome.

Debes revisar y reportar evidencia de:
- logs de terminal
- consola del navegador
- network requests
- errores de API
- resultado de Playwright

Corrige cualquier error encontrado.

No cierres la tarea hasta dejarla lista para mi validación funcional.
No actualices OpenSpec salvo que yo lo pida explícitamente.
```

---

## Diagrama de flujo completo

```text
CASO B: PROYECTO EXISTENTE + FEATURE YA DEFINIDA EN OPENSPEC

┌──────────────────────────────────────────┐
│ 1. NUEVO CHAT / PÉRDIDA DE CONTEXTO      │
└────────────────────┬─────────────────────┘
                     ▼
┌──────────────────────────────────────────┐
│ 2. TÚ ESCRIBES EN TELEGRAM               │
│                                          │
│ "Inicializa el proyecto.                 │
│ Lee hermes-master.md y openspec.         │
│ Revisa git.                              │
│ Verifica accesos.                        │
│ No implementes todavía.                  │
│ Resume contexto y plan."                 │
└────────────────────┬─────────────────────┘
                     ▼
┌──────────────────────────────────────────┐
│ 3. HERMES LEE ARCHIVOS                   │
│                                          │
│ ~/AI-Standards/hermes-master.md          │
│ openspec/product.md                      │
│ openspec/architecture.md                 │
│ openspec/decisions.md                    │
│ openspec/features/[feature].md           │
│                                          │
│ Nota: OpenSpec define qué construir.     │
│ No se usa para registrar avance.         │
└────────────────────┬─────────────────────┘
                     ▼
┌──────────────────────────────────────────┐
│ 4. HERMES REVISA GIT                     │
│                                          │
│ git status                               │
│ git log                                  │
│ git branch                               │
│ git diff si corresponde                  │
│                                          │
│ Git define qué se ha construido.         │
└────────────────────┬─────────────────────┘
                     ▼
┌──────────────────────────────────────────┐
│ 5. HERMES VERIFICA ACCESOS               │
│                                          │
│ Código                                   │
│ Terminal                                 │
│ Git                                      │
│ Playwright                               │
│ Chrome                                   │
│ Logs                                     │
└────────────────────┬─────────────────────┘
                     ▼
┌──────────────────────────────────────────┐
│ 6. HERMES RESUME ANTES DE PROGRAMAR      │
│                                          │
│ Proyecto                                 │
│ Stack                                    │
│ Feature a implementar                    │
│ Criterios de aceptación                  │
│ Estado Git actual                        │
│ Riesgos                                  │
│ Archivos probables a modificar           │
│ Accesos disponibles                      │
└────────────────────┬─────────────────────┘
                     ▼
┌──────────────────────────────────────────┐
│ 7. TÚ DAS OK                             │
│                                          │
│ "OK, implementa siguiendo OpenSpec.      │
│                                          │
│ Prueba con Playwright/Chrome.            │
│ Revisa logs, consola y network.          │
│                                          │
│ Debes revisar y reportar evidencia de:   │
│ - logs de terminal                       │
│ - consola del navegador                  │
│ - network requests                       │
│ - errores de API                         │
│ - resultado de Playwright                │
│                                          │
│ Corrige cualquier error encontrado.      │
│                                          │
│ Antes de solicitar validación funcional: │
│ - deja el entorno operativo              │
│ - deja el servidor levantado             │
│ - entrega URL de acceso                  │
│ - entrega credenciales de prueba         │
│ - entrega datos de prueba necesarios     │
│ - indica exactamente qué debo probar     │
│ - indica limitaciones conocidas          │
│                                          │
│ No cierres la tarea hasta dejarla lista  │
│ para mi validación funcional.            │
│                                          │
│ Cuando entregues la validación funcional:│
│ - entrega la información una sola vez    │
│ - no repitas la checklist               │
│ - no generes recordatorios               │
│ - no vuelvas a solicitar validación      │
│ - no continúes ejecutando acciones       │
│ - no consumas más tokens                 │
│                                          │
│ Después de entregar la validación       │
│ funcional,                               │
│ detente y espera mi respuesta explícita.│
│                                          │
│ No actualices OpenSpec salvo que yo lo   │
│ pida explícitamente."                    │
└────────────────────┬─────────────────────┘
                     ▼
┌──────────────────────────────────────────┐
│ 8. HERMES IMPLEMENTA                     │
│                                          │
│ Revisa código existente                  │
│ Modifica archivos                        │
│ Mantiene arquitectura actual             │
│ Evita refactors innecesarios             │
│ No actualiza OpenSpec                    │
└────────────────────┬─────────────────────┘
                     ▼
┌──────────────────────────────────────────┐
│ 9. HERMES PRUEBA Y ANALIZA EVIDENCIA     │
│                                          │
│ Levanta app                              │
│ Ejecuta flujo funcional                  │
│ Captura logs terminal                    │
│ Captura consola navegador                │
│ Captura network requests                 │
│ Revisa errores API                       │
│ Ejecuta Playwright                       │
│ Analiza evidencia                        │
└────────────────────┬─────────────────────┘
                     ▼
        ┌────────────────────────────────────────────┐
        │           ¿Hay errores?                    │
        └────────────────────┬───────────────────────┘
                             │
                  ┌──────────┴──────────┐
                  │                     │
                 SÍ                    NO
                  │                     │
                  ▼                     ▼
┌──────────────────────────────┐   ┌──────────────────────────────────────┐
│ 10A. HERMES DEPURA           │   │ 10B. HERMES ENTREGA EVIDENCIA        │
│                              │   │ TÉCNICA                              │
│ Identifica causa raíz         │   │                                      │
│ Corrige código                │   │ Debe reportar:                       │
│ Vuelve a levantar app         │   │ - resultado logs terminal            │
│ Vuelve a probar               │   │ - resultado consola navegador        │
│ Vuelve a revisar evidencia    │   │ - resultado network requests         │
└─────────┬────────────────────┘   │ - resultado Playwright               │
          │                        │ - errores encontrados                │
          │                        │ - correcciones realizadas            │
          │                        │                                      │
          │                        │ Estado: listo para validación        │
          │                        │ funcional del usuario.               │
          └──────────────────┬─────┴──────────────────────────────────────┘
                             ▼
          ┌────────────────────────────────────────────┐
          │ 10C. HERMES PREPARA VALIDACIÓN USUARIO     │
          │                                            │
          │ Antes de entregar, Hermes debe dejar       │
          │ todo listo para pruebas funcionales.       │
          │                                            │
          │ Debe entregar:                             │
          │                                            │
          │ ✓ Servidor levantado                       │
          │ ✓ URL de acceso                            │
          │ ✓ Credenciales de prueba                   │
          │ ✓ Datos de prueba necesarios               │
          │ ✓ Casos de prueba sugeridos                │
          │ ✓ Qué probar específicamente               │
          │ ✓ Limitaciones conocidas                   │
          │                                            │
          │ Ejemplo:                                   │
          │                                            │
          │ URL: http://localhost:3000                 │
          │ Usuario: test@empresa.com                  │
          │ Password: Test123!                         │
          │                                            │
          │ Probar:                                    │
          │ 1. Crear pedido                            │
          │ 2. Aplicar propina                         │
          │ 3. Emitir boleta                           │
          │ 4. Revisar total calculado                 │
          │                                            │
          │ Estado: listo para validación funcional.   │
          └────────────────────┬───────────────────────┘
                               ▼
          ┌────────────────────────────┐
          │ 11. TÚ PRUEBAS             │
          │                            │
          │ Validación funcional       │
          │ Revisión visual            │
          │ Casos reales de negocio    │
          │ Casos borde                │
          └──────────────┬─────────────┘
                         ▼
               ┌────────────────────┐
               │ ¿Tú apruebas?      │
               └───────┬────────────┘
                       │
            ┌──────────┴──────────┐
            │                     │
           NO                    SÍ
            │                     │
            ▼                     ▼
  ┌───────────────────┐   ┌────────────────────────────┐
  │ 12A. REPORTAS     │   │ 12B. APROBACIÓN FUNCIONAL  │
  │ AJUSTES           │   │                            │
  │                   │   │ Estado: aprobado por       │
  │ Ejemplo:          │   │ el usuario                 │
  │ "El botón se corta│   └──────────────┬─────────────┘
  │ en móvil"         │                  ▼
  └─────────┬─────────┘   ┌────────────────────────────┐
            ▼             │ 13. HERMES REVISA GIT      │
  ┌───────────────────┐   │                            │
  │ HERMES AJUSTA     │   │ git status                 │
  │ Y VUELVE A PROBAR │   │ git diff                   │
  │                   │   │ archivos modificados       │
  │ Vuelve a etapa 9  │   │                            │
  └─────────┬─────────┘   │ No actualiza OpenSpec      │
            │             └──────────────┬─────────────┘
            │                            ▼
            │             ┌────────────────────────────┐
            │             │ 14. HERMES SUGIERE COMMIT │
            │             │                            │
            │             │ Ejemplo:                   │
            │             │ feat: implementa propinas │
            │             └──────────────┬─────────────┘
            │                            ▼
            │             ┌────────────────────────────┐
            │             │ 15. FEATURE CERRADA        │
            │             │                            │
            │             │ Implementada               │
            │             │ Probada por Hermes         │
            │             │ Evidencia técnica revisada │
            │             │ Probada por usuario        │
            │             │ Aprobada funcionalmente    │
            │             │ Historial queda en Git     │
            │             └────────────────────────────┘
            │
            └────────────► vuelve a 9
```

---

## Evidencia técnica obligatoria

Antes de entregar la feature para validación funcional, Hermes debe reportar:

```text
Evidencia técnica:

Terminal:
- Resultado:
- Errores:
- Warnings críticos:

Consola navegador:
- Resultado:
- Errores:
- Warnings críticos:

Network:
- Requests exitosas:
- Requests fallidas:
- Status >= 400:
- Timeouts:
- Errores CORS:

Playwright:
- Flujo ejecutado:
- Resultado:
- Errores:

Correcciones realizadas:
-

Conclusión:
- Lista para validación funcional / No lista
```

---

## Regla de logs

Hermes no puede marcar una feature como lista para validación funcional si existe:

- error no explicado
- request fallida no esperada
- excepción sin resolver
- error de API sin analizar
- warning crítico sin justificar

Si un error es conocido y aceptado, debe indicarlo explícitamente en la entrega.

---

## Cierre

Después de aprobación funcional del usuario, Hermes debe:

1. Revisar Git.
2. Mostrar archivos modificados.
3. Sugerir commit.
4. No actualizar OpenSpec salvo instrucción explícita del usuario.

Ejemplo de commit:

```text
feat: implementa flujo de propinas
```