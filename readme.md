1- Instalar eslint

  yarn add eslint -D

2- Inicializar eslint 

  yarn eslint --init

3- Instalar plugins
  yarn add babel-eslint eslint-config-prettier eslint-plugin-react-hooks prettier eslint-plugin-prettier -D

3-Copiar os arquivos .eslintrc .prettierrc

4- Inslar libs para utilizar caminho absoluto nos imports '~/'

  yarn add customize-cra react-app-rewired babel-plugin-root-import eslint-import-resolver-babel-plugin-root-import -D

  4.1- copiar a configuração para o projeto
    config-overrides.js
  4.2- Modificar os scripts package.json
    "start": "react-scripts start" -> "start": "react-app-rewired start",
    "build": "react-scripts build" -> "build": "react-app-rewired build",
    "test": "react-scripts test" -> "test": "react-app-rewired test",
    
  4.3- Para fazer que o vscode consiga encontrar os arquivos utilizando CTRL + CLICK copiar este arquivo para a raiz do projeto.
    jsconfig.json