# Artigos - Herança

**Autor**: Lucas Frutig - [lucas-frutig](https://github.com/lucas-frutig)

**Data**: 1465841561998

Diferente das linguagens mais conhecidas, como Java o C++, que utilizam a orientação a objetos clássica,
**JavaScript** utiliza um tipo de orientação diferente, baseada em protótipos.

## Herança Clássica (OOP)

Herança em Orientação a Objetos (OOP) é a capacidade de classes compartilharem entre sí, atributos(propriedades) e métodos.

**Ex: Java**
'
// setamos a classe como abstrata pois não desejamos criar
// objetos do tipo animal, apenas os tipos mais
// especializados como Gato ou Cachorro podem ser instânciados

public abstract class Animal {
  public void nascer() {
    // ...
  }

  public void morrer() {
    // ...
  }

  public void respirar() {
    // ...
  }
}
'
Agora definiremos a classe Gato herdando atributos e métodos da classe Animal. Podemos chamar a classe Animal de superclasse também.

**Ex:**
'
// além do método miar, os objetos do tipo Gato
// terão também, devido a herança, os métodos de Animal
class Gato extends Animal {
  public void miar() {
    // ...
  }

  // construtor
  public Gato() {
    // ...
  }
}
'
A palavra reservada 'extends' é responsável pela relação de herança no exemplo acima.

## Protótipos (JS)

Na linguagem de programaça **JavaScript** praticamente tudo é um objeto, até mesmo 'function' são objetos.
Então se quisermos herdar propriedades e métodos de um objeto, utilizamos como herança o protótipo deste objeto, por exemplo:

**Herança em JS**

'
//Primeiro criamos um objeto vazio.
//Automaticamente usará o protótipo de Object.

var Animal = {}

Animal.comer = true;
Animal.respirar = function(){
 console.log('Eu respiro');
}
Animal.morrer - true;
Animal.hasOwnProperty('comer') // método herdado de Object
Object.getPrototypeOf(Animal) // retorna Object

'
**Obs:Podemos criar objetos no JavaScript através de funções construtoras:**
'
function Animal(comer,respirar,morrer){
   this.comer = true;
   this.respirar = true;
   this.morrer = true;
};
'
**Herdando de funções construtoras**
'
var gato = new Animal(comer,respirar,morrer){
};

gato.comer; // true
'
**Obs:**
Podemos criar propriedades e métodos específicos de cada animal:

'
//Criando porpriedades exclusivas:
gato.escalamuro = true;
ga.escalamuro; //true

//Criando métodos exclusivas:
gato.miar = function(){
 return console.log("Miau");
};



