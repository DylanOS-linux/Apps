# DylanOS Apps

Repositorio oficial de aplicaciones y componentes de software del ecosistema **DylanOS**.

Este repositorio contiene las aplicaciones, servicios, componentes del escritorio, widgets y herramientas desarrolladas para integrarse con DylanOS.

La arquitectura está organizada como un repositorio modular: cada proyecto puede desarrollarse, compilarse y evolucionar de forma independiente, mientras mantiene compatibilidad con el ecosistema DylanOS.

---

## 📦 Contenido

### 🖥️ Aplicaciones principales

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

### 🧩 Componentes del escritorio

| Proyecto | Descripción |
|---|---|
| `dylanos-widgets` | Sistema principal de widgets |
| `dylanos-widgets-lib` | Biblioteca compartida para widgets |
| `dylanos-widgets-calculator` | Widget de calculadora |
| `dylanos-widgets-calendar` | Widget de calendario |
| `dylanos-widgets-clock` | Widget de reloj |
| `dylanos-widgets-weather` | Widget meteorológico |
| `dylanos-widgets-network` | Widget de red |
| `dylanos-widgets-battery` | Widget de batería |
| `dylanos-widgets-media` | Widget multimedia |
| `dylanos-widgets-disk` | Widget de almacenamiento |
| `dylanos-widgets-info` | Widget de información |
| `dylanos-widgets-notes` | Widget de notas |
| `dylanos-widgets-todo` | Widget de tareas |
| `dylanos-widgets-photos` | Widget de fotografías |
| `dylanos-widgets-pomodoro` | Widget Pomodoro |
| `dylanos-widgets-resources` | Widget de recursos del sistema |
| `dylanos-widgets-screenshot` | Widget de capturas de pantalla |
| `dylanos-widgets-shortcuts` | Widget de accesos directos |
| `dylanos-widgets-updates` | Widget de actualizaciones |
| `dylanos-widgets-worldclock` | Widget de reloj mundial |
| `dylanos-widgets-clipboard` | Widget del portapapeles |
| `dylanos-widgets-nextevent` | Widget del próximo evento |

### 🧱 Componentes del sistema

| Proyecto | Descripción |
|---|---|
| `com.dylanos.activeapp` | Componente para identificar la aplicación activa |
| `com.dylanos.dashboard` | Dashboard del escritorio |
| `com.dylanos.dock` | Dock de DylanOS |
| `com.dylanos.search` | Componente de búsqueda |

### 🛠️ Otros

| Proyecto | Descripción |
|---|---|
| `workspace` | Componentes relacionados con el espacio de trabajo |

---

## 🏗️ Arquitectura

```text
Apps/
│
├── Aplicaciones
│   ├── dylanos-browser
│   ├── dylanos-store
│   ├── dylanos-app-center
│   ├── dylanos-explorer
│   ├── dylanos-configuration
│   ├── dylanos-control-center
│   ├── dylanos-process
│   ├── dylanos-spotlight
│   ├── calculator
│   ├── archivos
│   └── ozi-flappy
│
├── Escritorio
│   ├── com.dylanos.activeapp
│   ├── com.dylanos.dashboard
│   ├── com.dylanos.dock
│   └── com.dylanos.search
│
├── Widgets
│   ├── dylanos-widgets
│   ├── dylanos-widgets-lib
│   └── dylanos-widgets-*
│
└── workspace
```

El patrón `dylanos-widgets-*` permite mantener cada widget como un componente independiente sin perder la posibilidad de compartir infraestructura mediante `dylanos-widgets-lib`.

---

## 🎨 Filosofía de diseño

Las aplicaciones de DylanOS deben mantener una identidad visual coherente con el sistema.

Principios:

- **Negro, rojo y blanco** como identidad principal.
- Interfaces modernas y limpias.
- Integración con **Crimson Glass** cuando corresponda.
- Consistencia entre aplicaciones y componentes.
- Animaciones y efectos utilizados con moderación.
- Prioridad al rendimiento y la fluidez.
- Integración nativa con el escritorio cuando sea posible.

El objetivo no es clonar otro sistema operativo, sino construir una **identidad propia para DylanOS**.

---

## ⚙️ Tecnologías

Dependiendo del proyecto, este repositorio puede utilizar tecnologías como:

- **C++**
- **Qt 6**
- **QML**
- **Python**
- **JavaScript**
- **TypeScript**
- **React**
- **HTML / CSS**
- **Node.js**
- **D-Bus**
- **KDE Frameworks**
- APIs nativas de Linux

Cada aplicación debe documentar sus requisitos y proceso de compilación en su propio `README.md` cuando sea necesario.

---

## 🧪 Desarrollo

Clona el repositorio:

```bash
git clone https://github.com/dylanos/Apps.git
cd Apps
```

Para trabajar en una aplicación concreta:

```bash
cd dylanos-configuration
```

o:

```bash
cd dylanos-widgets-weather
```

Cada proyecto es responsable de documentar sus propias instrucciones de desarrollo, compilación y pruebas.

---

## 📋 Estándares

El código debe priorizar:

- **KISS**
- **DRY**
- **SOLID**
- Modularidad
- Seguridad
- Rendimiento
- Mantenibilidad
- Reutilización de componentes

Los componentes compartidos deben evitar duplicación innecesaria y, cuando sea apropiado, utilizar las bibliotecas existentes del ecosistema DylanOS.

---

## 🔀 Contribuciones

Las contribuciones deben mantener la estabilidad del ecosistema DylanOS.

Antes de realizar cambios:

1. Comprender la arquitectura existente.
2. Revisar dependencias y componentes relacionados.
3. Implementar cambios de forma modular.
4. Probar la aplicación afectada.
5. Comprobar que no se rompan integraciones existentes.
6. Documentar cambios relevantes.
7. Crear un Pull Request.

Los cambios que afecten múltiples aplicaciones o componentes deben evaluarse cuidadosamente antes de integrarse.

---

## 🧩 Relación con DylanOS

Este repositorio forma parte de la arquitectura modular de la organización DylanOS:

```text
DylanOS
│
├── DylanOS
│   └── Sistema operativo principal
│
├── Apps
│   └── Aplicaciones y componentes
│
├── Themes
│   └── Temas y personalización
│
├── Updates
│   └── Sistema de actualizaciones
│
└── Documentation
    └── Documentación del ecosistema
```

El repositorio `DylanOS` contiene el desarrollo principal del sistema operativo, mientras que `Apps` permite mantener el software del ecosistema de forma independiente y reutilizable.

---

## 📄 Licencia

Este repositorio se distribuye bajo los términos establecidos en [`LICENSE`](./LICENSE).

Las aplicaciones que incluyan una licencia específica o dependencias con licencias diferentes deben respetar sus respectivos términos.

---

## 🌐 DylanOS

**DylanOS** es un sistema operativo basado en Linux enfocado en una experiencia moderna, personalizable, integrada y eficiente.

**DylanOS Apps** es el espacio donde sus aplicaciones y componentes cobran vida.

> **Build the ecosystem. Not just the OS.**