# Artigo 2  - Garbage Collector
**Autor**: Lucas Frutig - [https://github.com/lucas-frutig/]
**Data**: 1465829267575

# Garbage Collector

Garbage Collector teria uma tradução do tipo: "Memória Gerenciada"
É utilizado para o controle de variaveis, permitindo que variaveis não utilizadas possam ser descartadas.

# Exemplo de Garbage Collector

var eu = "Lucas Frutig";
document.write(eu);

Aqui declaro uma variável de nome "eu" e atribuo a ela o meu nome como valor. Depois chamo uma função nativa do JS que irá escrever
o valor desta função no documento.

Ok, agora caso eu não precise mais utilizar esta variável, basta setar o valor dela para null.

var eu = null;

Com isso o navegador limpa para nós a variável liberando automaticamente memória.

#Obs:

No caso de funções o gerenciamento de memória é feito automaticamente, pois em JS uma vez utilizada a função, ela é descartada, ou seja,
seus valores são resetados, fazendo assim a limpeza da memória.

**EX**:

function exibeNome(){
	var eu = "Lucas Frutig"
	document.write(eu);
};
exibeNome();






