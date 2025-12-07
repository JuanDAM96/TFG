# RNF-001 — Rendimiento API
Estado: Aprobado
Versión: v1.0.0
Fecha: 2025-12-07
Autores: Juan Antonio Lucas Márquez

## Descripción
La API debe responder con fluidez para operaciones clave del entregable E1.

## Métrica
p95 de latencia por endpoint (ms) en entorno de demo.

## Umbral
- P95 ≤ 300 ms (carga normal ~100 concurrentes)

## Método(s) de verificación
- Pruebas de carga (k6/JMeter), reporte P95

## Trazabilidad
- HU: HU-001, HU-004, HU-005, HU-006, HU-007
- Release: E1-v1.1

## Historial de cambios
- v1.1 (2025-12-07): Definición inicial para E1.
