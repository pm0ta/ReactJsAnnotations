```js
import { useState } from "react";

export default function Condicional() {

  const [list, setList] = useState(false);

  function handleTask() {
    setList(prevState => !prevState);
  }

  return (
  <>
  <h1> TodoList </h1>
  <p> Estudar ReactJS </p>
  <p> {list ? 'Feito' : 'A fazer'} </p> {/* Se list for verdadeira (true), irá ser exibido 'Feito' na tela.
  Caso list for falsa (false), irá ser exibido 'A fazer' na tela.
  */}
  <button onClick={handleTask} > {/* Chamamos a função handleTask para nosso evento onClick */}
    {list ? 'Desmarcar como feito' : 'Marcar como feito'} {/* Se list for verdadeiro (true), irá aparecer 'Desmarcar como feito'
    como nome do botão. Caso for falso (false), irá aparecer 'Marcar como feito' como nome do botão */}
  </button>
  </>
  )
}

// https://www.youtube.com/watch?v=N0yd73QZ2wk - Vídeo explicativo sobre renderização condicional.  
```
