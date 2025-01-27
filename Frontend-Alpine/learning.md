install alpine

## install a server to bunder all the files and run

install vite
npm install vite --save-dev

## configure vite

create viteconfig.js

```js
import { defineConfig } from "vite";

export default defineConfig({
  server: {
    open: true, // Automatically open the browser
  },
});
```

## create index.js

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Alpine.js App</title>
  </head>
  <body>
    <div x-data="{ count: 0 }">
      <button @click="count++">Increment</button>
      <p>Count: <span x-text="count"></span></p>
    </div>

    <script type="module" src="/src/main.js"></script>
  </body>
</html>
```

## Create src and main.js

- create src folder and inside that create main.js

```
import Alpine from 'alpinejs';

window.Alpine = Alpine;

Alpine.start();

```
