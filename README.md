# Desafio de Detecção de Phishing

Este repositório contém uma solução simples para detectar e-mails de phishing com base em palavras-chave específicas. O código verifica se o corpo do e-mail contém termos frequentemente usados em tentativas de phishing.

## Passos do Desafio

### 1. Análise do Problema
O objetivo do desafio era criar uma função simples para detectar e-mails de phishing. A função precisa identificar palavras-chave frequentemente associadas a e-mails de phishing, como "ganhe", "prêmio", "urgente", "desconto", entre outras.

### 2. Implementação da Solução
A solução foi implementada em Python, utilizando uma lista de palavras suspeitas e verificando se essas palavras estavam presentes no corpo do e-mail.

### 3. Testes Realizados
Foram feitos testes com várias mensagens, incluindo e-mails legítimos e e-mails de phishing. O código classifica corretamente os e-mails em "Phishing" ou "Seguro".

### 4. Ferramentas Utilizadas
- Python (versão 3.x)
- Biblioteca sys para leitura de entradas via terminal

## Como Rodar o Código

1. Clone este repositório para o seu computador:
   ```bash
   git clone https://github.com/SEU_USUARIO/desafio_phishing_detection.git
