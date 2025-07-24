# 🤝 Contributing to EIDOLON

¡Gracias por tu interés en contribuir a EIDOLON! Este documento te guiará através del proceso de contribución para mantener un alto estándar de calidad en el proyecto.

## 🌟 Code of Conduct

Al participar en este proyecto, te comprometes a mantener un ambiente respetuoso y colaborativo. Lee nuestro [Código de Conducta](CODE_OF_CONDUCT.md) antes de contribuir.

## 🚀 Getting Started

### Prerequisites
- Node.js 18+ 
- npm 9+
- Git
- PostgreSQL 14+ (para desarrollo backend)

### Setup Local Development
```bash
# 1. Fork y clona el repositorio
git clone https://github.com/tu-usuario/eidolon.git
cd eidolon

# 2. Instala dependencias
npm install

# 3. Configura variables de entorno
cp .env.example .env.local
# Edita .env.local con tus configuraciones

# 4. Ejecuta en modo desarrollo
npm run dev
```

## 📋 How to Contribute

### 🐛 Reporting Bugs
1. Busca en [Issues existentes](https://github.com/tu-usuario/eidolon/issues) para evitar duplicados
2. Usa el template de [Bug Report](.github/ISSUE_TEMPLATE/bug_report.md)
3. Incluye toda la información solicitada
4. Proporciona pasos claros para reproducir el problema

### ✨ Suggesting Features
1. Revisa [Issues existentes](https://github.com/tu-usuario/eidolon/issues) y el [Roadmap](README.md#roadmap)
2. Usa el template de [Feature Request](.github/ISSUE_TEMPLATE/feature_request.md)
3. Explica el problema que resuelve tu propuesta
4. Incluye mockups o ejemplos si aplica

### 🔧 Code Contributions

#### Workflow para Pull Requests
1. **Fork** el repositorio
2. **Crea** una rama desde `develop`:
   ```bash
   git checkout develop
   git pull origin develop
   git checkout -b feature/nombre-descriptivo
   ```
3. **Realiza** tus cambios siguiendo los estándares de código
4. **Ejecuta** tests y linting:
   ```bash
   npm run test
   npm run lint
   npm run format
   ```
5. **Commit** con mensajes descriptivos:
   ```bash
   git commit -m "feat: add user authentication with Clerk"
   ```
6. **Push** y crea Pull Request usando nuestro [template](.github/pull_request_template.md)

#### Commit Message Standards
Seguimos [Conventional Commits](https://www.conventionalcommits.org/):

```
type(scope): description

feat: nueva funcionalidad
fix: corrección de bug
docs: cambios en documentación
style: formateo, espacios (no cambios de lógica)
refactor: refactoring de código
test: agregar o modificar tests
chore: tareas de mantenimiento
```

**Ejemplos:**
- `feat(auth): implement Clerk authentication`
- `fix(ui): resolve modal close button issue`
- `docs(api): update API documentation`

### 🏗️ Project Structure

```
EIDOLON/
├── apps/
│   ├── frontend/          # Next.js + React + TypeScript
│   │   ├── components/    # Componentes reutilizables
│   │   ├── app/          # App Router pages
│   │   ├── lib/          # Utilidades y configuración
│   │   └── styles/       # CSS y Tailwind
│   └── backend/          # NestJS + TypeScript
│       ├── src/
│       │   ├── modules/   # Módulos de negocio
│       │   ├── shared/    # Código compartido
│       │   └── config/    # Configuración
│       └── test/         # Tests del backend
├── packages/             # Código compartido entre apps
├── docs/                 # Documentación técnica
└── tools/               # Scripts y herramientas
```

## 🧪 Testing Guidelines

### Frontend Testing
```bash
# Unit tests
npm run test:frontend

# E2E tests  
npm run test:e2e

# Coverage report
npm run test:coverage
```

### Backend Testing
```bash
# Unit tests
npm run test:backend

# Integration tests
npm run test:integration
```

**Requirements:**
- Mantén coverage > 80%
- Incluye tests para funcionalidades nuevas
- Tests deben ser determinísticos y rápidos

## 📝 Code Standards

### TypeScript
- Usa **strict mode** habilitado
- Define tipos explícitos para APIs públicas
- Evita `any` - usa `unknown` cuando sea necesario
- Usa **interfaces** para objetos, **types** para uniones

### React/Next.js
- Componentes funcionales con **hooks**
- **Server Components** por defecto, **Client Components** cuando sea necesario
- Props con **TypeScript interfaces**
- Use **CSS Modules** o **Tailwind** para estilos

### NestJS
- Usa **decoradores** apropiados
- **DTOs** para validación de entrada
- **Guards** para autenticación/autorización
- **Interceptors** para logging y transformación

### General
- **Nombres descriptivos** para variables y funciones
- **Funciones pequeñas** con responsabilidad única
- **Comentarios** para lógica compleja
- **Error handling** robusto

## 🔒 Security Guidelines

- Nunca commits credenciales o secrets
- Valida toda entrada de usuario
- Usa HTTPS en producción
- Implementa rate limiting en APIs
- Sanitiza datos antes de guardar en DB

## 📚 Documentation

- Documenta APIs públicas con **JSDoc**
- Actualiza README si cambias funcionalidad principal
- Incluye ejemplos en documentación
- Mantén changelog actualizado

## 🏷️ Labeling System

**Types:**
- `bug` - Error confirmed
- `enhancement` - Nueva funcionalidad
- `documentation` - Mejoras en docs
- `help-wanted` - Necesita ayuda de comunidad
- `good-first-issue` - Bueno para principiantes

**Priority:**
- `priority-high` - Crítico
- `priority-medium` - Importante
- `priority-low` - Nice to have

**Areas:**
- `frontend` - React/Next.js
- `backend` - NestJS/API
- `database` - Schema/migrations
- `ai` - IA services
- `ui/ux` - Interfaz de usuario

## 🎯 Development Workflow

### Branches
- `main` - Código en producción
- `develop` - Rama de desarrollo principal
- `feature/*` - Nuevas funcionalidades
- `fix/*` - Correcciones de bugs
- `hotfix/*` - Fixes críticos para producción

### Release Process
1. Feature freeze en `develop`
2. Testing exhaustivo
3. Merge a `main`
4. Tag con versión semántica
5. Deploy automático via CI/CD

## 💬 Communication

- **GitHub Issues** - Bugs y features
- **Discussions** - Preguntas y propuestas
- **Pull Requests** - Code review y colaboración

## 🙏 Recognition

Todos los contributors serán reconocidos en:
- [Contributors](CONTRIBUTORS.md)
- Release notes
- README highlights

---

## 📞 Need Help?

- 📖 Lee la [documentación](docs/)
- 🔍 Busca en [Issues existentes](https://github.com/tu-usuario/eidolon/issues)
- 💬 Inicia una [Discussion](https://github.com/tu-usuario/eidolon/discussions)
- 📧 Contacta maintainers via GitHub

¡Gracias por hacer EIDOLON mejor! 🚀✨
