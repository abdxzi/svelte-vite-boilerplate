# Svelte + Vite boiler-plate

This template should help get you started developing with Svelte in Vite and develop using the help of vscode inbuilt browser.

## Recommended IDE Setup

[VS Code](https://code.visualstudio.com/) + [Svelte](https://marketplace.visualstudio.com/items?itemName=svelte.svelte-vscode).

## Setup

Clone this repo and use ```pnpm install``` or intall using ```create-vite``` and replace files

```sh
npm install -g create-vite
create-vite my-svelte-app --template svelte
cd my-svelte-app
npm install
npm run dev
```

#### vscode inline browser
Use  ```CTRL+SHIFT+P``` and edit ```keybindings.json```

```js
// Place your key bindings in this file to override the defaults
[
  // Browser
  {
    "key": "alt+shift+b",
    "command": "workbench.action.tasks.runTask",
    "args": "Simple Browser"
  },
]
```
Ensure the port in ```.vscode/tasks.json``` is same as the vite opening port.
```
{
    "version": "2.0.0",
    "tasks": [
        {
            "label": "Simple Browser",
            "command": "${input:openSimpleBrowser}",
            "problemMatcher": []
        }
    ],
    "inputs": [
        {
            "id": "openSimpleBrowser",
            "type": "command",
            "command": "simpleBrowser.show",
            "args": [
                "http://localhost:5173"
            ]
        }
    ]
}
```

use ```alt+shift+b``` to open browser
Inline screen size is given by ```./src/utils/Screen.svelte``` component.

### vite enviromental variables
We can access the ```.env``` variables using ```import.meta.env.VITE_KEY_NAME```

> **Warning**
>
> The enviromental variables given here in ```.env``` directly exposed in js code in client app.