# SRM — Sistema de Catastro

Aplicación web para la gestión catastral: registro de predios, copropietarios,
delimitación geoespacial y generación de documentos. Construida con
**React + TypeScript + Vite + Tailwind**, con mapas interactivos y backend en
**Supabase**.

> ⚠️ Este repo y `sistemacatastro` comparten la misma base de código
> (package.json idéntico). Se mantiene aquí como versión de trabajo y el otro
> como snapshot del sistema completo. Considera unificarlos en uno solo.

## Stack

- React 18 + TypeScript + Vite
- Tailwind CSS
- Mapas: Leaflet + react-leaflet + Leaflet.draw + Turf
- Base de datos y auth: Supabase
- Offline-first local: Dexie (IndexedDB)
- Exportación: react-pdf, FileSaver, QRCode

## Requisitos

- Node.js 18+ y npm
- Una cuenta de Supabase con un proyecto creado

## Puesta en marcha

```bash
npm install
```

Crea un archivo `.env` en la raíz con las credenciales de tu proyecto Supabase:

```bash
VITE_SUPABASE_URL=https://<tu-proyecto>.supabase.co
VITE_SUPABASE_ANON_KEY=<tu-anon-key>
```

Aplica el esquema de base de datos que está en `supabase/` (schema.sql,
storage.sql, usuarios.sql) desde el SQL Editor de Supabase.

```bash
npm run dev
```

## Scripts

| Comando | Descripción |
| --- | --- |
| `npm run dev` | Servidor de desarrollo |
| `npm run build` | Build de producción |
| `npm run preview` | Previsualiza el build |
| `npm run typecheck` | Verificación de tipos |
| `npm run lint` | Linting |

## Estructura

```
src/
  lib/supabase.ts   # Cliente Supabase
  ...               # Componentes y vistas del sistema catastral
supabase/           # Scripts SQL de esquema, storage y usuarios
public/             # Assets y datos geográficos (torbes_boundary.json)
```

---

Desarrollado por [junnior-dev](https://github.com/junnior-dev).
