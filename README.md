# CSW Shared Components

Componentes compartidos para las aplicaciones de CSW Ingeniería Civil.

## 🚀 Características

- **Header**: Navegación principal con logo y enlaces
- **Footer**: Pie de página con información de contacto y redes sociales
- **MobileMenu**: Menú de navegación móvil
- **LegalModal**: Modal para avisos legales
- **useModal**: Hook para manejo de modales
- **Constantes**: Configuración centralizada para todas las apps

## 📦 Instalación

### Como Git Submodule

```bash
# En cada aplicación
git submodule add https://github.com/Gauss137/csw-shared-components.git shared
```

### Como dependencia local

```bash
npm install ../csw-shared-components
```

## 🔧 Uso

### Importación de componentes

```tsx
import { Header, Footer } from 'csw-shared-components';

export default function Layout({ children }) {
  return (
    <div>
      <Header />
      <main>{children}</main>
      <Footer />
    </div>
  );
}
```

### Importación de constantes

```tsx
import { APP_CONFIG, EXTERNAL_LINKS } from 'csw-shared-components';

console.log(APP_CONFIG.company); // "CSW Ingeniería Civil"
```

### Importación de hooks

```tsx
import { useModal } from 'csw-shared-components';

function MyComponent() {
  const { isOpen, openModal, closeModal } = useModal();
  
  return (
    <button onClick={openModal}>Abrir Modal</button>
  );
}
```

## 🔄 Actualización

### Actualizar submodule en todas las apps

```bash
# En cada aplicación
git submodule update --remote
git add shared
git commit -m "Update shared components"
git push
```

## 🏗️ Estructura

```
src/
├── components/
│   ├── Header.tsx
│   ├── Footer.tsx
│   ├── MobileMenu.tsx
│   └── LegalModal.tsx
├── hooks/
│   └── useModal.ts
├── constants/
│   └── index.ts
├── types/
│   └── index.ts
└── index.ts
```

## 📝 Desarrollo

### Construir

```bash
npm run build
```

### Desarrollo con watch

```bash
npm run dev
```

## 🤝 Contribución

1. Hacer cambios en el repositorio compartido
2. Commit y push
3. Actualizar submodules en todas las apps
4. Deploy

## 📄 Licencia

MIT - CSW Ingeniería Civil
