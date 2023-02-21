Legend: ''' > don't copy: signs just show what to paste in 

----------------------------------------------------------

yarn create react-app name-app --template typescript

cd name-app
code .

--> open Terminal in VSCODE and type in 

yarn add @mui/material @emotion/react @emotion/styled

----------------------------------------------------------

--> link fonts in index.html document

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Bigelow+Rules&family=Roboto:wght@300;400;500;700&display=swap" rel="stylesheet">

----------------------------------------------------------

yarn add -D babel-plugin-import
--> create .babelrc.js in root directory

'''

const plugins = [
  [
    'babel-plugin-import',
    {
      libraryName: '@mui/material',
      libraryDirectory: '',
      camel2DashComponentName: false,
    },
    'core',
  ],
  [
    'babel-plugin-import',
    {
      libraryName: '@mui/icons-material',
      libraryDirectory: '',
      camel2DashComponentName: false,
    },
    'icons',
  ],
];

module.exports = { plugins };

''' 
- paste in .babelrc.js

----------------------------------------------------------

yarn add -D react-app-rewired customize-cra

create config-overrides.js in root directory same as .babelrc.js --> on level of package.json

'''

/* config-overrides.js */
/* eslint-disable react-hooks/rules-of-hooks */
const { useBabelRc, override } = require('customize-cra');

module.exports = override(useBabelRc())

''' 
- paste in config-overrides.js

----------------------------------------------------------

open package.json and edit it with the following  

'''

{
    "start": "react-app-rewired start",
    "build": "react-app-rewired build",
    "test": "react-app-rewired test",
    "eject": "react-scripts eject"
}

'''

----------------------------------------------------------

after that just type in your Terminal:    yarn start
