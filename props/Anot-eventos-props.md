## Index.js

```js
import Button from './evento/Button';

export default function Evento() {

  function Actived() { //Criamos a função
    console.log("Fui ativado !");
  }

  return <Button 
    event={Actived} //demos um nome para a props (event), e nela adicionamos a função ({Actived})
    BTNname="Ativar!"
    />;
}
```

## Evento.js

```js
export default function Evento({ BTNname, event }) {
  return <button onClick={event} /* chamamos o evento (que é o onClick) e nele chamamos a props event, que está com nossa função Actived. */ >  
  {BTNname} 
  </button>
}
```
