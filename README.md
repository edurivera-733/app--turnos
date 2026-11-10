# 🌙☀️ Calendario de turnos

Calendario de turnos editable para iPhone: **7x7 día y noche** (intercalado), **7x7 solo de día** o **4x3 solo de día**. Ya viene cargado con la secuencia del **Calendario de Turnos 2026** y la sigue automáticamente en los años siguientes.

## Turno 7x7 día y noche (intercalado, ciclo de 28 días)

| Día | Qué pasa |
|---|---|
| **Martes** | Subo a faena y trabajo la 1ª noche 🌙 |
| Miércoles → lunes | Noches 2 a 7 🌙 |
| **Martes (mañana)** | Termina el turno de noche y bajo de faena ⬇️ |
| Miércoles → lunes | Descanso 🏠 |
| **Martes** | Subo a faena ⬆️ |
| Miércoles → martes | Turno de día ☀️ (el último martes bajo en la noche ⬇️) |
| Miércoles → lunes | Descanso 🏠 |

La referencia es el martes 6 de enero de 2026 (inicio de noche).

## Turno 7x7 solo de día (ciclo de 14 días)

| Día | Qué pasa |
|---|---|
| **Lunes** (en la noche) | Subo a faena ⬆️ |
| Martes → lunes | Turno de día ☀️ (7 días; el último lunes bajo en la noche ⬇️) |
| Martes → domingo | Descanso 🏠 |

También con subida el **martes** (trabajo de miércoles a martes, descanso de miércoles a lunes) u otro día.

## Turno 4x3 (solo de día, ciclo de 7 días)

| Día | Qué pasa |
|---|---|
| **Lunes** | Subo a faena y trabajo ⬆️☀️ |
| Martes y miércoles | Turno de día ☀️ |
| **Jueves** | Último día; al terminar bajo ⬇️ |
| Viernes → domingo | Descanso 🏠 |

El día de inicio también se puede cambiar (por ejemplo, martes a viernes).

## Feriados de Chile

Los feriados aparecen **en rojo** (número en rojo, borde y barra roja) en el calendario del mes, la vista del año y los próximos días, con su nombre al tocar el día. Se pueden ocultar en *Ajustes*.

### Cambiar el tipo de turno o el día de ingreso

En **Ajustes → Cambiar turno o día de ingreso** eliges **7x7 día y noche**, **7x7 solo día** o **4x3 solo día**, y el día en que subes (martes o miércoles para día y noche; lunes o martes para solo día; lunes para 4x3; u otro día) y la fecha en que subes al turno de noche. Con esa sola fecha la app calcula todas las subidas, bajadas, días y noches (por ejemplo, con ingreso miércoles: noches de miércoles a martes, bajada el miércoles en la mañana, subida el miércoles y turno de día de jueves a miércoles).

- **Desde esa fecha:** lo anterior queda como estaba (útil cuando la empresa cambia la secuencia a partir de cierta semana).
- **Todo el calendario:** recalcula también los meses pasados (útil para otra persona o para corregir la fecha).

Los cambios quedan en un historial y se pueden quitar.

## Qué incluye

- **Hoy:** turno de hoy (noche 3 de 7, descanso 2 de 6…), barra de avance, cuántos días faltan para la próxima subida y bajada, próximos 21 días y lo que tienes agendado.
- **Mes:** calendario con ☀️ día, 🌙 noche, ↑ subida, ↓ bajada, feriados de Chile en rojo. Toca un día para:
  - agregar **vacaciones, permisos, cursos, licencia médica, día administrativo, turno extra, cambio de turno, examen médico** u otro (un día o un rango; atajo “todo el turno”),
  - **cambiar el turno de ese día** a mano (día, noche, descanso, subida o bajada),
  - escribir una **nota**.
- **Año:** los 12 meses como en el calendario impreso.
- **Resumen:** días, noches, descansos y subidas del año, días de vacaciones o permiso (y cuántos eran días de turno), tabla por mes.
- **Ajustes:** día y fecha de ingreso al turno de noche (martes, miércoles u otro), horarios, categorías editables (emoji, nombre y color), tema claro u oscuro, **exportar al Calendario del iPhone** (.ics con aviso el día antes de subir), respaldo en iCloud y opción para importarlo.

## Instalar en el iPhone

1. Con GitHub Pages activo en este repositorio, abre en **Safari**: `https://edurivera-733.github.io/app--turnos/`
2. **Compartir** → **Agregar a pantalla de inicio** → **Agregar**.
3. Abre **Turnos** desde la pantalla de inicio. Funciona sin internet y los datos quedan solo en tu teléfono.

### Activar GitHub Pages (una sola vez)

En GitHub: **Settings** → **Pages** → *Source: Deploy from a branch* → rama `main` (o `claude/inspiring-allen-atqxm0` para probar ya) y carpeta **`/ (root)`** → **Save**. En un par de minutos la app queda en la dirección de arriba.

## Probar en el computador

```bash
python3 -m http.server 8000
# abre http://localhost:8000
```

## Estructura

```
index.html            Estructura de la app y barra de pestañas
css/styles.css        Estilos (modo claro y oscuro, adaptado a iPhone)
js/app.js             Secuencia 7x7, vistas, eventos y almacenamiento local
manifest.webmanifest  Datos para instalarla como app
sw.js                 Service worker (uso sin conexión)
icons/                Íconos de la app
```

Sin dependencias ni compilación: HTML, CSS y JavaScript puro.
