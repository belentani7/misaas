# SRS -- misaas
Fecha: 2026-09-25 | Estado: Draft | Traza a: PRD prd-misaas.md

## Requisitos funcionales

| ID | Requisito | Traza PRD | Prioridad |
|---|---|---|---|
| FR-001 | El sistema implementa: Hero WebGL — 4.600 partículas en esfera áurea con ruido procedural en el vertex shader, bl | F1 | Must |
| FR-002 | El sistema implementa: Diseño premium — tema oscuro, un solo acento (cian #00f3ff), glassmorphism real con bordes | F2 | Must |
| FR-003 | El sistema implementa: Dashboard funcional — gráfica de área con animación de entrada y crosshair, sparklines por | F3 | Must |
| FR-004 | El sistema implementa: Rendimiento — cero frameworks, cero build, DPR limitado a 2, animaciones pausadas fuera de | F4 | Must |
| FR-005 | El sistema implementa: Accesibilidad — canvas decorativos con aria-hidden, switches con role="switch", contraste  | F5 | Must |
| FR-006 | El sistema implementa: Colores y tipografía: variables CSS en :root (assets/css/main.css). Cambia --accent para r | F6 | Must |
| FR-007 | El sistema implementa: Núcleo WebGL: parámetros en la llamada a CoreScene (count, radius, size, turbulence, speed | F7 | Must |
| FR-008 | El sistema implementa: Datos: los agentes, logs y actividad del dashboard están en arrays al inicio de dashboard. | F8 | Must |

## Requisitos no funcionales

| ID | Requisito | Metrica | Traza |
|---|---|---|---|
| NFR-001 | Build reproducible | `build` pasa en CI | todos |
| NFR-002 | Calidad estatica | lint + typecheck sin errores | todos |
| NFR-003 | Seguridad | 0 secretos; validacion de entrada | FR-001 |
| NFR-004 | Observabilidad | logs estructurados y errores claros | todos |
| NFR-005 | Accesibilidad (si hay UI) | WCAG 2.1 AA | FR-001 |
| NFR-006 | CI verde | workflow en cada PR | todos |

## Trazabilidad

`PRD -> FR/NFR -> tests -> verificacion`. Todo cambio actualiza la documentacion
en el mismo PR y debe pasar la suite antes de fusionar.
