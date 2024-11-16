
---

## File Tree  

```
discord-windows-emulator-example/
├── public/
│   ├── index.html
├── src/
│   ├── components/
│   │   └── WelcomeDialog.vue
│   ├── App.vue
│   ├── main.js
├── package.json
└── README.md
```

---

### File Contents  

#### `public/index.html`  

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Discord Windows Emulator Example</title>
</head>
<body>
  <div id="app"></div>
</body>
</html>
```

#### `src/App.vue`  

```html
<template>
  <div>
    <h1>Discord Windows Emulator</h1>
    <WelcomeDialog />
  </div>
</template>

<script>
import WelcomeDialog from './components/WelcomeDialog.vue';

export default {
  components: {
    WelcomeDialog,
  },
};
</script>
```

#### `src/components/WelcomeDialog.vue`  

```html
<template>
  <Windows95Dialog title="Welcome to Windows 95 Emulator">
    <p>This is a sample Discord message styled like Windows 95!</p>
    <Windows95Button @click="sendToDiscord">Send to Discord</Windows95Button>
  </Windows95Dialog>
</template>

<script>
export default {
  methods: {
    sendToDiscord() {
      alert('This would send a message to Discord via a webhook.');
    },
  },
};
</script>
```

#### `src/main.js`  

```javascript
import { createApp } from 'vue';
import App from './App.vue';
import WindowsEmulator from 'discord-windows-emulator';
import 'discord-windows-emulator/dist/style.css';

const app = createApp(App);

app.use(WindowsEmulator);

app.mount('#app');
```

#### `package.json`  

```json
{
  "name": "discord-windows-emulator-example",
  "version": "1.0.0",
  "private": true,
  "scripts": {
    "serve": "vue-cli-service serve",
    "build": "vue-cli-service build"
  },
  "dependencies": {
    "discord-windows-emulator": "^1.0.0",
    "vue": "^3.0.0"
  },
  "devDependencies": {
    "@vue/cli-service": "^5.0.0"
  }
}
```

---

### Instructions  

1. **Install dependencies**:  
   Run the following commands in the project directory:  
   ```bash
   npm install
   ```

2. **Serve the application**:  
   Start the development server:  
   ```bash
   npm run serve
   ```

3. **View the app**:  
   Open your browser and navigate to the provided localhost URL (usually `http://localhost:8080`).  

---

Let me know if you want any additional features for this example!
