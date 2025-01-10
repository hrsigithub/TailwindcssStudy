Tailwindcss

https://tailwindcss.com/


% node -v
v23.5.0

% npm init -y
———
npm install -D tailwindcss
npx tailwindcss init

—-
Vscodeの設定ファイルに以下、追加。

"css.lint.unknownAtRules": "ignore"
—
ビルド

npx tailwindcss -i ./src/input.css -o ./src/output.css --watch

—
pakeage.json

"scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "build": "npx tailwindcss -i ./src/input.css -o ./src/output.css --watch"
  },
—
拡張機能

Tailwind CSS IntelliSense

—
背景色設定

tailwind.config.js

theme: {
    extend: {},
    backgroundImage: {
      "tutorial-bg": "url('../src/img/main-bg.jpg')",       or "tutorial-bg": "url('./img/main-bg.jpg')",

    },
  },

クラス名は、
     <div
        class="bg-tutorial-bg min-h-screen bg-cover bg-center object-cover"
      ></div>
  
