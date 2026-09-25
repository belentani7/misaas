# PRD -- misaas
Fecha: 2026-09-25 | Estado: Draft (auditoria automatica, requiere revision humana) | Autor: auditoria belentani7 (NOIACORE)

## 1. Problema

Frontend SaaS premium con hero WebGL para orquestación de agentes autónomos. Landing page + dashboard operativo, sin dependencias de build: HTML, CSS y JavaScript puro.

## 2. Usuarios objetivo

- **Primario**: usuario final que necesita resolver el caso de uso de misaas.
- **Secundario**: equipo/persona que mantiene y despliega el proyecto.
- **Terciario**: agentes CLI que operan sobre el repositorio.

## 3. Features (MoSCoW)

| ID | Feature | MoSCoW |
|---|---|---|
| F1 | Hero WebGL — 4.600 partículas en esfera áurea con ruido procedural en el vertex shader, blending aditivo, parallax de ratón y pausa automáti | Must |
| F2 | Diseño premium — tema oscuro, un solo acento (cian #00f3ff), glassmorphism real con bordes y profundidad, grano de película, scanlines y rej | Must |
| F3 | Dashboard funcional — gráfica de área con animación de entrada y crosshair, sparklines por KPI, filtros por estado, búsqueda con Ctrl+K, swi | Must |
| F4 | Rendimiento — cero frameworks, cero build, DPR limitado a 2, animaciones pausadas fuera de viewport, prefers-reduced-motion respetado en tod | Must |
| F5 | Accesibilidad — canvas decorativos con aria-hidden, switches con role="switch", contraste de texto ≥ 4.5:1, fallback CSS si WebGL no está di | Must |
| F6 | Colores y tipografía: variables CSS en :root (assets/css/main.css). Cambia --accent para recolorear todo el sistema. | Must |
| F7 | Núcleo WebGL: parámetros en la llamada a CoreScene (count, radius, size, turbulence, speed). El shader vive en webgl-core.js. | Must |
| F8 | Datos: los agentes, logs y actividad del dashboard están en arrays al inicio de dashboard.js, listos para sustituir por una API real. | Must |
| F90 | Checklist de produccion (build, tests, deploy, seguridad) | Should |
| F91 | Documentacion viva (esta cadena) | Must |

## 4. Criterios de aceptacion (GWT)

### F1 -- Hero WebGL — 4.600 partículas en esfera áurea con ruido proc
- Given el usuario en el contexto de misaas / When usa Hero WebGL — 4.600 partículas en esfera áurea con  / Then obtiene el resultado esperado sin error.
- Given entrada invalida / When la envia / Then recibe un error generico y el detalle queda en logs.

### F2 -- Diseño premium — tema oscuro, un solo acento (cian #00f3ff),
- Given el usuario en el contexto de misaas / When usa Diseño premium — tema oscuro, un solo acento (cian / Then obtiene el resultado esperado sin error.
- Given entrada invalida / When la envia / Then recibe un error generico y el detalle queda en logs.

### F3 -- Dashboard funcional — gráfica de área con animación de entra
- Given el usuario en el contexto de misaas / When usa Dashboard funcional — gráfica de área con animació / Then obtiene el resultado esperado sin error.
- Given entrada invalida / When la envia / Then recibe un error generico y el detalle queda en logs.

### F4 -- Rendimiento — cero frameworks, cero build, DPR limitado a 2,
- Given el usuario en el contexto de misaas / When usa Rendimiento — cero frameworks, cero build, DPR lim / Then obtiene el resultado esperado sin error.
- Given entrada invalida / When la envia / Then recibe un error generico y el detalle queda en logs.


## 5. Metricas de exito

- Build reproducible en un comando.
- CI verde en cada PR.
- Cero secretos en el repositorio.
- Documentacion actualizada en el mismo PR que el codigo.

## 6. Out of scope

- Funcionalidad no descrita en el README vigente.
- Cambios que rompan compatibilidad sin ADR que lo justifique.
