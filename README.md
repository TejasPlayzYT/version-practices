# WinDiscordUI

[![Showcase](https://img.youtube.com/vi/TTLLMlUsw3U/0.jpg)](https://www.youtube.com/watch?v=TTLLMlUsw3U)

A Vue.js library for creating Discord interfaces that emulate the look and feel of various Windows versions. Perfect for creating nostalgic and engaging user experiences in Discord bot interfaces or standalone apps.  

## Features  
- **Windows Version Themes**: Emulate Windows 95, XP, Vista, and beyond.  
- **Vue.js Integration**: Easily integrate with any Vue.js project.  
- **Customizable Components**: Buttons, dialogs, and icons styled to match each Windows version.  
- **Responsive Design**: Fully functional on both desktop and mobile browsers.  
- **Discord Webhooks**: Seamlessly integrates with Discord webhooks and bots.  

## Installation  

Install the library via npm:  
```bash  
npm install discord-windows-emulator  
```  

## Usage  

Import and use the library in your Vue.js project:  

```javascript  
import { createApp } from 'vue';  
import App from './App.vue';  
import WindowsEmulator from 'discord-windows-emulator';  
import 'discord-windows-emulator/dist/style.css';  

const app = createApp(App);  
app.use(WindowsEmulator);  
app.mount('#app');  
```  

### Example  

Here’s how you can create a Windows 95-styled dialog in your app:  

```html  
<template>  
  <Windows95Dialog title="Welcome to Windows 95 Emulator">  
    <p>This is a sample Discord message styled like Windows 95!</p>  
    <Windows95Button @click="sendMessage">Send to Discord</Windows95Button>  
  </Windows95Dialog>  
</template>  

<script>  
export default {  
  methods: {  
    sendMessage() {  
      // Logic to send a message via Discord webhook  
    },  
  },  
};  
</script>  
```  

## Customization  

You can customize themes and components through a simple configuration file:  

```javascript  
WindowsEmulator.configure({  
  defaultTheme: 'WindowsXP',  
  customStyles: {  
    buttonColor: '#000080',  
  },  
});  
```  

## Useful Contributions  

Looking for ways to contribute? Here are some ideas to get started:  

1. **New Windows Versions**: Add support for more Windows themes, like Windows 11 or even custom futuristic themes.  
2. **Advanced Customization**: Implement options for dynamic styling and theming beyond the default configurations.  
3. **Enhanced Accessibility**: Ensure components are accessible with ARIA attributes and keyboard navigation.  
4. **Performance Optimization**: Analyze and improve the library’s performance, especially for large-scale projects.  
5. **Documentation**: Create detailed guides, tutorials, and example projects to help others use the library.  
6. **Integration Examples**: Provide integration demos with Discord bots and webhook services.  
7. **Bug Fixes**: Identify and resolve any existing issues in the codebase.  

Contributions don’t have to be code! Feedback, design ideas, or suggestions for new features are equally valuable.  

## Contributing  

We welcome contributions! Feel free to fork the repository, create new features, or fix bugs. Submit a pull request, and we’ll review it as soon as possible.  

## License  

This library is open-source and licensed under the MIT License.  

--- 
