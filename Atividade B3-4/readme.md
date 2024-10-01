**Sistema de Gerenciamento de Pedidos (Versão Recursiva)**

**Componentes da Equipe**
- Rafael Willian Galindo Neto
- Murilo Grillo Bastos
- Vitor Tamais Fischer
- Giovanni Montteiro

### **Descrição de Negócio**
O sistema de gerenciamento de pedidos foi desenvolvido para otimizar o atendimento ao cliente em restaurantes. Ele permite que os operadores gerenciem os pedidos de forma eficiente, garantindo que os itens estejam disponíveis em estoque e calculando o tempo total de preparo de forma precisa. O sistema opera em tempo real, proporcionando uma interação contínua e eficiente.

### **Problema Proposto / Solução Proposta**
O principal problema abordado pelo sistema é a gestão ineficiente de pedidos e de estoque nos restaurantes. A solução proposta automatiza o processamento de pedidos e monitora o estoque em tempo real, garantindo um atendimento rápido e eficiente. Além disso, o sistema fornece o tempo total de preparo, facilitando o planejamento e a organização da equipe de cozinha.

**Questões principais que o sistema resolve:**
- **Eficiência no Atendimento**: Automatizar o processamento de pedidos, diminuindo o tempo de espera.
- **Gestão de Estoque**: Verificar o estoque antes de processar cada pedido.
- **Planejamento de Preparo**: Oferecer uma visão clara do tempo total de preparo dos pedidos.

### **Requisitos do Sistema (Versão Recursiva)**

**Funcionais**
- **Entrada de Dados**: O sistema deve permitir a inserção do número de pedidos, tempos de preparo dos itens e quantidades disponíveis no estoque.
- **Processamento de Pedidos**: O sistema deve gerar e processar pedidos aleatórios a partir do menu, verificando o estoque e calculando o tempo total.
- **Verificação e Atualização de Estoque**: O sistema deve verificar o estoque antes de processar os pedidos e atualizá-lo após cada pedido processado.
- **Continuação de Pedidos**: O sistema deve permitir que o usuário continue processando pedidos até o esgotamento do estoque ou até que o usuário deseje parar.

**Não Funcionais**
- **Usabilidade**: O sistema deve ser simples e fácil de usar.
- **Desempenho**: O sistema deve ser capaz de processar pedidos rapidamente, mesmo em casos de múltiplos pedidos.
- **Confiabilidade**: O sistema deve operar sem falhas e de forma contínua.

### **Resumo do Código (Versão Recursiva)**

O código implementa o sistema utilizando **recursividade** para processar pedidos e verificar o estoque, ao invés de loops tradicionais. Ele é composto pelas seguintes funcionalidades:

- **Entrada de Dados**: O usuário insere o número de pedidos, tempos de preparo e quantidades em estoque.
- **Processamento de Pedidos**: Pedidos são processados aleatoriamente, e o sistema verifica a disponibilidade no estoque antes de processar cada um.
- **Verificação e Atualização de Estoque**: O estoque é verificado antes do processamento, e atualizado após cada pedido.
- **Processamento Recursivo**: O sistema continua processando pedidos de forma recursiva até que o estoque acabe ou o usuário decida parar.
  
### **Fluxo do Programa**
1. **Início**: O sistema solicita ao usuário o número de pedidos, os tempos de preparo dos itens e as quantidades no estoque.
2. **Entrada de Dados**: O usuário insere os dados de preparo e estoque.
3. **Processamento Recursivo**: O sistema processa pedidos recursivamente e verifica o estoque.
4. **Verificação de Estoque**: O sistema utiliza uma função recursiva para verificar se os itens estão disponíveis.
5. **Atualização do Estoque**: O estoque é atualizado após cada pedido.
6. **Continuação**: O sistema pergunta se o usuário deseja continuar processando pedidos ou parar.
7. **Cálculo do Tempo Total**: Após o término dos pedidos, o sistema calcula o tempo total de preparo recursivamente.
8. **Fim**: O programa termina.

### **Macro Solução**
A solução recursiva proposta consiste nas seguintes partes principais:

1. **Entrada de Dados**: O sistema solicita ao usuário o número de pedidos, tempos de preparo e quantidades em estoque.
   
2. **Funções Recursivas**:
    - **calcular_tempo_total(pedidos)**: Utiliza recursão para calcular o tempo total de preparo dos pedidos.
    - **verificar_estoque(estoque)**: Verifica de forma recursiva a disponibilidade de itens no estoque.
    - **processar_pedidos_recursivo(menu, estoque, pedidos, num_pedidos)**: Processa os pedidos de forma recursiva até que o número de pedidos seja zero.
    - **continuar_processando(estoque, menu, pedidos)**: Permite ao usuário continuar processando pedidos até o esgotamento do estoque ou até que ele decida parar.

