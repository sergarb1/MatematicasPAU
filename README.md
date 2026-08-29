# SelectivoMates

Explicaciones de exámenes PAU de Matemáticas II (Valencia) con el estilo de Estefanía: paso a paso, claros, directos y con trucos para no fallar.

## Enlace al sitio

**https://sergarb1.github.io/MatematicasPAU/**

## Contenido

| Convocatoria | Problemas | Estado |
|:---|:---:|:---:|
| Junio 2025 - Ordinaria | 4 | ✅ |
| Junio 2025 - Reserva | 4 | ✅ |
| Junio 2024 - Ordinaria | 8 | ✅ |
| Julio 2024 - Extraordinaria | 8 | ✅ |
| Junio 2023 - Ordinaria | 8 | ✅ |

Cada problema incluye:
- **Narrativa** — contexto real para entender qué piden
- **Resolución paso a paso** — todos los apartados
- **Truco de Estefanía** — atajo para no perder tiempo
- **⚠️ Error típico** — lo que suele fallar
- **Tabla resumen** — método y resultado rápido
- **¿Qué llevarte para la vida?** — clave para el examen

## Estructura del repositorio

```
selectivoMates/
├── web/                              # Sitio Astro (GitHub Pages)
│   ├── src/content/examenes/         # Markdown con explicaciones
│   ├── src/pages/{año}/{conv}/       # Páginas por convocatoria
│   ├── src/Layout.astro              # Layout con KaTeX
│   └── astro.config.mjs              # Configuración (base: /MatematicasPAU)
├── examenes/                         # PDFs descargados y textos extraídos
│   ├── 2025/ordinaria/
│   ├── 2024/ordinaria/
│   └── ...
├── scripts/                          # Scripts de descarga
│   ├── descargar_examenes.py         # Descarga PDFs y extrae texto
│   └── ids_carpetas.py              # IDs de carpetas GVA
└── openspec/                         # Estándares de calidad
```

## Tecnologías

- **Astro** — generador de sitios estáticos
- **KaTeX** — renderizado de fórmulas matemáticas
- **Markdown** — contenido de las explicaciones
- **GitHub Pages** — hosting gratuito

## Desarrollo local

```bash
cd web
npm install
npm run dev       # http://localhost:4321
```

## Despliegue

El sitio se despliega automáticamente al hacer push a la rama `main` del repositorio.

```bash
cd web
npm run build          # Genera dist/
cd dist
git init
git add -A
git commit -m "Mensaje"
git push origin main
```

## Descarga de exámenes

```bash
# Todos los exámenes (2010-2025)
python scripts/descargar_examenes.py

# Un año específico
python scripts/descargar_examenes.py --year 2024
```
