 <p align="center">
    <img alt="Curso de Next.js" src="https://static.platzi.com/media/achievements/badge-nextjs-2259fc68-f86b-486e-bc09-95311a887985.png" width="60" />
 </p>
 <h1 align="center">
    Start NextJS + TypeScript
 </h1>
 <p align="center">
    This guide is created by Fernando Jose Aguilar Rivas
 </p>
 
 This is a technical guide to create nextjs project without nextjs CLI. All the procedure is manual using this form we have more adventages like:

-  Performance
-  Less dependecies
-  Scalability

## Installation guide

*  **Step 1**
Create project folder and excute on terminal.
	> npm init

* **Step 2**
Install dependencies.

	> npm install react react-dom next

* **Step 3**
Create **page** directory and index.jsx file.
	> mkdir page

* **Step 4**
Add the scripts in **package.json**
```json
"scripts": {
    "dev": "next", //Start dev server
    "build": "next build", // Compile project
    "start": "next start" //Start production server
  }
```
#### If you need work [NextJS using Typescript](https://nextjs.org/docs/basic-features/typescript).

* **Step 1**
Create **tsconfig.json** file and include this [configuration.](https://github.com/vercel/next.js/blob/canary/examples/with-typescript/tsconfig.json "configuration")

	> touch tsconfig.json

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

*  **Step 2**
Install dev dependencies.
	> npm install typescript @types/react @types/node -D

**Important:**
Rename .jsx files to .tsx and use the same package.json script options. NextJS know transpile TypeScript project.

Happy hacking!!!
