# Polícia e Ladrão

**Número da Lista**: 3<br>
**Conteúdo da Disciplina**: Algoritmos Gulosos<br>

## Alunos
|Matrícula | Aluno |
| -- | -- |
| 17/0138798  |  Caio Fernandes |
| 17/0050939  |  Lucas Dutra |

## Sobre 
### Problema Polícia e Ladrão:

Dado um `array` de tamanho **n** que tem as seguintes especificações:

1. Cada elemento do `array` contém um **policial** ou um **ladrão**.
2. Cada policial pode pegar apenas um ladrão.
3. Um policial não pode pegar um ladrão que esteja a mais de **K** unidades de distância do policial.

O objetio é encontrar o número máximo de ladrões que podem ser capturados.

Uma abordagem de força bruta seria verificar todos os conjuntos de combinações de polícia e ladrão e retornar o tamanho máximo definido entre eles. Sua complexidade de tempo é exponencial.

Uma solução eficiente é usar um **Greed Algorithm** (Algoritmo ambicioso). Mas selecionar uma propriedade ambiciosa pode ser complicado. Podemos tentar usar: *“Para cada policial da esquerda pegue o ladrão mais próximo possível”*.
Isso funciona para o exemplo três fornecido acima, mas falha para o exemplo dois, pois produz 2, que está incorreto.<br>

Também podemos tentar: 
*“Para cada policial da esquerda pegar o ladrão mais distante possível”*.
Isso funciona para o exemplo dois fornecido acima, mas falha para o exemplo três, pois produz 2, que está incorreto.<br>

Um argumento simétrico pode ser aplicado para mostrar que a travessia para estes do lado direito do `array` também falha.


Podemos observar que pensar independentemente do policial e se concentrando apenas nas obras de loteamento:

1. Oter o menor índice de policial `p` e ladrão `t`. Fazer uma distribuição
`if | p-t | <= k`  incrementando para o próximo `p` e `t` encontrado.
2. Caso contrário, aumentar `min(p, t)` para o próximo `p` ou `t` encontrado.
3. Repetir as duas etapas acima até que os próximos `p` e `t` sejam encontrados.
4. Retornar o número de distribuições feitas.


## Screenshots
Adicione 3 ou mais screenshots do projeto em funcionamento.

## Instalação 
**Linguagem**: Python<br>

### Para `MacOS`:
1. `venv` no python 3:
    ```
        python3 -m venv <envname>
    ```
2. Ativando `virtualenv`:
    ```
        source <envname>/bion/activate
    ```
3. Instalando `requirements.txt`:
    ```
        pip3 install -r requirements.txt
    ```
4. Ativando `venv` no Jupyter Notebook:
    ```
        python3 -m ipykernel install --name=<envname>
    ```


## Uso 
Explique como usar seu projeto caso haja algum passo a passo após o comando de execução.

## Outros 
Quaisquer outras informações sobre seu projeto podem ser descritas abaixo.




