# 📱 CryptoMonitor

## 🎯 Objetivo

O CryptoMonitor é um aplicativo Android desenvolvido em Kotlin com o objetivo de exibir, em tempo real, o valor atual do Bitcoin (BTC) negociado na plataforma Mercado Bitcoin. O app faz requisições à API do serviço e exibe o preço atualizado em Reais, junto da data e hora da última cotação.

---

## 🧰 Tecnologias Utilizadas

- **Kotlin** – Linguagem principal de programação  
- **Android SDK** – Base para desenvolvimento nativo Android  
- **Retrofit** – Cliente HTTP para chamadas à API REST (presumido)  
- **Coroutines** – Para chamadas assíncronas e sem travar a interface do app  
- **AppCompat** – Personalização e compatibilidade de interface  
- **ViewBinding / findViewById** – Acesso e atualização dos elementos da interface  

---

## 📂 Estrutura do Projeto

- `MainActivity.kt`: Tela principal do app. Configura a toolbar, o botão de atualização e realiza chamadas à API.  
- `MercadoBitcoinServiceFactory`: Classe com Retrofit que cria a instância de serviço para comunicação com a API.  
- Arquivo de layout XML: Contém a toolbar, botão de atualizar e os TextViews para valor e data.  

---

## 🔄 Funcionamento

1. O usuário abre o app e visualiza a toolbar e um botão **Atualizar**.  
2. Ao clicar em **Atualizar**, o app:
   - Inicia uma coroutine para realizar uma requisição HTTP.
   - Lê a resposta da API e extrai o preço atual do Bitcoin e o timestamp.
   - Formata o valor no padrão brasileiro de moeda (R$).
   - Converte o timestamp para data/hora legíveis.
   - Atualiza a tela com os dados recebidos.
3. Em caso de erro, uma mensagem (`Toast`) é exibida com a descrição apropriada.

---

## 📸 Capturas de Tela

### Antes de atualizar:
<img src="https://github.com/user-attachments/assets/c777c7b1-208b-464c-a37d-89a6df0a3b11" width="300">


### Depois de atualizar:
<img src="https://github.com/user-attachments/assets/57cd157c-a41f-40a9-bf2c-b04902277cf3" alt="Depois da atualização" width="300">

> As imagens mostram a interface principal do app, onde o usuário visualiza a cotação atual do Bitcoin e a data/hora da última consulta.

---

## 🧑‍💻 Referencias
Este projeto foi inspirado no repositório [Android Crypto Monitor][ref].

[ref]: https://github.com/carreiras/android-crypto-monitor

