# 1 **Vetor auto-ajustável (dinâmico)**
## language : C++

## 1. Introdução
 Neste tutorial, aprenderemos sobre vetores em C++ com a ajuda de exemplos.
Em C++, os vetores são usados ​​para armazenar elementos de tipos de dados semelhantes. No entanto, ao contrário dos arrays, o tamanho de um vetor pode crescer dinamicamente.

 > Ou seja, podemos alterar o tamanho do vetor durante a execução de um programa conforme nossos requisitos.

Eles fazem parte da bibliote Padrão C++ **vector**
```c++ 
#include <vector>
```

## 1.2 Declaração de vetor C++

Veja como podemos declarar um vetor em C++ :

```c++ 
// inicializa o vetor;
std::vector<Type> vect_name;
```

> O parâmetro type **T** especifica o tipo do vetor. Seja ele primitivo ou não.

## 1.3 Adicionar elementos a um vetor

Para adicionar um elemento em um vetor, usamos o metodo push_back(). Ele insere um elemento no final do vetor.

```c++ 
#include <iostream>
#include <vector>
using namespace std;

int main() {
  vector<int> num {1, 2, 3, 4, 5};

  cout << "Vetor inicial: ";

  for (auto i : num) {
    cout << i << "  ";
  }
  
  // incrementa o numero 6 e depois o 7 no vector
  num.push_back(6);
  num.push_back(7);

  cout << "\nVetor atualizado: ";

  for (auto i : num) {
    cout << i << "  ";
  }

  return 0;
}
```
### Resultado
```
Vetor inicial: 1 2 3 4 5  
Vetor atualizado: 1 2 3 4 5 6 7
```

> **Nota** : Também podemos usar as funções insert()e emplace()para adicionar elementos a um vetor.

## 1.4 Acessar Elementos de um Vetor

Como um **array** , também podemos usar os colchetes [] para acessar os elementos do vetor. Por exemplo,

```c++
vector<int> num {1, 2, 3};
cout << num[1];  // Output: 2
```

> **Nota** : Existe um método **at()** que é similar a acessar com colchetes, mas ela faz uma verificação se o vector está fora do limite.



# 2 Vantagens e desvantagens do vetor auto-ajustável (dinâmico) sobre o array em C++


## 2.1 Introdução
Vector é uma classe de modelo e é apenas uma construção C++, enquanto os arrays são uma construção de linguagem interna e estão presentes em C e C++.

Eles são implementados como arrays dinâmicos com interface de lista, enquanto arrays podem ser implementados estaticamente ou dinamicamente com interface de tipo de dados primitivo.

## Diferenças entre vetor e array

- Um vetor é um array dinâmico, cujo tamanho pode ser aumentado, enquanto o tamanho do array não pode ser alterado.
- O espaço de reserva pode ser fornecido para vetor, enquanto que para array você não pode fornecer espaço reservado. 
    > reservar espaço na memoria **HEAP** array fica no **STACK**
- Um vetor é uma classe enquanto uma array é um tipo de dados.
- Vetores podem armazenar qualquer tipo de objeto, enquanto um array pode armazenar apenas valores homogêneos.

## Vantagens em Arrays

- Arrays suportam acesso aleatório eficiente aos membros.
- É fácil ordenar um array.
- Eles são mais apropriados para armazenar um número fixo de elementos.

## Desvantagens dos Arrays

- Elementos não podem ser excluídos
- A criação dinâmica de arrays não é possível
- Vários tipos de dados não podem ser armazenados

## Vantagens do Vetor

- O tamanho do vetor pode ser alterado
- Vários **objetos** podem ser armazenados
- Elementos podem ser deletados de um vetor

## Desvantagens do Vetor

- Um vetor é um objeto, o consumo de memória é maior.