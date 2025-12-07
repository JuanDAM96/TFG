# ADR-002 — Seguridad Simplificada con API Key 

Estado: Aprobado
Fecha: 2025-12-07

## Contexto
En Sprint 1 se necesita protección básica de la API sin invertir días en un sistema completo de autenticación/usuarios. La prioridad es avanzar en funcionalidad core.

## Decisión
Autenticación básica por cabecera `X-API-KEY` (valor p. ej. `clase2025`) activada en perfil `dev`. 

## Motivo
Evitar bloqueo por complejidad de seguridad al inicio; protección suficiente para dev.

## Implementación (tareas accionables 2–3)
1. Filtro servlet que valide `X-API-KEY` en perfil `dev` en cada petición.
2. Configurar variable de entorno `API_KEY` y leerla desde el filtro (sin hardcode).
3. Responder `401 Unauthorized` con JSON descriptivo si la clave es inválida/ausente.

## Alternativas descartadas (al menos 2)
- JWT completo en Sprint 1
- OAuth2/OIDC con proveedor externo

## Consecuencias
- Protección básica (no producción)
  
## Trazabilidad
- HUs: HU-002 (Registro/Login), HU-003 (Perfil)
- RNFs: RNF-002 (Disponibilidad)
- Trello: https://trello.com/c/RcVbVX9s
