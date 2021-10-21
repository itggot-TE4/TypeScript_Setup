# Kom igång med TypeScript

## 1. Installation

### 1.1 Installera Node

`brew install node`

Testa med `node -v`

### 1.2 Installera TypeScript

`npm install -g typescript`

Testa med `tsc -v`

### 1.3.1 Installera Yarn

Yarn behövs för bl.a. exercism

`brew install yarn`

testa med `yarn -v`

### 1.3.2 Lägg till TypeScript-stöd i yarn

`yarn global add typescript`

## 2. Konfiguration

### 2.1 Mappstruktur

Skapa en mapp för projektet med följande mappstruktur (obs ej för Exercism)

````
src/ts
app/js
````

### 2.2 tsconfig.json

`tsc --init` (obs Exercism ger er en färdig `tsconfig.json`)

I tsconfig.json gör följande ändringar på lämpliga rader:
(låt bli de första 5 raderna för Exercism, men `Strict Type Checking Options` och `Additional Checks` borde vara ok att koppla på i Exercisms `tsconfig.json`

````json
"target": "es2021",
"module": "es2021",
"sourceMap": true,
"outDir": "./app/",
"removeComments": true, 


 /* Strict Type-Checking Options */
 "strict": true,                                    
 "noImplicitAny": true,                          
"strictNullChecks": true,                       
"strictFunctionTypes": true,                    
"strictBindCallApply": true,                    
"strictPropertyInitialization": true,           
"noImplicitThis": true,                         
"useUnknownInCatchVariables": true,             
"alwaysStrict": true,                           
"noUnusedLocals": true,     
````

## 2. Kompilering och körning

(Med inställningar enligt ovanstående `tsconfig.json`

`tsc` (Kompilera)

`node app/js/filens_namn.js` (Kör)

