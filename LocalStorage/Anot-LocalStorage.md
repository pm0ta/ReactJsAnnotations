O localStorage mantém o dado gravado mesmo se o browser é fechado e reaberto. Isso facilita criar alguns comportamentos de interface durante o uso do usuário. E obviamente, nem preciso dizer, que não serve para gravar dados sensíveis.

Podemos criar entradas de par de chaves com o *localStorage.setItem("nome", "valor")"*

Também podemos ler as entradas com *localStorage.getItem("nome")*

Atualize uma entrada com o mesmo método setItem(), mas com uma chave já existente: *localStorage.setItem("nome", "novo valor")*

Para excluir uma entrada: *localStorage.removeItem("nome")*

E para excluir tudo: *localStorage.clear()*

```js
import { useState } from 'react';

function LocalStorage() {

  /*
    localStorage.setItem("nome", "Pedro"); criando uma chave chamada nome, e colocando o valor, que é Pedro

    localStorage.setItem("nome", "Gabriel"); irá atualizar a chave, então de "Pedro", passará a ser "Gabriel"

    localStorage.getItem("nome"); utilizamos para recuperar uma chave, no caso recuperamos a chave nome

    localStorage.removeItem(nome); remove a chave

    localStorage.clear(); limpa tudoo
  */

  const [name, setName] = useState("");
  
  function Armazenar(chave, valor) {
    localStorage.setItem(chave, valor);
  }

  function Consultar(chave) {
    alert(localStorage.getItem(chave));
  }

  function Remove(chave) {
    localStorage.removeItem(chave);
  }

  return (
    <>
    <input type="text" value={name} onChange={(e) => setName(e.target.value)} />

    <button onClick={()=>Armazenar("nome", name)}> Gravar nome </button>

    <button onClick={()=>Consultar("nome")}> Consultar nome </button>
    
    <button onClick={()=>Remove("nome")}> Remover nome </button>
    </>
  )
}

export default LocalStorage;
```

Fontes: https://tableless.com.br/guia-f%C3%A1cil-sobre-usar-localstorage-com-javascript/ - https://warcontent.com/localstorage-javascript/
VídeoAula: https://www.youtube.com/watch?v=De5np8phQxo -  https://www.youtube.com/watch?v=oaDdTH2JQrA&t=300s
