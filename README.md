# Colegio Centenario "7047 Tacna" — Sistema de Reservas AIP

Página web interna para gestionar las reservas del Aula de Innovaciones Pedagógicas (AIP).

## 🚀 Cómo subir a GitHub Pages

1. Crea un repositorio en GitHub (ej: `colegio-7047-tacna`)
2. Sube el archivo `index.html` a la raíz del repositorio
3. Ve a **Settings → Pages → Deploy from branch → main / root**
4. Tu sitio estará en: `https://TU_USUARIO.github.io/colegio-7047-tacna/`

## ⚙️ Configuración rápida

Abre `index.html` y edita las siguientes variables al inicio del `<script>`:

```js
const ADMIN_PIN = "7047";   // ← cambia esto por tu PIN secreto
```

También puedes ajustar las secciones:
```js
const SECTIONS = ["1°A","1°B", ...];  // ← agrega o quita secciones
```

## 📋 Funcionalidades

- ✅ Horario semanal visual (Lun–Vie, 9 horas pedagógicas)
- ✅ Reserva de turnos con nombre del docente y sección
- ✅ Prevención de doble reserva (turnos tomados no se pueden pisar)
- ✅ Límite de 2 horas por sección por semana
- ✅ Navegación entre semanas (anterior / siguiente)
- ✅ Panel de administrador con PIN para eliminar reservas
- ✅ Filtro por nombre de docente
- ✅ Datos guardados en localStorage (persisten en el navegador)
- ✅ Diseño responsive (funciona en celular)

## 📅 Horario configurado

| Período | Horario |
|---------|---------|
| 1ª hora | 7:30 – 8:15 |
| 2ª hora | 8:15 – 9:00 |
| 🔴 Recreo | 9:00 – 9:15 |
| 3ª hora | 9:15 – 10:00 |
| 4ª hora | 10:00 – 10:45 |
| 5ª hora | 10:45 – 11:30 |
| 6ª hora | 11:30 – 12:15 |
| 🔴 Recreo | 12:15 – 12:45 |
| 7ª hora | 12:45 – 13:30 |
| 8ª hora | 13:30 – 14:15 |
| 9ª hora | 14:15 – 15:00 |

## ⚠️ Nota sobre los datos

Los datos se guardan en `localStorage` del navegador. Esto es ideal para uso interno en una red donde los docentes usan el mismo dispositivo o se accede desde una PC fija. Si necesitas que los datos sean compartidos entre dispositivos, el siguiente paso sería integrar una base de datos (Firebase, Supabase, etc.).

---
© 2026 Colegio Centenario "7047 Tacna" · Barranco, Lima
