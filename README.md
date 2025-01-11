# Detecção de Phishing em E-mails

Este projeto é uma implementação simples em Python para detectar e-mails suspeitos de phishing, verificando se o corpo do e-mail contém palavras-chave frequentemente associadas a tentativas de fraude.

## Descrição do Código

O código foi desenvolvido para ajudar a identificar e-mails de phishing por meio da busca de palavras-chave específicas. Quando um e-mail contém termos como "ganhe", "prêmio", "urgente", "desconto", entre outros, o código classifica o e-mail como **Phishing**. Caso contrário, ele é classificado como **Seguro**.

## Como Funciona

1. **Função `verificar_phishing`**:
   A função recebe o corpo do e-mail como entrada e verifica se ele contém alguma das palavras-chave associadas a phishing. As palavras suspeitas são:
   - 'ganhe'
   - 'prêmio'
   - 'urgente'
   - 'desconto'
   - 'click'
   - 'promoção'

2. **Entrada do Usuário**:
   O e-mail é lido da entrada padrão, ou seja, o código espera que o texto do e-mail seja fornecido diretamente ao executar o script.

3. **Processamento**:
   O código percorre a lista de palavras suspeitas e verifica se alguma delas aparece no corpo do e-mail. Se encontrar uma palavra suspeita, o código retorna a classificação "Phishing", indicando que o e-mail é potencialmente perigoso. Caso contrário, retorna "Seguro".

4. **Saída**:
   O resultado da verificação (se é **Phishing** ou **Seguro**) é impresso no console.

Aqui está a explicação dos itens de 1 a 8 em formato Markdown:


## Explicação do Código

### 1. **Importação do módulo `sys`**
```python
import sys
```
- **Função:** A biblioteca `sys` é usada para acessar variáveis e funções que interagem diretamente com o sistema. No caso, ela é utilizada para ler a entrada do usuário a partir do terminal.
- **Uso:** Permite usar `sys.stdin.readline()` para capturar a entrada do usuário no terminal.

### 2. **Definição da função `verificar_phishing`**
```python
def verificar_phishing(mensagem):
```
- **Função:** Define uma função chamada `verificar_phishing` que recebe o corpo do e-mail como entrada. Essa função é responsável por identificar se o e-mail contém palavras-chave suspeitas de phishing.
- **Uso:** A função facilita a reutilização do código e a modularização.

### 3. **Lista de palavras suspeitas**
```python
palavras_suspeitas = ['ganhe', 'prêmio', 'urgente', 'desconto', 'click', 'promoção']
```
- **Função:** Cria uma lista com palavras-chave associadas a mensagens de phishing. Essas palavras são geralmente usadas em tentativas de fraudes, como "ganhe", "prêmio" e "urgente".
- **Uso:** A lista serve como uma referência para verificar se algum desses termos aparece no corpo do e-mail.

### 4. **Laço `for` para verificar palavras suspeitas**
```python
for palavra in palavras_suspeitas:
    if palavra.lower() in mensagem.lower():
        return "Phishing"
```
- **Função:** O laço `for` percorre cada palavra na lista `palavras_suspeitas`.
- **Uso:** Para cada palavra da lista, a função verifica se ela aparece no corpo do e-mail (`mensagem`). A função `lower()` é usada para garantir que a comparação seja feita sem considerar maiúsculas ou minúsculas.
- **Explicação:** Se uma palavra suspeita for encontrada, a função retorna "Phishing", indicando que o e-mail pode ser uma tentativa de phishing.

### 5. **Retorno de "Seguro"**
```python
return "Seguro"
```
- **Função:** Se nenhuma das palavras suspeitas for encontrada no corpo do e-mail, a função retorna "Seguro".
- **Uso:** Indica que o e-mail não contém palavras-chave de phishing e é considerado seguro.

### 6. **Leitura do corpo do e-mail**
```python
email_usuario = sys.stdin.readline().strip()
```
- **Função:** Usa `sys.stdin.readline()` para ler uma linha de entrada do terminal, que será o corpo do e-mail fornecido pelo usuário.
- **Uso:** A função `strip()` é utilizada para remover quaisquer espaços em branco ou quebras de linha extras antes e depois do conteúdo, garantindo que apenas o texto relevante seja processado.

### 7. **Chamada da função `verificar_phishing`**
```python
resultado = verificar_phishing(email_usuario)
```
- **Função:** A função `verificar_phishing` é chamada com o corpo do e-mail fornecido pelo usuário como argumento.
- **Uso:** O resultado retornado pela função (que pode ser "Phishing" ou "Seguro") é armazenado na variável `resultado`.

### 8. **Exibição do resultado**
```python
print(f"Classificação: {resultado}")
```
- **Função:** Exibe a classificação final do e-mail no terminal, informando se ele foi classificado como "Phishing" ou "Seguro".
- **Uso:** O comando `print()` é utilizado para exibir o resultado da verificação para o usuário.
```
