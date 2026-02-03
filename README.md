# React + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react) uses [Babel](https://babeljs.io/) (or [oxc](https://oxc.rs) when used in [rolldown-vite](https://vite.dev/guide/rolldown)) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh

## React Compiler

The React Compiler is not enabled on this template because of its impact on dev & build performances. To add it, see [this documentation](https://react.dev/learn/react-compiler/installation).

## Expanding the ESLint configuration

If you are developing a production application, we recommend using TypeScript with type-aware lint rules enabled. Check out the [TS template](https://github.com/vitejs/vite/tree/main/packages/create-vite/template-react-ts) for information on how to integrate TypeScript and [`typescript-eslint`](https://typescript-eslint.io) in your project.

## 🛒 Real-World eCommerce React Project Folder Structure

ecommerce-app/
│
├── public/
│   ├── index.html
│   ├── favicon.ico
│   ├── robots.txt
│   └── images/
│       └── og-product.png
│
├── src/
│   ├── app/                       # App bootstrap & providers
│   │   ├── App.jsx
│   │   ├── routes.jsx
│   │   ├── providers.jsx
│   │   └── ErrorBoundary.jsx
│   │
│   ├── assets/                    # Static assets
│   │   ├── images/
│   │   │   ├── logo.png
│   │   │   ├── placeholder.png
│   │   │   └── banners/
│   │   │       └── sale-banner.jpg
│   │   │
│   │   ├── icons/
│   │   │   ├── cart.svg
│   │   │   ├── heart.svg
│   │   │   └── search.svg
│   │   │
│   │   └── fonts/
│   │       ├── Inter-Regular.woff2
│   │       └── Inter-Bold.woff2
│   │
│   ├── components/                # Reusable UI components
│   │   ├── Button/
│   │   ├── Modal/
│   │   ├── Loader/
│   │   ├── ProductCard/
│   │   └── Price/
│   │
│   ├── layouts/                   # App layouts
│   │   ├── MainLayout.jsx
│   │   ├── AuthLayout.jsx
│   │   └── AdminLayout.jsx
│   │
│   ├── features/                  # Feature-based modules ⭐
│   │   ├── auth/
│   │   │   ├── pages/
│   │   │   │   ├── Login.jsx
│   │   │   │   └── Register.jsx
│   │   │   ├── components/
│   │   │   │   └── LoginForm.jsx
│   │   │   ├── hooks/
│   │   │   │   └── useAuth.js
│   │   │   ├── auth.api.js
│   │   │   └── authSlice.js
│   │   │
│   │   ├── products/
│   │   │   ├── pages/
│   │   │   │   ├── ProductList.jsx
│   │   │   │   └── ProductDetails.jsx
│   │   │   ├── components/
│   │   │   │   ├── ProductGrid.jsx
│   │   │   │   └── ProductFilter.jsx
│   │   │   ├── hooks/
│   │   │   │   └── useProducts.js
│   │   │   ├── products.api.js
│   │   │   └── productsSlice.js
│   │   │
│   │   ├── cart/
│   │   │   ├── components/
│   │   │   │   └── CartItem.jsx
│   │   │   ├── hooks/
│   │   │   │   └── useCart.js
│   │   │   └── cartSlice.js
│   │   │
│   │   ├── checkout/
│   │   │   ├── pages/
│   │   │   │   └── Checkout.jsx
│   │   │   ├── hooks/
│   │   │   │   └── useCheckout.js
│   │   │   └── checkout.api.js
│   │   │
│   │   └── orders/
│   │       ├── pages/
│   │       │   └── Orders.jsx
│   │       └── orders.api.js
│   │
│   ├── hooks/                     # Global reusable hooks
│   │   ├── useDebounce.js
│   │   ├── useLocalStorage.js
│   │   └── useWindowSize.js
│   │
│   ├── services/                  # API & integrations
│   │   ├── apiClient.js
│   │   ├── paymentService.js
│   │   └── analyticsService.js
│   │
│   ├── store/                     # Global state
│   │   ├── index.js
│   │   └── rootReducer.js
│   │
│   ├── utils/                     # Helpers
│   │   ├── formatCurrency.js
│   │   ├── calculateDiscount.js
│   │   └── constants.js
│   │
│   ├── styles/                    # Global styles
│   │   ├── globals.css
│   │   ├── variables.css
│   │   └── fonts.css
│   │
│   ├── main.jsx
│   └── index.css
│
├── .env
├── .env.production
├── package.json
└── vite.config.js




## 📁 Folder Structure & Naming Conventions

### public/
**Purpose**
- Static files served directly by the browser.

**Naming**
- Use **kebab-case** for files and folders.
- Keep names short and descriptive.

**Examples**
- `favicon.ico`
- `robots.txt`
- `og-product.png`

---

### src/
Main application source code.

---

### src/app/
**Purpose**
- Application bootstrap and configuration layer.

**Naming**
- Files use **PascalCase** for React components.
- Config files use **camelCase**.

**Examples**
- `App.jsx`
- `routes.jsx`
- `providers.jsx`
- `ErrorBoundary.jsx`

---

### src/assets/
**Purpose**
- Centralized static assets used inside the app.

**Naming**
- Folders use **plural nouns**.
- Files use **kebab-case**.

**Examples**
- `images/logo.png`
- `icons/cart.svg`
- `fonts/inter-regular.woff2`

---

### src/components/
**Purpose**
- Reusable, presentational UI components.
- No business logic or API calls.

**Naming**
- Folder: **PascalCase**
- Component file: **Same as folder name**
- Optional `index.js` for exports

**Examples**
- `Button/Button.jsx`
- `Modal/Modal.jsx`
- `ProductCard/ProductCard.jsx`

---

### src/layouts/
**Purpose**
- Layout wrappers defining page structure.

**Naming**
- Use **PascalCase** with `Layout` suffix.

**Examples**
- `MainLayout.jsx`
- `AuthLayout.jsx`
- `AdminLayout.jsx`

---

### src/features/
**Purpose**
- Feature-based (domain-driven) modules.

**Naming**
- Feature folders use **camelCase** or **kebab-case** (be consistent).
- Files follow responsibility-based naming.

**Examples**
- `auth/`
- `products/`
- `cart/`
- `checkout/`
- `orders/`

---

### src/features/[feature]/pages/
**Purpose**
- Route-level pages for a specific feature.

**Naming**
- Use **PascalCase**.
- Page names reflect the route.

**Examples**
- `Login.jsx`
- `ProductList.jsx`
- `ProductDetails.jsx`

---

### src/features/[feature]/components/
**Purpose**
- Feature-specific UI components.

**Naming**
- Same rules as global components.

**Examples**
- `LoginForm.jsx`
- `ProductGrid.jsx`
- `CartItem.jsx`

---

### src/features/[feature]/hooks/
**Purpose**
- Feature-specific custom hooks.

**Naming**
- Must start with `use`.
- Use **camelCase**.

**Examples**
- `useAuth.js`
- `useProducts.js`
- `useCheckout.js`

---

### src/hooks/
**Purpose**
- Global reusable custom hooks.

**Naming**
- Must start with `use`.
- Use **camelCase**.

**Examples**
- `useDebounce.js`
- `useLocalStorage.js`
- `useWindowSize.js`

---

### src/services/
**Purpose**
- API clients and third-party integrations.

**Naming**
- Use **camelCase**.
- Use clear service suffixes.

**Examples**
- `apiClient.js`
- `paymentService.js`
- `analyticsService.js`

---

### src/store/
**Purpose**
- Global state management.

**Naming**
- Use **camelCase** for files.
- Redux slices use `[feature]Slice.js`.

**Examples**
- `authSlice.js`
- `productsSlice.js`
- `rootReducer.js`

---

### src/utils/
**Purpose**
- Utility and helper functions.

**Naming**
- Use **camelCase**.
- Function names should describe behavior.

**Examples**
- `formatCurrency.js`
- `calculateDiscount.js`
- `constants.js`

---

### src/styles/
**Purpose**
- Global styles and design tokens.

**Naming**
- Use **kebab-case** for CSS files.

**Examples**
- `globals.css`
- `variables.css`
- `fonts.css`

---

### Root Files
**Naming**
- Environment files use `.env` pattern.
- Config files follow tool naming.

**Examples**
- `.env`
- `.env.production`
- `vite.config.js`
- `package.json`

