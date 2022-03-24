# Introdução do ReactJS

- O que é o React?
- Pré-requisitos do ReactJS
- Começar um projecto React
- Conceitos do React
-- Componentes
-- Propriedades
-- JSX
-- Estados

## O que é o ReactJS?

Criado pela Facebook (Meta), o React é uma biblioteca JavaScript utilizada para a construção de interfaces. [[https://reactjs.org/](https://reactjs.org/)]

## Pré-requisitos do ReactJS

- Conhecimentos de HTML e CSS;
- Conhecimentos de Javascript + ES6;
- Compreender o DOM;
- Ter o Node e NPM instalados globalmente.

## Começar um projecto React

**Terminal**

```
npx create-react-app@latest nome-app
cd nome-app
npm start
```

Após a instalação devemos limpar a nossa aplicação.

## Conceitos do React

### Componentes

Um componente é uma função em Javascript que determina como um elemento aparece no ecrã. Cada componente funciona como um bloco independente e reutilizável.

**Componente.js**

```js
export function Componente() {
   return <h1>O meu primeiro componente</h1>
}
```

**App.js**

```js

import {Componente} from './components/Componente'

function App(){
   return <Componente />
}

export default App();
```

### JSX

A maioria dos componetes em React são escritos em JSX, uma extensão da sintaxe do Javascript que apesar de parecer HTML é Javascript com XML.

### Propriedades

Semelhantes aos atributos do HTML, as propriedades servem para personalizar os elementos. 
O termo props é uma convenção, mas pode-se utilizar qualquer outra palavra.

**Componente.js**

```jsx
export function Componente(props) {
   return <h1>O meu nome é {props.nome}</h1>
}
```

**App.js**

```js

import {Componente} from './components/Componente'

function App(){
   return <Componente nome="Sara"/>
}

export default App();
```

### Estados

Os elementos do React, uma vez renderizados, são imutáveis. Para alterar um elemento é preciso alterar o seu estado de modo que este seja de nove renderizado. 
Recente foi introduzido o hook 'useState()' que facilita muito este processo.

**Contador.js** 

```js
import { useState } from 'react';

export function Contador() {
  const [count, setCount] = useState(0);

  return (
    <div>
      <p>Número de cliques: {count}</p>
      <button onClick={() => setCount(count + 1)}>
        Clicar
      </button>
    </div>
  );
```

