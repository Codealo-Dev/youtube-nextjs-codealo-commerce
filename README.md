# Codealo Commerce con NextJs

Este repositorio existe a la par del curso de ReactJs con NextJs de Codealo.

Aquí puedes encontrar la lista de contenido y los videos publicados.

### Videos

### Setup

Aquí dejamos las instrucciones para crear configurar la aplicación desde 0 utilizando tus conocimientos de la consola.

1. Crear proyecto de NextJs con TypeScript

```bash
npx create-next-app@latest --ts commerce
```

2. Copiar codigo a carpeta local y borrar carpeta de `commerce`

** Linux / macOS **

```bash
cp -a ./commerce/. ./
rm -r commerce
```

** PowerShell **

```powershell
Get-ChildItem -Path ".\commerce\*" -Recurse | Move-Item -Destination ".\"
Remove-Item ".\commerce" -Recurse
```

Se debio de haber copiado el código de la carpeta `commerce` a la principal del proyecto.

3. Agregar TailwindCss

Puedes encontrar la guía aquí: https://tailwindcss.com/docs/guides/nextjs

```bash
yarn add -D tailwindcss postcss autoprefixer
npx tailwindcss init -p
```

Editar `tailwind.config.js` a lo siguiente

```javascript
module.exports = {
  content: [
    "./pages/**/*.{js,ts,jsx,tsx}",
    "./components/**/*.{js,ts,jsx,tsx}",
  ],
  theme: {
    extend: {},
  },
  plugins: [],
}
```

Agregar las directivas a `./styles/globals.css`

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

4. Correr proyecto

```bash
yarn dev
```

Navega a http://localhost:3000

Debes de ser presentado con la aplicación base.


### Ayuda