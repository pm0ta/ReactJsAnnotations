Para renderizar uma lista vamos primeiramente precisar de um array;

Depois utilizamos a função map, para percorrer cada um dos itens;

Podendo assim renderizar algo na tela;

É possível unir operadores condicionais com a renderização de listas;


# Rend-Listas.js
```js
import OutraLista from "./OutraLista";

export default function RendLista() {

  const names = ['Pedro', 'Raphaela', 'Gabriel', 'Davi'];   //Criamos um array com vários nomes

  return (
    <>
    <OutraLista names={names} />  {/* importamos 'OutraLista.js' e passamos o array names através das props */}
    </>
  );
}
```

# OutraLista.js
```js
export default function OutraLista({ names }) {
  return (
    <>
    {
      names.map((itens, index) => ( //mapeamos o array names
        <h2 key={index}> {itens} </h2> //retornamos um h2 com os itens
      ))
    }
    </>
  );
}
```


> Para que serve o map ?
> O JavaScript map faz parte do conjunto de métodos disponíveis na linguagem para a manipulação de objetos do tipo array. Ele funciona como uma estrutura de repetição, pois percorre todos os elementos do array, executa determinada ação e retorna um novo conteúdo.
