# *Trabalho Prático II: Implementando um Gerenciador de Memória* 

> Project Status: Concluído :white_check_mark: 

> Repositório: [*MemoryManager*](https://github.com/erikldr/MemoryManager) :shipit:

**Alunos:** 

Erik Lucas da Rocha - 2732
        
Paulo Gabriel Pimenta Gomes - 3687

Foi disponibilizado pelo professor o codigo base, onde a partir dali deveriamos implementar a função do gerenciador de memória escolhida e assim realizar testes e comparar os resultados com o gerenciador de memória random.

### Como executar:

1 - Acessar a pasta do arquivo pelo terminal Linux 
2 - Para compilar o códig digitar o seguinte comando : gcc -Wall vmm.c -o vm 
3 - Para executar: ./vmm nru 10 < anomaly.dat

Apos isso o resultado sera mostrado no terminal.

**Explicação:**

Quando a execução do gerenciador Random é feita temos como resultado valores que variam de 8 a 10.
Já quando executamos o gerenciador NRU obtemos sempre 7 como resultado. 

O page fault (que é o que analisamos neste projeto) acontece quando uma aplicação tenta acessar determinado endereço de memória e ele não esta mapeado na memória RAM.

### Testes:

A titulo de comparação abaixo o resultado de 10 execuções dos dois gerenciadores de memória.

Random: {9, 10, 8, 8, 7, 8, 9, 7, 10, 9}

NRU: {7, 7, 7, 7, 7, 7, 7, 7, 7, 7}

Média de page faults dos gerenciadores:

Random: 8.5

NRU: 7
         
### Resultados:

Bem, com os resultados de ambos os gerenciadores podemos observar que:

O fato do gerenciador Random utilizar um metodo para gera numeros aleatoriamente faz com que haja uma oscilação grande, mas que mesmo se todas as execuções retornassem o menor valor (8) ainda assim o gerenciador nru seria melhor pois ficou abaixo desse valor com 7 page faults.


### Erros:
    Encontrado um erro que impedia a execução do código corretamente, mais especificamente na linha 140 onde é retornado como erro "core dumped" (acesso a posição de memória inexistente). 
	Objetivando encontrar o erro foram feitas algumas ações porem sem exito, não sendo possível resolver o erro da linha 140 e assim foi necessário comenta-la para a execução do código.
   
> Agradecemos ao projeto proposto pelo professor Rodrigo Moreira na disciplina de Sistemas Operacionais, da UFV-CRP. 
