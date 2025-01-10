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
