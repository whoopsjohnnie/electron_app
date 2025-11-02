john@nuke /scratch/john/development/electron_app5>node --version 
v20.11.0
john@nuke /scratch/john/development/electron_app5>npx create-electron-app@latest my-new-app --template=webpack

✔ Resolving package manager: npm
✔ Resolving template: webpack
  › Using @electron-forge/template-webpack (local module)
✔ Initializing directory
✔ Initializing git repository
✔ Preparing template
✔ Initializing template
✔ Installing template dependencies
john@nuke /scratch/john/development/electron_app5>cd my-new-app 
john@nuke /scratch/john/development/electron_app5/my-new-app>npm install --save-dev @babel/core @babel/preset-react babel-loader


added 34 packages, and audited 795 packages in 4s

129 packages are looking for funding
  run `npm fund` for details

7 vulnerabilities (5 low, 2 moderate)

To address all issues (including breaking changes), run:
  npm audit fix --force

Run `npm audit` for details.
john@nuke /scratch/john/development/electron_app5/my-new-app>vim webpack.rules.js
john@nuke /scratch/john/development/electron_app5/my-new-app>npm install --save react react-dom


added 3 packages, and audited 798 packages in 2s

129 packages are looking for funding
  run `npm fund` for details

7 vulnerabilities (5 low, 2 moderate)

To address all issues (including breaking changes), run:
  npm audit fix --force

Run `npm audit` for details.
john@nuke /scratch/john/development/electron_app5/my-new-app>vim src/app.jsx
john@nuke /scratch/john/development/electron_app5/my-new-app>vim src/renderer.js 
john@nuke /scratch/john/development/electron_app5/my-new-app>sudo chown root:root node_modules/electron/dist/chrome-sandbox 
john@nuke /scratch/john/development/electron_app5/my-new-app>sudo chmod 4755 node_modules/electron/dist/chrome-sandbox 
john@nuke /scratch/john/development/electron_app5/my-new-app>          

