# Animations
Something that isn't always necessary but can be useful depending on the project's needs. 
This will be a living document of all the different types of animation systems I've found and how to configure them.

## TailwindCSS-Animated 

[Documentation](https://www.tailwindcss-animated.com/)


TailwindCSS comes with a few animations built in, but they are pretty simple. This is my favorite package for extending those animations, it's simple and lightweight.
It also comes with a fun to use [editor](https://www.tailwindcss-animated.com/configurator.html)

### Install
```
npm i tailwindcss-animated
```
### Setup
1. Add the plugin to the tailwind.config.ts file.
```typescript
module.exports ={
    // …
    plugins:[
        require(‘tailwindcss-animated’)
    ],
   }
```
2. Configure for use with typescript. In the `/node_modules/tailwindcss-animated/` folder add new file `index.d.ts`
```typescript
    // node_modules/tailwindcss-animated/index.d.ts
    declare const plugin: { handler:()=> void }
    export = plugin
```
### How to Use

- Go to https://www.tailwindcss-animated.com/configurator.html
- Design the animation you want to make using their editor
- When finished click **Copy animation classes** in the bottom right.
- Paste the TailwindCSS classes in the desired component className.
- Enjoy!

