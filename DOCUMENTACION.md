# 📋 Documentación - Multi-Site Hosting con Firebase

## Proyecto: cristhian-vasquez-2026

**Fecha de configuración:** 6 de febrero de 2026  
**Tecnología:** SvelteKit (Svelte 5) + adapter-static + Firebase Hosting

---

## 🏗️ ¿Qué es esto?

Este proyecto permite alojar **múltiples sitios web** dentro de un solo proyecto de Firebase.  
Cada sitio es una aplicación SvelteKit independiente que se compila a HTML estático y se despliega a su propia URL en Firebase Hosting.

---

## 🌐 Sitios desplegados

| Sitio | URL | Carpeta del código | Carpeta del build |
|-------|-----|--------------------|-------------------|
| Golden House Peru | https://goldenhouseperu-618e1.web.app | `golden/goldenhouseperu/src/` | `golden/goldenhouseperu/build/` |
| Valparaíso | https://valparaiso-cv.web.app | `Valparaiso/valparaiso/src/` | `Valparaiso/valparaiso/build/` |

---

## 📁 Estructura del proyecto

```
cristhianVazquez-Multi-site Hosting/
├── firebase.json          ← Configuración de hosting (define los sitios)
├── .firebaserc            ← Vincula targets con sitios de Firebase
├── DOCUMENTACION.md       ← Este archivo
│
├── golden/
│   └── goldenhouseperu/
│       ├── src/            ← Código fuente (Svelte)
│       │   ├── app.html
│       │   ├── app.css
│       │   ├── lib/
│       │   │   └── components/   ← Componentes (Hero, About, Contact, etc.)
│       │   └── routes/
│       │       ├── +page.svelte   ← Página principal
│       │       ├── +layout.svelte
│       │       └── +layout.js
│       ├── build/          ← Archivos compilados (lo que se sube a Firebase)
│       ├── package.json
│       ├── svelte.config.js
│       └── vite.config.js
│
└── Valparaiso/
    └── valparaiso/
        ├── src/            ← Código fuente (Svelte)
        ├── build/          ← Archivos compilados
        ├── package.json
        ├── svelte.config.js
        └── vite.config.js
```

---

## ⚙️ Archivos de configuración clave

### `firebase.json`
Define los sitios de hosting. Cada entrada tiene:
- **target**: nombre lógico del sitio (ej: `golden`, `valparaiso`)
- **public**: ruta a la carpeta `build/` de cada proyecto
- **rewrites**: redirige todas las rutas a `index.html` (SPA)

### `.firebaserc`
Vincula cada **target** con el **sitio real** en Firebase:
- `golden` → `goldenhouseperu-618e1`
- `valparaiso` → `valparaiso-cv`

### `svelte.config.js` (en cada proyecto)
Usa `@sveltejs/adapter-static` para generar HTML estático en la carpeta `build/`.

---

## 🚀 Comandos importantes

### Hacer build de un sitio

Debes entrar a la carpeta de cada proyecto y ejecutar:

```bash
# Golden House Peru
cd golden/goldenhouseperu
npm install
npm run build

# Valparaíso
cd Valparaiso/valparaiso
npm install
npm run build
```

### Desplegar a Firebase

Siempre ejecutar desde la **raíz del proyecto** (donde está `firebase.json`):

```bash
# Desplegar AMBOS sitios
firebase deploy --only hosting

# Desplegar SOLO Golden
firebase deploy --only hosting:golden

# Desplegar SOLO Valparaíso
firebase deploy --only hosting:valparaiso
```

### Desarrollo local

Para trabajar en un sitio en modo desarrollo:

```bash
cd golden/goldenhouseperu
npm run dev
# Se abre en http://localhost:5173

cd Valparaiso/valparaiso
npm run dev
# Se abre en http://localhost:5173
```

---

## 🔄 Flujo de trabajo completo

1. **Editar** el código en `src/` del sitio que quieras modificar
2. **Probar** localmente con `npm run dev`
3. **Compilar** con `npm run build`
4. **Volver a la raíz** del proyecto
5. **Desplegar** con `firebase deploy --only hosting`

---

## ➕ ¿Cómo agregar un nuevo sitio?

1. **Crear la carpeta** del nuevo proyecto SvelteKit:
   ```bash
   mkdir NuevoSitio/nuevositio
   cd NuevoSitio/nuevositio
   npx sv create .
   ```

2. **Configurar** `svelte.config.js` con `adapter-static`

3. **Crear el sitio en Firebase:**
   ```bash
   firebase hosting:sites:create nombre-del-sitio
   ```

4. **Vincular el target:**
   ```bash
   firebase target:apply hosting nombretarget nombre-del-sitio
   ```

5. **Agregar al `firebase.json`** una nueva entrada en el array `hosting`:
   ```json
   {
     "target": "nombretarget",
     "public": "NuevoSitio/nuevositio/build",
     "ignore": ["firebase.json", "**/.*", "**/node_modules/**"],
     "rewrites": [{ "source": "**", "destination": "/index.html" }]
   }
   ```

6. **Build y deploy:**
   ```bash
   cd NuevoSitio/nuevositio
   npm run build
   cd ../..
   firebase deploy --only hosting:nombretarget
   ```

---

## 🌍 Dominios personalizados

Para conectar un dominio propio (ej: `www.goldenhouseperu.com`):

1. Ir a [Firebase Console](https://console.firebase.google.com/project/cristhian-vasquez-2026/hosting)
2. Seleccionar el sitio deseado
3. Click en **"Add custom domain"**
4. Seguir los pasos para verificar DNS

---

## 📌 Notas

- Los warnings de Svelte sobre "element implicitly closed" y "unused CSS selector" son solo advertencias, no errores. El sitio funciona correctamente.
- Cada sitio es **independiente**: tienen su propio `package.json`, `node_modules`, y `build`.
- Firebase CLI debe estar instalado globalmente: `npm install -g firebase-tools`
- Debes estar logueado: `firebase login`
