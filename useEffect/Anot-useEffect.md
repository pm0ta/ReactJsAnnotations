useEffect é um hook que vai ser chamado assim que a página for recarregada;
useEffect() recebe como primeiro parâmetro uma função que será executada assim que o componente renderizar. 
A beleza deste Hook é que podemos definir facilmente quando queremos que esta função seja executada novamente. Basta passar como segundo parâmetro ao useEffect() um Array com as variáveis que controlarão esse Hook.

```js
import { useState, useEffect } from 'react';

function UseEffect() {

    //useEffect é um hook que vai ser chamado assim que á página é carregada

    const [count, setCount] = useState(0);

    useEffect(() => {
        document.title = count; //quando a página for recarregada, o titulo ira ser o valor que estiver em count
    }, [count]);

    return (
        <>        
        <h1> {count} </h1>
        <button onClick={
            () => setCount(count + 1)            
        }>
            Adicionar
        </button>
        </>
    );
}

export default UseEffect;
```
