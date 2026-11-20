<h1 align="center">DylanOS Apps</h1>

<p align="center">
  <strong>Aplicaciones, componentes de escritorio y widgets del ecosistema DylanOS.</strong><br>
  Repositorio modular: cada proyecto se desarrolla, compila y evoluciona de forma independiente.
</p>

<p align="center">
  <a href="https://www.debian.org/"><img src="https://img.shields.io/badge/base-Debian%2013-A81D33?style=flat-square&logo=debian&logoColor=white" alt="Base Debian 13"></a>
  <a href="https://kde.org/plasma-desktop/"><img src="https://img.shields.io/badge/escritorio-KDE%20Plasma%206-1D99F3?style=flat-square&logo=kde&logoColor=white" alt="Escritorio KDE Plasma 6"></a>
  <a href="./LICENSE"><img src="https://img.shields.io/badge/licencia-GPL--3.0--or--later-blue?style=flat-square" alt="Licencia GPL-3.0-or-later"></a>
</p>

---

## Acerca de este repositorio

Este repositorio reúne las aplicaciones, los servicios, los componentes del escritorio y los widgets desarrollados para integrarse con DylanOS.

La arquitectura es modular: cada proyecto puede desarrollarse, compilarse y evolucionar por separado, siempre que mantenga la compatibilidad con el ecosistema y con la identidad visual del sistema.

## Contenido

### Aplicaciones principales

| Proyecto | Descripción |
|---|---|
| `dylanos-configuration` | Centro de configuración de DylanOS |
| `dylanos-control-center` | Centro de control del sistema |
| `dylanos-explorer` | Explorador de archivos |
| `dylanos-store` | Tienda de aplicaciones |
| `dylanos-app-center` | Centro de aplicaciones |
| `dylanos-browser` | Navegador web de DylanOS |
| `dylanos-process` | Administrador de procesos |
| `dylanos-spotlight` | Buscador y lanzador de aplicaciones |
| `calculator` | Calculadora |
| `archivos` | Aplicación de archivos |
| `ozi-flappy` | Juego Flappy |

### Componentes del escritorio

| Proyecto | Descripción |
|---|---|
| `com.dylanos.activeapp` | Identificación de la aplicación activa |
| `com.dylanos.dashboard` | Dashboard del escritorio |
| `com.dylanos.dock` | Dock de DylanOS |
| `com.dylanos.search` | Componente de búsqueda |
| `workspace` | Componentes del espacio de trabajo |

### Widgets

| Proyecto | Descripción |
|---|---|
| `dylanos-widgets` | Sistema principal de widgets |
| `dylanos-widgets-lib` | Biblioteca compartida para widgets |
| `dylanos-widgets-battery` | Widget de batería |
| `dylanos-widgets-calculator` | Widget de calculadora |
| `dylanos-widgets-calendar` | Widget de calendario |
| `dylanos-widgets-clipboard` | Widget del portapapeles |
| `dylanos-widgets-clock` | Widget de reloj |
| `dylanos-widgets-disk` | Widget de almacenamiento |
| `dylanos-widgets-info` | Widget de información |
| `dylanos-widgets-media` | Widget multimedia |
| `dylanos-widgets-network` | Widget de red |
| `dylanos-widgets-nextevent` | Widget del próximo evento |
| `dylanos-widgets-notes` | Widget de notas |
| `dylanos-widgets-photos` | Widget de fotografías |
| `dylanos-widgets-pomodoro` | Widget Pomodoro |
| `dylanos-widgets-resources` | Widget de recursos del sistema |
| `dylanos-widgets-screenshot` | Widget de capturas de pantalla |
| `dylanos-widgets-shortcuts` | Widget de accesos directos |
| `dylanos-widgets-todo` | Widget de tareas |
| `dylanos-widgets-updates` | Widget de actualizaciones |
| `dylanos-widgets-weather` | Widget meteorológico |
| `dylanos-widgets-worldclock` | Widget de reloj mundial |

## Estructura

```text
Apps/
├── dylanos-browser/            # Aplicaciones
├── dylanos-store/
├── dylanos-app-center/
├── dylanos-explorer/
├── dylanos-configuration/
├── dylanos-control-center/
├── dylanos-process/
├── dylanos-spotlight/
├── calculator/
├── archivos/
├── ozi-flappy/
├── com.dylanos.activeapp/      # Componentes del escritorio
├── com.dylanos.dashboard/
├── com.dylanos.dock/
├── com.dylanos.search/
├── workspace/
├── dylanos-widgets/            # Widgets
├── dylanos-widgets-lib/
└── dylanos-widgets-*/
```

El patrón `dylanos-widgets-*` permite mantener cada widget como un componente independiente sin perder la infraestructura compartida de `dylanos-widgets-lib`.

## Desarrollo

Clona el repositorio:

```bash
git clone https://github.com/DylanOS-linux/Apps.git
cd Apps
```

Cada proyecto documenta sus propios requisitos, instrucciones de compilación y pruebas en su `README.md`. Para trabajar en un proyecto concreto:

```bash
cd dylanos-configuration
```

## Tecnologías

Según el proyecto, el repositorio utiliza:

- **C++**, **Qt 6** y **QML**
- **Python**
- **JavaScript** y **TypeScript**
- **React**
- **HTML** y **CSS**
- **Node.js**
- **D-Bus** y **KDE Frameworks**
- APIs nativas de Linux

## Criterios de desarrollo

Las aplicaciones de DylanOS mantienen una identidad visual coherente con el sistema:

- negro, rojo y blanco como identidad principal;
- interfaces limpias y animaciones moderadas;
- integración con Crimson Glass cuando corresponda;
- prioridad al rendimiento, la fluidez y la integración nativa con el escritorio.

El código prioriza KISS, DRY, SOLID, modularidad, seguridad, rendimiento, mantenibilidad y reutilización de componentes. Los componentes compartidos evitan la duplicación innecesaria y utilizan las bibliotecas existentes del ecosistema cuando es apropiado.

El objetivo no es clonar otro sistema operativo, sino construir una identidad propia para DylanOS.

## Contribuir

Antes de enviar un cambio:

1. Comprende la arquitectura existente.
2. Revisa las dependencias y los componentes relacionados.
3. Implementa el cambio de forma modular.
4. Prueba la aplicación afectada.
5. Comprueba que no se rompan las integraciones existentes.
6. Documenta los cambios relevantes.
7. Abre un pull request.

Los cambios que afectan a varias aplicaciones o componentes se evalúan antes de integrarse.

## Licencia

Este repositorio se distribuye bajo los términos de [`LICENSE`](./LICENSE) (GPL-3.0-or-later). Las aplicaciones con una licencia específica o con dependencias de terceros respetan sus propios términos.

## Ecosistema DylanOS

| Repositorio | Contenido |
|---|---|
| [DylanOS](https://github.com/dylanneymarmontalvo2014-lgtm/DylanOS) | Sistema operativo y desarrollo principal |
| [Apps](https://github.com/DylanOS-linux/Apps) | Aplicaciones y componentes |
| [Branding](https://github.com/DylanOS-linux/Branding) | Identidad visual y recursos oficiales |
| [Documentation](https://github.com/DylanOS-linux/Documentation) | Documentación técnica |
| [Temas](https://github.com/DylanOS-linux/Temas) | Temas y personalización |

---

<p align="center"><sub>DylanOS — Tu sistema, tu experiencia.</sub></p>
