# Apex Code Style
------------------

Guia de nomenclatura é  importante para os programadores por várias razões:

* 80% do custo de vida de um pedaço de software vai para manutenção.
Dificilmente qualquer software é mantido por toda a sua vida pelo autor original.
* Guia de Nomenclatura melhora a legibilidade do software, permitindo que os engenheiros entendam o novo código de forma mais rápida e completa.
* Se você enviar o código-fonte como um produto, você precisa se certificar que está bem embalado e limpo como qualquer outro produto que você cria.

## Tipos de Capitalização


Os tipos de capitalização determinam como um identificador será grafado em relação a letras maiúsculas e minúsculas, exemplos:

#### Pascal Case

A primeira letra do identificador e a primeira letra de cada palavra subsequente ao identificador é capitalizada (maiúscula).

Exemplo: **B**ack**C**olor

``` java  
class BackColor {
}
```

#### camel Case
A primeira letra do identificador é minúscula e a primeira letra de cada palavra concatenada ao identificador é capitalizada.

Exemplo: **b**ack**C**olor

### UPPER_CASE
Todas as letras do identificador são capitalizadas.

Exemplo: ***BACK_COLOR***

## Utilização dos Tipos de Capitalização


Na tabela abaixo são sumarizados os tipos de identificadores e a utilização dos tipos de  capitalização para cada identificador:

| Indentificadores | Capitalização (Case)| Exemplo |
| -- | -- | -- |
| Class | Pascal | Object , SalesOrder |
| Interface | Pascal | Notificable |
| Enum type | Pascal | StatusType |
| Enum Values | UPPER | APPROVED, WAITING_FOR_APPROVAL |
| Constants | UPPER | FILE_PATH |
| variables | camel | name, customerPONumber, purchaseOrder, customers |
| Class Attributes | camel | email , name , customerCode |
| methods | camel | sendMail , sendToApproval, findById |


## Declarações


### Classes e Interfaces

A primeira letra deve ser maiúscula e, se várias palavras forem escritas juntas para formar o nome, a primeira letra de cada palavra interna deve ser maiúscula (formato chamado “camelCase”). Para classes, os nomes devem normalmente ser substantivos. Para interfaces os nomes devem ser normalmente adjetivos.

Exemplo:

``` java

public with sharing class SalesOrder  {

    Supplier supplier;
    Customer customer;
    Billto billto;
    Shipto shito;

   	public SalesOrder() {
   	}
...
}

```

### Métodos

A primeira letra deve ser minúscula, e depois as regras camelCase devem ser usadas. Além disso, os nomes devem normalmente ser par de verbos-substantivo.

Exemplo: public void  **sendToApproval** () {}.

``` java

public with sharing class SalesOrder  {

    //attributes

   	public void sendToApproval () {
        // some code ...
    }

}

```

### Atributos de instância e de classe

Como nos métodos, o formato camelCase deve ser usado, começando com letra minúscula. A Sun recomenda usar nomes curtos e significativos.

Exemplo: nomeDoAtributo


Properties / Attributes
	Utilizar todos os atributos de instância como properties para minimizar o número de linhas de código. Evitar lógicas nos métodos get e set.
Constantes
As constantes Java são criadas marcando-se variáveis como static e final. Elas devem ser nomeada usando letras maiúsculas com caracteres underscore(“_”) como separadores.

Exemplo: READ_ONLY

Comentários
Todos os arquivos devem começar com um comentário estilo “linguagem C“ que relaciona o programador (s), a data, os direitos autorais e também uma breve descrição da finalidade do programa. Por exemplo:

/**
 * Classe Description
 *
 * @author
 */

OBS: Para os comentários em métodos e blocos de código usar a referência da Sun:

http://www.oracle.com/technetwork/java/javase/documentation/index-137868.html#format
