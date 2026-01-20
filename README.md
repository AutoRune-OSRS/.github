# AutoRune

A sophisticated multi-component automation platform built with modern technologies. AutoRune demonstrates advanced software engineering practices including bytecode manipulation, real-time communication, event-driven architecture, and human behavior simulation.

## Platform Architecture

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                              AutoRune Platform                               │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  ┌─────────────┐     WebSocket      ┌─────────────┐                        │
│  │  Dashboard  │◄──────────────────►│   Client    │                        │
│  │   (React)   │    Socket.IO       │  (Kotlin)   │                        │
│  └─────────────┘                    └──────┬──────┘                        │
│                                            │                                │
│                                            │ Uses                           │
│                                            ▼                                │
│                                    ┌──────────────┐                        │
│                                    │  Script-API  │                        │
│                                    │   (Kotlin)   │                        │
│                                    └──────┬───────┘                        │
│                                           │                                 │
│                                           │ Built on                        │
│                                           ▼                                 │
│  ┌─────────────┐    Generates     ┌──────────────┐                        │
│  │ Management  │─────────────────►│   OSRS-API   │                        │
│  │  (Kotlin)   │                  │  (Generated) │                        │
│  └──────┬──────┘                  └──────────────┘                        │
│         │                                                                   │
│         │ Uses                                                              │
│         ▼                                                                   │
│  ┌─────────────┐                                                           │
│  │  Utilities  │◄─────────── Shared across all modules                     │
│  │(Kotlin/Java)│                                                           │
│  └─────────────┘                                                           │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

## Repositories

### [Client](./Client)
The central orchestration layer of the platform. Manages multiple concurrent instances, executes user scripts, simulates human-like interactions, and communicates with the remote dashboard.

| Technology | Purpose |
|------------|---------|
| Kotlin 1.3 | Primary language |
| Kotlin Coroutines | Async operations |
| Guava EventBus | Event-driven architecture |
| Netty Socket.IO | Real-time communication |
| ASM 7.x | Bytecode manipulation |
| Swing + Substance | Modern UI theming |

**Key Features:**
- Multi-instance management with isolated ClassLoaders
- Coroutine-based script execution framework
- Human-like mouse simulation (Perlin noise, Bezier curves)
- Per-account behavioral characteristic profiles
- Real-time screenshot capture and state broadcasting

---

### [Dashboard](./Dashboard)
A modern React web application for remote monitoring and control via WebSocket communication.

| Technology | Purpose |
|------------|---------|
| React 16 | UI framework |
| Redux + Thunk | State management |
| Socket.IO Client | Real-time sync |
| Material-UI | Component library |
| Immer | Immutable state |

**Key Features:**
- Real-time instance/account/script management
- KPI dashboard with metrics visualization
- Bidirectional WebSocket communication
- Auto-reconnect with state recovery
- Responsive Material Design UI

---

### [Management](./Management)
Developer tools for maintaining the platform across version updates. Handles bytecode analysis, hook generation, API generation, and injection.

| Technology | Purpose |
|------------|---------|
| ASM 7.x | Bytecode manipulation |
| JavaPoet | Code generation |
| Kotlin Coroutines | Async processing |

**Modules:**

| Module | Purpose |
|--------|---------|
| **Updater** | 100+ bytecode analyzers for structure identification |
| **Injector** | Three-layer bytecode injection framework |
| **API Generator** | JavaPoet-based interface generation |
| **Mixins** | Horizontal code composition via injection |

**Key Features:**
- 18-stage deobfuscation pipeline
- Automated hook generation from bytecode patterns
- Mixin-based code extension system
- JSON-driven configuration

---

### [Utilities](./Utilities)
Shared library providing common functionality across all modules.

| Category | Components |
|----------|------------|
| **ASM Extensions** | 170+ opcode masks, pattern matching, instruction navigation |
| **JAR Utilities** | Download, load, parse JAR files |
| **Scene Math** | 3D projection, coordinate transforms, convex hull |
| **Deobfuscation** | 18 transformer stages for bytecode cleaning |
| **Resources** | World fetching, binary protocol parsing |

---

### [Script-API](./Script-Api)
Clean, coroutine-based API for script development with comprehensive game system coverage.

| Coverage | Details |
|----------|---------|
| **Widgets** | 800+ predefined mappings |
| **VarBits** | 700+ game variable definitions |
| **Actions** | 60+ interaction types |
| **Containers** | 15+ inventory/bank systems |
| **Skills** | All 23 skills with XP tracking |

