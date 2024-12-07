## 1.install React template

```
/*in R:*/
yarn create vite p2.react.yarn.rest.spa --template react
cd p2.react.yarn.rest.spa
yarn add react@18.2.0 react-dom@18.2.0
yarn set version stable
yarn config set nodeLinker node-modules
yarn
yarn dev
```

## 2.assign to git
use command "…or create a new repository on the command line" from github

## 3.install other

```
yarn add react-router-dom@5.2.0
yarn add stylelint
```
## 4. no install

                            /*

                            yarn add materialize-css@next
                            yarn add json-server
                            yarn add concurrently --dev

                            */

## 5.clear the template

/*
Remove-Item -Recurse -Force .yarn, .pnp.* , node_modules

Remove-Item — команда для удаления файлов и папок.
-Recurse — рекурсивное удаление всех вложенных файлов и папок.
-Force — принудительное удаление, даже если файлы скрыты или защищены.
*/

 Remove-Item -Recurse -Force ./public/*
 Remove-Item -Recurse -Force ./src/assets/*

 echo "" > .\src\App.css
 echo "" > .\src\index.css
 echo "" > .\src\App.jsx  
 echo "" > flow.md

New-Item -ItemType Directory -Name "./src/assets/image"
New-Item -ItemType Directory -Name "./src/component"        
New-Item -ItemType Directory -Name "./src/component/utils"                                             
New-Item -ItemType Directory -Name "./src/layout"
New-Item -ItemType Directory -Name "./src/pages" 
New-Item -ItemType Directory -Name "./src/services"
echo "" > .\src\services\api.js
echo "" > config.js      

Set-Content -Path .\src\App.jsx -Value @"
function App() {
    return <div>Hi</div>;
}

export default App;
"@ -Encoding UTF8

Set-Content -Path .\src\component\Preloader.jsx -Value @"
function Preloader() {
    return <div>Preloader</div>;
}

export {Preloader};
"@ -Encoding UTF8

Set-Content -Path .\src\component\Search.jsx -Value @"
function Search() {
    return <div>Search</div>;
}

export {Search};
"@ -Encoding UTF8

Set-Content -Path .\src\layout\Footer.jsx -Value @"
function Footer() {
    return <div>Footer</div>;
}

export {Footer};
"@ -Encoding UTF8

Set-Content -Path .\src\layout\Header.jsx -Value @"
function Header() {
    return <div>Header</div>;
}

export {Header};
"@ -Encoding UTF8

yarn dev


# 6. push

git add -A
git commit -m "initial"
git push