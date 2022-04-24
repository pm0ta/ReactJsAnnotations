O State Lift é uma técnica utilizada para compartilhar o state;

É normal vários componentes dependerem do mesmo estado;

Então precisamos elevar o nível do mesmo a um componente pai;

Então centralizamos o state no pai, e definimos quem usa e quem define (useState);


# Index.js ( Pai )
```js
import React, { useState } from 'react';
import SeuNome from './components/SeuNome';
import Saudacao from './components/Saudacao';

export default function App() {

  const [name, setName] = useState(); //criamos o state

  return (
    <>  {/* <<< Fragments */}
    <SeuNome setName={setName} /> {/* passamos o state para 'SeuNome' pelas props */}
    <Saudacao name={name} />
    </>
  );
}
```



# SeuNome.js ( Filho )
```js
export default function SeuNome({ setName }) {

  return (
    <>
    <p> Digite seu nome: </p>
    <input type="text" placeholder="Qual é o seu Nome ?" onChange={(e) => setName(e.target.value)} />
    </>
  );
}
```



# Saudacao.js ( Filho )
```js
export default function Saudacao({ name }) {
  return (
    <>
    <p> Olá {name}, tudo bem ? </p>
    </>
  )
}
```
