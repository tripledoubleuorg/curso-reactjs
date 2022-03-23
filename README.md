# ReactJS

## O que é o ReactJS?

React é um biblioteca javascript utilizada para a construção de interfaces. [[https://reactjs.org/](https://reactjs.org/)]

## Pré-requisitos do ReactJS

- Conhecimentos de HTML e CSS;
- Conhecimentos de Javascript + ES6;
- Compreender o DOM;
- Ter o Node e NPM instalados globalmente.

## Começar um projecto React

**Terminal**

```
npx create-react-app@latest primeira-app
cd primeira-app
npm start
```

Após da instalação devemos limpar a nossa aplicação.

## Conceitos do React

### Componentes

Componentes são funções que retornam o HTML, CSS e Javascript que determina como um elemento aparece no ecrã.

**Componente.jsx**

```jsx
import React from 'react';

export function Componente() {
   return <h1>O meu primeiro componente</h1>
}
```

**index.jsx**

```jsx
import React from 'react';
import ReactDOM from 'react-dom';
import {Componente} from './components/MeuComponente'

const elementoID = document.getElementById('root');
ReactDOM.render( <Componente />, elementoID);   
```

### JSX

A maioria dos componetes em React são escritos em JSX, uma extensão da sintaxe do Javascript que apesar de parecer HTML é Javascript com XML.

### Propriedades

Semelhantes aos atributos do HTML, as propriedades servem para personalizar os elementos. 
O termo props é uma convenção, mas pode-se utilizar qualquer outra palavra.

**Componente.js**

```jsx
import React from 'react';

export function Componente(props) {
   return <h1>O meu nome é {props.nome}</h1>
}
```

**index.jsx**

```jsx
import React from 'react';
import ReactDOM from 'react-dom';
import {Componente} from './components/MeuComponente'

const elementoID = document.getElementById('root');
ReactDOM.render( <Componente nome="João" />, elementoID);   
```

### Estados

Os elementos do React, uma vez renderizados, são imutáveis. Para alterar um elemento é preciso alterar o seu estado. Recente foi introduzido os *hooks* que facilitam muito este processo.

**Contador.jsx** 

```jsx
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

