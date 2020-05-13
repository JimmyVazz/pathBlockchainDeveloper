# Ruta de aprendizaje de un desarrollador blockchain 💻

![Blockchain](https://www.welivesecurity.com/wp-content/uploads/2018/09/blockchain-que-es-como-funciona.jpg)

En este 2020 uno de los temas centrales en tecnología sigue siendo blockchain y las empresas buscan de que manera implementarlo. Para eso ha crecido la demanda por desarrolladores que dominen y tengan los skills necesarios para integrarlo a proyectos. 

Según [Google Trends]([https://trends.google.es/trends/explore?geo=MX&q=blockchain](https://trends.google.es/trends/explore?geo=MX&q=blockchain)) la búsqueda ha crecido y mantenido en los últimos meses. 
Si estás leyendo este artículo, espero que domines las bases y el concepto del funcionamiento del mismo. Sino, puedes correr a leer el siguiente [articulo]([https://medium.com/@JimmyVazz/el-verdadero-potencial-del-blockchain-moda-o-revoluci%C3%B3n-ca07fef2ea7a?source=---------8------------------](https://medium.com/@JimmyVazz/el-verdadero-potencial-del-blockchain-moda-o-revoluci%C3%B3n-ca07fef2ea7a?source=---------8------------------)) y después seguir con este path. 
Para resumir blockchain podemos decir de forma exacta que es:

>Conjunto de tecnologias que sirven para mover un activo o valor de un lugar a otro, sin la necesidad de un intermediario a través de una red distribuida de varios puntos a la vez 👍


Nos centraremos en la red blockchain ***ethereum*** la cual esta siendo muy potenciada por la comunidad y la cual nos deja desplegar scripts llamados ***"Smart Contracts".***  

No te enseñaré a fondo, sino que te mostrare el camino correcto, te diré donde leer, donde aprender y que usar para desarrollar 🔥.
<a name="top"> </a>
## Contenido
* [Funcionamiento de Ethereum](#item1)
* [Smart Contracts](#item2)
* [Solidity](#item3)
* [Herramientas de desarrollo](#item4)
* [Redes de prueba](#item5)
* [Foros de ayuda](#item6)
* [Buenas prácticas](#item7)
* [¿Dónde trabajar y de qué trabajar?](#item8)
<a name="item1"></a>
### Funcionamiento de ethereum
![Ethereum](https://quesoncriptomonedas.org/wp-content/uploads/2018/09/ethereum_logo.jpg)
Ethereum es parte de lo que se llama Blockchain 2.0, integrando programas llamados "Smart Contracts" que veremos en el siguiente bloque. Tiene el mismo protocolo de consenso como Bitcoin: ***Proof of work*** pero ya esta en camino la actualización que nos dará ***Proof of Stake***, la cuál saldrá en Ethereum 2.0 a mediados de año . Junto con su propia criptomoneda llamada ETH y su EVM, constituyen una super red que esta siendo usada por miles de devs para construir D'apps (aplicaciones descentralizadas).

Los conceptos más importantes que debes aprender son:
1. [Gas](https://medium.com/astec/entendiendo-el-gas-en-ethereum-e77a6f30090f)
2. [Ethereum Virtual Machine](https://criptotendencia.com/2018/05/13/ethereum-virtual-machine-una-caracteristica-que-hace-unica-a-ethereum/)
3. [Ether (ETH)](https://blockgeeks.com/guides/es/que-es-ethereum/)
4. [Tokens](https://es.cointelegraph.com/explained/what-is-a-token-and-how-does-it-work)
#### ¿Dónde estar al día?
1. El mejor lugar para estar al tanto de las noticias y cosas por venir es en la página oficial de  [Ethereum](https://ethereum.org/)
2. También te recomiendo seguir la [DevCon](https://archive.devcon.org/) la conferencia anual de desarrolladores ethereum. 
3. Y por último seguir a su creador [Vitalik Buterin](https://twitter.com/vitalikbuterin?lang=es) que siempre publica blogs o noticias. 

<a name="item2"></a>
### Smart Contracts
![Smart Contract](https://miro.medium.com/max/800/1*dZ5WRGrGQ5nQFkHV3iBzSA.jpeg)
Un SM es un programa que se ejecuta en la EVM y una vez deployado en la red, ya no puede ser modificado. Son usados debido a que su funcionamiento es automatizado y de acuerdo a los parámetros que recibe de la misma red se ejcuta tal y como fue programado. Por ejemplo:
1. Simplemente el funcionamiento de las transacciones de ETH fueron escritas en un SM.
2. Las apuestas virtuales son escritas con un SM, para que al ganador directamente se le depositen los fondos.
3. Ayuda a la creación de tokens (activos virtuales)

Puedes leer más y tener una perspectiva más clara en este [blog](https://es.cointelegraph.com/explained/what-is-a-smart-contract)

<a name="item3"></a>
### Solidity
![Solidity](https://i2.wp.com/cryptohabanero.com/wp-content/uploads/2018/10/400px-Solidity.png?fit=400%2C165&ssl=1)

Solidity es un lenguaje de programación orientado a objetos para escribir contratos inteligentes. Podemos decir que es una fusión entre JavaScript y Go. En Solidity tienes acceso tipos de datos diferentes como:
1. Integers
2. Booleans
3. Address
4. Strings
5. Contract
6. Estructuras de datos como: Arrays, Mappings.

Los que más debemos aprender y tener en cuenta son los address, contracts y mappings. Ya que, estos son los que son capaces de guardar las direcciones de wallets de otros usuarios y tienen la funcion de enviar o recibir eth.
Ejemplo:
```
pragma solidity >=0.4.22 <0.7.0;  //Versión, hay que tener en cuenta que de acuerdo a como declaremos la versión de compilador solo podrá correr en esas condiciones

/**
 * @title Storage
 * @Guarda y retorna el valor en una variable
 */
contract Storage {    //Clase Padre Storage que es de tipo contract

    uint256 number;    //Variable que guarda el valor 

    /**
     * @ guarda el valor
     * @param number 
     */
    function store(uint256 num) public {    //Funcion publica que recibe un valor y lo guarda
        number = num;
    }

    /**
     * @dev Return value 
     * @return value of 'number'
     */
    function retreive() public view returns (uint256){   //Funcion publica que retorna el valor guardado
        return number;
    }
}

```
La sintáxis puede parecerte rara o dificil, pero solo es un ejemplo de como se crea un SM. Ahora lo importante es saber donde aprender:
1. [Documentación oficial](https://solidity.readthedocs.io/)
2.  [Solidity Essentialls Book](https://arxiv.org/pdf/1905.01659)
3. Repositorio [GitHub]([https://github.com/ethereum/solidity](https://github.com/ethereum/solidity))

#### CriptoZombies
Es un juego interactivo para aprender a crear SM y D'apps. Es el que más recomiendo. Puedes jugarlo en [CriptoZombies](https://cryptozombies.io/es/)

<a name="item4"></a>
### Herramientas de desarrollo
![Truffle](https://blog.desdelinux.net/wp-content/uploads/2019/12/truffle-suite-herramientas-blockchain-imagen-destacada-blog-desdelinux-830x429.jpg)


<a name="item5"></a>
### Redes de prueba
![Metamask](https://miro.medium.com/max/800/1*QbMVQ5j_8XicEJX9-cLP1w.png)


<a name="item6"></a>
### Foros de ayuda
![openzepellin](https://www.endeavor.org.ar/wp-content/uploads/2019/02/OZ_logo_color.svg)

<a name="item7"></a>
### Buenas prácticas
![Remix](https://remix.ethereum.org/assets/img/sleepingRemiCroped.webp)

<a name="item8"></a>
### ¿Dónde trabajar y de qué trabajar?
![BD](https://miro.medium.com/max/600/1*dUCWPN9nE1TG45Sd5aAsJg.png)

[Subir](#top)
