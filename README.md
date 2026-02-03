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