3. **Ferramentas Utilizadas**
    - **Linguagem de Programação**: Python
    - **Ferramentas**: Python 3.x, GitHub para controle de versão.

---

### **Evolução da Análise**

### **Objetivos do Projeto**
O objetivo é otimizar o atendimento em restaurantes, automatizando a gestão de pedidos e verificando o estoque de forma eficiente.

### **Estrutura do Código**
A versão recursiva utiliza chamadas recursivas para processar pedidos e verificar o estoque, removendo a necessidade de loops tradicionais.

### **Cenários de Execução**
- **Melhor Caso**: Todos os itens estão disponíveis no estoque e o número de pedidos é pequeno. O processamento é rápido, pois os pedidos são processados imediatamente.
- **Pior Caso**: O estoque está quase esgotado e o número de pedidos é grande. O sistema pode precisar de várias verificações de estoque antes de processar pedidos, aumentando o tempo total de execução.

---

### **Função Assintótica Simplificada**
A análise assintótica do sistema recursivo é semelhante à versão com loops, mas agora o tempo de execução é descrito em termos das chamadas recursivas.

### **Funções Principais**
- **calcular_tempo_total(pedidos)**: A função percorre recursivamente a lista de pedidos, somando os tempos de preparo. A complexidade é \( O(n) \), onde \( n \) é o número de pedidos.
  
- **verificar_estoque(estoque)**: A função percorre recursivamente o estoque até encontrar o primeiro item disponível ou até percorrer todo o estoque. A complexidade é \( O(m) \), onde \( m \) é o número de itens no estoque.

- **processar_pedidos_recursivo(menu, estoque, pedidos, num_pedidos)**: A função processa pedidos recursivamente, com complexidade \( O(k \cdot n) \) para processar os pedidos e \( O(k \cdot m) \) para verificar o estoque, onde \( k \) é o número de pedidos.

### **Função Assintótica Final**
A complexidade total do sistema recursivo pode ser descrita como \( O(n + m + k \cdot (n + m)) \), onde \( n \) é o número de pedidos, \( m \) o número de itens no estoque e \( k \) o número de iterações necessárias.

---

### **Conclusão**
A versão recursiva do sistema de gerenciamento de pedidos mantém a eficiência, permitindo que os pedidos sejam processados de forma ordenada e que o estoque seja atualizado corretamente. A recursão oferece uma maneira alternativa de implementar o sistema, simplificando a lógica e eliminando a necessidade de laços.

---

### **Código em Python (Versão Recursiva)**

```
python
import random

def calcular_tempo_total(pedidos):
    if len(pedidos) == 0:
        return 0
    return pedidos[0] + calcular_tempo_total(pedidos[1:])

def verificar_estoque(estoque, index=0):
    if index >= len(estoque):
        return -1  # Nenhum item disponível
    if estoque[index] > 0:
        return index  # Retorna o índice do primeiro item disponível
    return verificar_estoque(estoque, index + 1)  # Verifica o próximo item

def processar_pedidos_recursivo(menu, estoque, pedidos, num_pedidos):
    if num_pedidos == 0:
        return pedidos

    item_index = random.randint(0, len(menu) - 1)  # Seleciona aleatoriamente um item do menu
    if estoque[item_index] > 0:
        pedidos.append(menu[item_index])
        estoque[item_index] -= 1
        print(f"Pedido processado: tempo de preparo = {menu[item_index]} minutos")
    else:
        print(f"Item {item_index + 1} esgotado!")

    return processar_pedidos_recursivo(menu, estoque, pedidos, num_pedidos - 1)

def continuar_processando(estoque, menu, pedidos):
    if verificar_estoque(estoque) == -1:
        print("Nenhum item disponível no estoque.")
        return pedidos

    continuar = input("Deseja continuar processando mais pedidos? (s/n): ")
    if continuar.lower() != 's':
        return pedidos

    num_pedidos =

 int(input("Digite o número de novos pedidos: "))
    pedidos = processar_pedidos_recursivo(menu, estoque, pedidos, num_pedidos)

    return continuar_processando(estoque, menu, pedidos)

def main():
    random.seed()  # Inicializa o gerador de números aleatórios

    num_pedidos = int(input("Digite o número inicial de pedidos: "))
    menu = [int(input(f"Digite o tempo de preparo do item {i + 1} (em minutos): ")) for i in range(5)]
    estoque = [int(input(f"Digite a quantidade em estoque do item {i + 1}: ")) for i in range(5)]

    pedidos = processar_pedidos_recursivo(menu, estoque, [], num_pedidos)
    pedidos = continuar_processando(estoque, menu, pedidos)

    total_tempo = calcular_tempo_total(pedidos)
    print(f"\nTempo total de preparo dos pedidos: {total_tempo} minutos")

if __name__ == "__main__":
    main()
´´´
