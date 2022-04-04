# Avançando em __PROPS__

> Podemos definir tipos para as props (ou seja, strings, number e por ai vai), realizando uma espécie de validação;
> Definimos em um objeto chamdo __propTypes__ no próprio componente;
> E ainda há possibilidades de __definir um valor padrão__;
> Neste caso utilizamos o objeto __defaultProps__;

# Oque é __defaultProps__ ?

> Com a uma certa semelhança do propTypes aqui definimos um comportamento default para quando uma propriedade não for informada receber algum valor em especial.


```js
import PropTypes from 'prop-types';

export default function Item({ marca, lancamento }) {
  return (
    <li> {marca} - {lancamento} </li>
  );
  
}
  Item.propTypes = {  // "PropTypes exporta uma variedade de validadores que podem ser usados para certificar que os dados que você recebe são válidos."
    marca: PropTypes.string.isRequired, // Aqui falamos que marca é uma string, e que ela é necessária, ou seja, marca não pode ser enviada sem nenhbum valor.
    lancamento: PropTypes.number.isRequired, // Aqui falamos que lancamento é number (número), e que também é necessário, ou seja, não pode ser enviado sem nenhum valor.
  }

  Item.defaultProps = { // Caso nenhum valor for atribuido para 'marca', iremos adicionar um valor pelo default. Veja o exemplo: 
    marca: 'Nem um valor recebido', // Se caso 'marca' não tiver nenhum valor, irá ser exibido 'Nem um valor recebido'.
    lancamento: 0 // Se caso 'lancamento' não tiver nenhum valor, irá ser exibido '0'.
  }
```

[Vídeo explicativo](https://youtu.be/hcp1LqP2OCE)
