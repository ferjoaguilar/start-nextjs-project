 <p align="center">
    <img alt="Curso de Next.js" src="https://static.platzi.com/media/achievements/badge-nextjs-2259fc68-f86b-486e-bc09-95311a887985.png" width="60" />
 </p>
 <h1 align="center">
    Start NextJS + TypeScript Manual setup
 </h1>
 <p align="center">
    This guide is created by Fernando Jose Aguilar Rivas
 </p>
 
Technical guide about setup manual nextJS using typescript preset. This guide include depencies, files configuration and enviroment variables, basic backend server and testing enviroment.

## Installation

**Step one**: Start node JS project using command:

`npm init`

**Step two**: Install NextJS dependencies and Dev dependencies:

`npm install next react react-dom`

`npm install typescript @types/react @types/node -D`

**Step three**: Add `package.json` script settings:

```json
"scripts": {
  "dev": "next dev",
  "build": "next build",
  "start": "next start",
  "lint": "next lint"
}
```
**Step four**: Add `tsconfig.json` settings:
```json
{
  "compilerOptions": {
    "target": "es5",
    "lib": ["dom", "dom.iterable", "esnext"],
    "allowJs": true,
    "skipLibCheck": true,
    "strict": false,
    "forceConsistentCasingInFileNames": true,
    "noEmit": true,
    "esModuleInterop": true,
    "module": "esnext",
    "moduleResolution": "node",
    "resolveJsonModule": true,
    "isolatedModules": true,
    "jsx": "preserve"
  },
  "include": ["next-env.d.ts", "**/*.ts", "**/*.tsx"],
  "exclude": ["node_modules"]
}
```
**Step five**: Create `src/pages` folder and add `_app.tsx` and `index.tsx`

_app.tsx

```javascript
import type { AppProps } from 'next/app'

export default function MyApp({ Component, pageProps }: AppProps) {
  return <Component {...pageProps} />
}
```

index.tsx

```javascript
function HomePage() {
  return <div>Welcome to Next.js!</div>
}

export default HomePage
```

<p align="center">
    <img alt="Created by Fernando Aguilar" src="https://res.cloudinary.com/dohkdu219/image/upload/v1642443309/portfolio/signature_oq60qf.png" width="80%" />
</p>
