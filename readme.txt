

john@nuke /scratch/john/development/electron_app>nvm ls
->     v10.15.3
        v11.1.0
       v12.14.1
       v12.16.1
      v12.22.12
       v14.18.0
       v14.19.1
       v16.10.0
       v16.14.2
       v16.18.0
        v17.9.0
       v18.10.0
       v20.11.0
default -> v10.15.3
node -> stable (-> v20.11.0) (default)
stable -> 20.11 (-> v20.11.0) (default)
iojs -> N/A (default)
unstable -> N/A (default)
lts/* -> lts/gallium (-> v16.14.2)
lts/argon -> v4.9.1 (-> N/A)
lts/boron -> v6.17.1 (-> N/A)
lts/carbon -> v8.17.0 (-> N/A)
lts/dubnium -> v10.24.1 (-> N/A)
lts/erbium -> v12.22.12
lts/fermium -> v14.19.1
lts/gallium -> v16.14.2


john@nuke /scratch/john/development/electron_app>nvm use v20.11.0
Now using node v20.11.0 (npm v10.2.4)
john@nuke /scratch/john/development/electron_app>node --version
v20.11.0
john@nuke /scratch/john/development/electron_app>npm --version 
10.2.4
john@nuke /scratch/john/development/electron_app>npx --version
10.2.4
john@nuke /scratch/john/development/electron_app>yarn --version
zsh: command not found: yarn


john@nuke /scratch/john/development/electron_app>npx create-electron-app@latest electron_app
Need to install the following packages:
create-electron-app@7.10.2
Ok to proceed? (y) y
npm WARN skipping integrity check for git dependency ssh://git@github.com/electron/node-gyp.git 
npm WARN deprecated inflight@1.0.6: This module is not supported, and leaks memory. Do not use it. Check out lru-cache if you want a good and tested way to coalesce async requests by a key value, which is much more comprehensive and powerful.
npm WARN deprecated rimraf@3.0.2: Rimraf versions prior to v4 are no longer supported
npm WARN deprecated @npmcli/move-file@2.0.1: This functionality has been moved to @npmcli/fs
npm WARN deprecated glob@7.2.3: Glob versions prior to v9 are no longer supported
npm WARN deprecated glob@8.1.0: Glob versions prior to v9 are no longer supported
npm WARN deprecated glob@8.1.0: Glob versions prior to v9 are no longer supported
npm WARN deprecated lodash.get@4.4.2: This package is deprecated. Use the optional chaining (?.) operator instead.
npm WARN deprecated boolean@3.2.0: Package no longer supported. Contact Support at https://www.npmjs.com/support for more info.

✔ Resolving package manager: npm
✔ Resolving template: vite
  › Using @electron-forge/template-vite (local module)
✔ Initializing directory
✔ Preparing template
✔ Initializing template
✔ Installing template dependencies


john@nuke /scratch/john/development/electron_app>ls -al
totalt 20
drwxrwxr-x   3 john john  4096 okt 27 18:29 .
drwxr-xr-x 227 john john 12288 okt 27 18:26 ..
drwxrwxr-x   4 john john  4096 okt 27 18:29 electron_app
john@nuke /scratch/john/development/electron_app>ls -al electron_app 
totalt 316
drwxrwxr-x   4 john john   4096 okt 27 18:29 .
drwxrwxr-x   3 john john   4096 okt 27 18:29 ..
-rw-rw-r--   1 john john   1906 okt 27 18:29 forge.config.js
-rw-rw-r--   1 john john   1215 okt 27 18:29 .gitignore
-rw-rw-r--   1 john john    270 okt 27 18:29 index.html
drwxrwxr-x 355 john john  12288 okt 27 18:30 node_modules
-rw-rw-r--   1 john john   1063 okt 27 18:30 package.json
-rw-rw-r--   1 john john 268848 okt 27 18:30 package-lock.json
drwxrwxr-x   2 john john   4096 okt 27 18:29 src
-rw-rw-r--   1 john john    100 okt 27 18:29 vite.main.config.mjs
-rw-rw-r--   1 john john    100 okt 27 18:29 vite.preload.config.mjs
-rw-rw-r--   1 john john    100 okt 27 18:29 vite.renderer.config.mjs


john@nuke /scratch/john/development/electron_app/electron_app>npm start

> electron_app@1.0.0 start
> electron-forge start

✔ Checking your system
✔ Locating application
✔ Loading configuration
✔ Preparing native dependencies [0.4s]
✔ Running generateAssets hook
✔ Running preStart hook
  ✔ [plugin-vite] Preparing Vite bundles
    ✔ Launched Vite dev servers for renderer process code [0.2s]
      ✔ Target main_window
        › ➜  Local:   http://localhost:5173/
          ➜  Network: use --host to expose
    ✔ Built main process and preload bundles [0.4s]
      ✔ Building src/main.js target
      ✔ Building src/preload.js target
✔ Launched Electron app. Type rs in terminal to restart main process.

Generated an empty chunk: "preload".
18:37:33 [@electron-forge/plugin-vite] target built src/preload.js
18:37:33 [@electron-forge/plugin-vite] target built src/main.js

[1315937:1027/183733.599049:FATAL:sandbox/linux/suid/client/setuid_sandbox_host.cc:166] The SUID sandbox helper binary was found, but is not configured correctly. Rather than run without sandboxing I'm aborting now. You need to make sure that /media/data/scratch/john/development/electron_app/electron_app/node_modules/electron/dist/chrome-sandbox is owned by root and has mode 4755.
john@nuke /scratch/john/development/electron_app/electron_app>ls -al node_modules/electron/dist/chrome-sandbox
-rwxr-xr-x 1 john john 15328 okt 27 18:30 node_modules/electron/dist/chrome-sandbox
john@nuke /scratch/john/development/electron_app/electron_app>sudo chown root:root node_modules/electron/dist/chrome-sandbox 
john@nuke /scratch/john/development/electron_app/electron_app>sudo chmod 4755 node_modules/electron/dist/chrome-sandbox 
john@nuke /scratch/john/development/electron_app/electron_app>ls -al node_modules/electron/dist/chrome-sandbox
-rwsr-xr-x 1 root root 15328 okt 27 18:30 node_modules/electron/dist/chrome-sandbox


john@nuke /scratch/john/development/electron_app/electron_app>npm start

> electron_app@1.0.0 start
> electron-forge start

✔ Checking your system
✔ Locating application
✔ Loading configuration
✔ Preparing native dependencies [0.5s]
✔ Running generateAssets hook
✔ Running preStart hook
  ✔ [plugin-vite] Preparing Vite bundles
    ✔ Launched Vite dev servers for renderer process code [0.2s]
      ✔ Target main_window
        › ➜  Local:   http://localhost:5173/
          ➜  Network: use --host to expose
    ✔ Built main process and preload bundles [0.4s]
      ✔ Building src/main.js target
      ✔ Building src/preload.js target
✔ Launched Electron app. Type rs in terminal to restart main process.

Generated an empty chunk: "preload".
18:43:06 [@electron-forge/plugin-vite] target built src/preload.js
18:43:06 [@electron-forge/plugin-vite] target built src/main.js


