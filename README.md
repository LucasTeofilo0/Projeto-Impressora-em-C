# **Controle de Impressora Elgin i9 em C**
## **Sobre o projeto**
Este projeto foi desenvolvido por alunos com o objetivo de criar uma aplicação em **linguagem C** capaz de se comunicar com a impressora térmica **Elgin i9**, utilizando a **DLL oficial da Elgin**, conexão **USB** e testes de impressão feitos direto na impressora.  O trabalho faz parte da disciplina de **Construção de algoritmos**.

---
## **Tecnologias Utilizadas**
- Linguagem C
- GCC (MinGW) ou Code::Blocks
- E1_Impressora01.dll (biblioteca da Elgin, versão x86 ou x64)
- GitHub

## **Estrutura do Projeto**
- main.c                → Código-fonte do programa
- E1_Impressora01.dll   → Biblioteca da Elgin (x86 ou x64, na raiz do projeto)
- XMLSAT.xml            → XML de teste para o cupom SAT
- CANC_SAT.xml          → XML de teste para o cancelamento SAT
- README.md             → Este arquivo

## **Como compilar e executar**
### 1- Baixar o Projeto do GitHub
- Acesse o repositório.
- Clique no botão Code.
- Selecione Download ZIP.
- Aguarde o download.

### **2. Extrair o Arquivo ZIP**
- Vá até o local onde o arquivo foi salvo.
- Clique com o botão direito → Extrair aqui / Extract All.
- Será criada uma nova pasta com os arquivos.
  
### **3. Conferir a DLL (32 ou 64 bits)**
- Abra o terminal na pasta do projeto (clique na barra de endereço, digite cmd e aperte Enter).
- Digite gcc -dumpmachine e veja o resultado:
- x86_64-w64-mingw32 → use a DLL da pasta x64
- mingw32 ou i686-w64-mingw32 → use a DLL da pasta x86
- Copie a E1_Impressora01.dll certa para a pasta do projeto, junto com main.c, XMLSAT.xml e CANC_SAT.xml.
  
### **4. Compilar e Executar**
1. Ligue a impressora e conecte o cabo **USB**.
2. No terminal, compile o programa:
   ```
   gcc main.c -o impressora.exe
   ```
3. Execute o programa:
   ```
   impressora.exe
   ```
4. Faça login com o usuário `admin` e a senha `1234`.
   São 3 tentativas.
6. No menu, escolha a opção **1** (Configurar conexão) e responda:
   - Tipo: `1` (USB)
   - Modelo: `i9` (ou `i8`)
   - Conexão: `USB`
   - Parâmetro: `0`
7. Escolha a opção **2** (Abrir conexão) antes de usar as opções de impressão.
8. Para sair, digite **0**.

## **Opções do menu**
 
1. Configurar conexão
2. Abrir conexão
3. Fechar conexão
4. Imprimir texto
5. Imprimir QR Code
6. Imprimir código de barras
7. Imprimir XML SAT
8. Imprimir XML de cancelamento SAT
9. Abrir gaveta (Elgin)
10. Abrir gaveta
11. Sinal sonoro
12. -> 0.  Sair
   
## **Testes**
 
- Login com usuário e senha (3 tentativas)
  Usuário Padrão: admin
  Senha Padrão: 1234
- Abertura e fechamento da conexão com a impressora
- Impressão de texto, QR Code e código de barras
- Impressão dos XMLs SAT, gaveta e sinal sonoro

## **Documentação Adicional**
- Manual da Impressora Elgin i9
- Documentação da DLL da Elgin (E1_Impressora01.dll): https://elgindevelopercommunity.github.io/group___m1.html
- Enunciado do trabalho (Programação em C: Controlando uma Impressora Térmica Elgin)

 
## **Autores**
- Heloisa Alves Lima
- Lucas Teófilo Patussi
- Rafael André Costa
