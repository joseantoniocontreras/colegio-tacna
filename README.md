# I.E. 7047 "Tacna" Barranco — Sistema AIP

## 🚀 Cómo subir a GitHub Pages

1. Sube `index.html` a la raíz de tu repositorio en GitHub
2. Ve a **Settings → Pages → Deploy from branch → main / root**
3. Tu sitio quedará en: `https://TU_USUARIO.github.io/NOMBRE_REPO/`

---

## 🔥 Configuración de Firebase (OBLIGATORIO — hacer una sola vez)

### Paso 1 — Reglas de seguridad en Firebase
1. Ve a [console.firebase.google.com](https://console.firebase.google.com)
2. Abre tu proyecto **aip-tacna**
3. En el menú izquierdo: **Realtime Database → Reglas**
4. Borra todo lo que hay y pega exactamente esto:

```json
{
  "rules": {
    ".read": true,
    ".write": true
  }
}
```

5. Haz clic en **Publicar**

> ⚠️ Estas reglas permiten lectura y escritura pública — correcto para una web interna de colegio.
> Si en el futuro quieres más seguridad, se pueden agregar reglas por usuario.

### Paso 2 — Dominios autorizados
1. En Firebase: **Authentication → Settings → Dominios autorizados**
2. Agrega tu dominio de GitHub Pages: `tu_usuario.github.io`

---

## ⚙️ Datos técnicos

| Elemento | Valor |
|---|---|
| PIN de administrador | `1107` |
| Base de datos | Firebase Realtime Database |
| Logo | Guardado en localStorage del navegador (por tamaño) |
| Reservas, links, archivos | Firebase (tiempo real, compartido entre todos) |

## 📋 Estructura en Firebase

```
aip-tacna-rtdb/
├── reservations/
│   └── 2026-01-20__1__p3  →  {teacher, grade, section, ts}
├── disabled/
│   └── 2026-01-20__0__p1  →  true
├── quickLinks/
│   └── [{id, name, url, emoji}, ...]
└── sharedFiles/
    └── [{id, name, url, desc, emoji}, ...]
```

---
© 2026 I.E. 7047 "Tacna" — Barranco, Lima