---

## Technology Stack

### Languages
![Kotlin](https://img.shields.io/badge/Kotlin-1.3.61-purple?style=flat-square&logo=kotlin)
![Java](https://img.shields.io/badge/Java-11-orange?style=flat-square&logo=openjdk)
![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-yellow?style=flat-square&logo=javascript)

### Backend
![Maven](https://img.shields.io/badge/Maven-3.8-red?style=flat-square&logo=apachemaven)
![Coroutines](https://img.shields.io/badge/Kotlin_Coroutines-1.3.3-purple?style=flat-square)
![ASM](https://img.shields.io/badge/ASM-7.3.1-blue?style=flat-square)
![Guava](https://img.shields.io/badge/Guava-28.1-green?style=flat-square)

### Frontend
![React](https://img.shields.io/badge/React-16.11-blue?style=flat-square&logo=react)
![Redux](https://img.shields.io/badge/Redux-4.0-purple?style=flat-square&logo=redux)
![Material-UI](https://img.shields.io/badge/Material_UI-4.3-blue?style=flat-square&logo=mui)

### Communication
![Socket.IO](https://img.shields.io/badge/Socket.IO-2.3-black?style=flat-square&logo=socketdotio)
![Netty](https://img.shields.io/badge/Netty-4.x-blue?style=flat-square)

---

## Technical Highlights

### Bytecode Engineering
- **Custom ASM Framework** - 170+ opcode masks with chainable pattern matching
- **Three-Layer Injection** - API interfaces → Field/method accessors → Specialized transforms
- **Deobfuscation Pipeline** - Control flow fixing, multiplier correction, dead code removal
- **Code Generation** - JavaPoet-based automatic API interface generation

### Real-Time Architecture
- **WebSocket Protocol** - Bidirectional Socket.IO communication
- **Event-Driven Design** - Guava EventBus for loose coupling
- **State Synchronization** - Redux + real-time socket updates
- **Multi-Instance Support** - Concurrent session management

### Human Simulation
- **Mouse Path Algorithms** - Linear, Perlin noise, Bezier curves, human-like patterns
- **Behavioral Profiles** - Per-account DPI, polling rate, misclick probability
- **Input Simulation** - Realistic timing and movement characteristics

### Computational Geometry
- **3D Projection** - Model-to-canvas rendering with camera transforms
- **Convex Hull** - Jarvis march algorithm for click boundaries
- **Polygon Operations** - Sutherland-Hodgman clipping, point-in-polygon

---

## Project Structure

```
AutoRune/
├── Client/                 # Main Kotlin/Java client application
│   ├── autorune-client/           # Core instance management
│   ├── autorune-socket-server/    # Dashboard communication
│   ├── autorune-interaction/      # Human simulation
│   └── autorune-client-launcher/  # Entry point
│
├── Dashboard/              # React/Redux web application
│   ├── src/actions/              # Redux actions
│   ├── src/reducers/             # State reducers
│   ├── src/components/           # React components
│   └── src/services/             # Socket emitters
│
├── Management/             # Developer maintenance tools
│   ├── updater/                  # Bytecode analyzers
│   ├── injector/                 # Injection framework
│   ├── api-generator/            # Code generation
│   └── mixins/                   # Code composition
│
├── Utilities/              # Shared library
│   ├── asm/                      # Bytecode extensions
│   ├── scene/                    # 3D mathematics
│   └── deob/                     # Transformers
│
└── Script-Api/             # Scripting interface
    ├── entity/                   # Players, NPCs, skills
    ├── container/                # Inventory, banking
    ├── widget/                   # UI system
    └── vars/                     # Game variables
```

---

## Architecture Patterns

| Pattern | Implementation |
|---------|---------------|
| **Event-Driven** | Guava EventBus for decoupled component communication |
| **Unidirectional Data Flow** | Redux with Thunk middleware |
| **Mixin Composition** | Bytecode-level horizontal extension |
| **Repository Pattern** | Singleton instance management |
| **Code Generation** | JavaPoet for type-safe API creation |
| **Pipeline Processing** | Chained bytecode transformers |

---

## Building

### Prerequisites
- JDK 11+
- Maven 3.8+
- Node.js 12+

### Client / Management / Utilities / Script-API
```bash
mvn clean install
```

### Dashboard
```bash
cd Dashboard
npm install
npm start
```

---

## License

This project is proprietary software. All rights reserved.

---

<p align="center">
  <strong>Built with Kotlin, React, and advanced bytecode engineering</strong>
</p>
