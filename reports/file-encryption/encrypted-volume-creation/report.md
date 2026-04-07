# 🔐 Report: Criação e Montagem de um Volume Criptografado com VeraCrypt

### 📁 Cybersecurity Portfolio
**Autor:** [Seu Nome]  
**Data:** Abril de 2026

---

## 📌 Introdução

Este relatório documenta, de forma detalhada e passo a passo, o processo completo de **criação, montagem e validação funcional de um container de arquivo criptografado** utilizando o VeraCrypt em ambiente Linux.

O objetivo é demonstrar conhecimento prático em **criptografia de dados em repouso (data-at-rest)**, com ênfase em boas práticas de segurança, tais como:
- Seleção de algoritmos fortes (**AES-256 + SHA-512**)
- Geração de senha complexa com gerenciador de senhas (Proton Pass)
- Coleta adequada de entropia durante a formatação
- Criação de container padrão (não oculto)
- Montagem segura do volume
- Validação de leitura e escrita
- Comportamento seguro do arquivo fora do software

O processo foi realizado em uma máquina virtual Linux com o intuito de demonstração e construção de portfólio.

---

## 🖥️ Ambiente Utilizado

- Sistema operacional: Linux (interface XFCE)
- Ferramentas utilizadas:
  - **VeraCrypt** (versão mais recente disponível)
  - **Proton Pass** (geração de senha)
  - **Thunar** (gerenciador de arquivos)

---

## ⚙️ Descrição Passo a Passo com Explicação das Imagens

### 🖼️ Image 1 – Janela Principal do VeraCrypt
![VeraCrypt Main Window](https://github.com/Juliocesar-sec/Criptografia.VeraCrypt/blob/main/print-vera.png)  
A tela inicial do VeraCrypt foi aberta. Cliquei em **"Create Volume"** para iniciar o assistente de criação.

### 🖼️ Image 2 – Tipo de Volume
![Volume Type](https://github.com/Juliocesar-sec/Criptografia.VeraCrypt/blob/main/print-vera.1.arquivo.png)  
Escolhi **"Create an encrypted file container"** → **"Standard VeraCrypt volume"**. Optei por um container padrão (não hidden) por ser suficiente para a demonstração de portabilidade e proteção básica.

### 🖼️ Image 3 – Localização do Container
![Container Location](https://github.com/Juliocesar-sec/Criptografia.VeraCrypt/blob/main/print-vera.2.arquivo.png)  
Selecionei o local e nomeei o arquivo como `meu-volume-seguro.vc`. O arquivo será um container único e portátil.

### 🖼️ Image 4 – Opções de Criptografia
![Encryption Options](https://github.com/Juliocesar-sec/Criptografia.VeraCrypt/blob/main/print-vera.3.arquivo.png)  
Escolhi **AES-256** como algoritmo de criptografia e **SHA-512** como função hash. Essa combinação oferece excelente segurança e desempenho.

### 🖼️ Image 5 – Tamanho do Volume
![Volume Size](https://github.com/Juliocesar-sec/Criptografia.VeraCrypt/blob/main/print-vera.4.arquivo.png)  
Defini o tamanho em **500 MB** (tamanho suficiente para demonstração).

### 🖼️ Image 6 – Senha do Volume
![Volume Password](https://github.com/Juliocesar-sec/Criptografia.VeraCrypt/blob/main/print-vera.5.arquivo.png)  
Gerei uma senha forte e longa utilizando o **Proton Pass**. A senha contém letras maiúsculas/minúsculas, números e símbolos, com mais de 20 caracteres.

### 🖼️ Image 7 – Formatação do Volume
![Volume Formatting](https://github.com/Juliocesar-sec/Criptografia.VeraCrypt/blob/main/print-vera.6.arquivo.png)  
Na tela de formatação, movi o mouse aleatoriamente por aproximadamente **45 segundos** até o indicador de aleatoriedade ficar verde. Isso coleta entropia suficiente para gerar chaves criptográficas fortes. Escolhi **exFAT** como sistema de arquivos para garantir **compatibilidade cross-platform** (Linux, Windows e macOS).

### 🖼️ Image 8 – Confirmação de Sobrescrita e Processo de Formatação
![Overwrite Confirmation](https://github.com/Juliocesar-sec/Criptografia.VeraCrypt/blob/main/print-vera.7.arquivo.png)  
Confirmei a sobrescrita (o container é criado do zero) e acompanhei o processo de formatação.

### 🖼️ Image 9 – Volume Criado com Sucesso (parte 1)
![Volume Successfully Created](https://github.com/Juliocesar-sec/Criptografia.VeraCrypt/blob/main/print-vera.8.arquivo.png)

### 🖼️ Image 10 – Tela Final “Volume Created”
![Final Volume Created](https://github.com/Juliocesar-sec/Criptografia.VeraCrypt/blob/main/print-vera.9.arquivo.png)  
O volume foi criado com sucesso.

### 🖼️ Image 11 – Seleção do Volume para Montagem
![Volume Selection for Mounting](https://github.com/Juliocesar-sec/Criptografia.VeraCrypt/blob/main/print-vera.10.arquivo.png)  
Selecionei o slot 1 e escolhi o arquivo do container.

### 🖼️ Image 12 – Entrada da Senha para Montagem
![Mount Password Entry](https://github.com/Juliocesar-sec/Criptografia.VeraCrypt/blob/main/print-vera.11.arquivo.png)  
Informe a senha gerada anteriormente.

### 🖼️ Image 13 – Solicitação de Privilégios de Administrador
![Administrator Privilege Request](https://github.com/Juliocesar-sec/Criptografia.VeraCrypt/blob/main/print-vera.12.arquivo.png)  
O sistema solicitou privilégios de administrador (sudo) para montar o volume.

### 🖼️ Image 14 – Volume Montado com Sucesso
![Volume Mounted Successfully](https://github.com/Juliocesar-sec/Criptografia.VeraCrypt/blob/main/print-vera.13.arquivo.png)  
O volume foi montado corretamente e apareceu como um disco removível no Thunar.

### 🖼️ Image 15 – Tentativa de Abrir o Container Diretamente
![Attempt to Open Container Directly](https://github.com/Juliocesar-sec/Criptografia.VeraCrypt/blob/main/print-vera.14.arquivo.png)  
Ao tentar abrir o arquivo `.vc` diretamente com o gerenciador de arquivos, o conteúdo aparece como dados binários ilegíveis — comprovando que a criptografia está funcionando.

---

## 🔒 Resultados Obtidos

- Volume criptografado criado com sucesso
- Container portátil e compatível com múltiplos sistemas operacionais
- Proteção eficaz de dados em repouso
- Montagem e desmontagem seguras realizadas
- Validação funcional: copiei arquivos de texto e imagens para dentro do volume, li e modifiquei o conteúdo, desmontei e remontei o volume sem perda de dados
- Tentativa de acesso direto ao container falhou (dados permanecem criptografados)

---

## 🛡️ Conclusões de Segurança e Lições Aprendidas

Esta prática demonstrou as seguintes competências em cibersegurança:

- Uso correto e completo do VeraCrypt
- Aplicação de algoritmos criptográficos fortes (AES-256 + SHA-512)
- Importância da coleta de entropia durante a geração de chaves
- Escolha consciente de filesystem (**exFAT**) para portabilidade
- Geração e gerenciamento seguro de senhas
- Validação prática de que o arquivo container não revela nenhum dado sem a senha correta
- Boas práticas operacionais: nunca deixar o volume montado desnecessariamente, desmontar após o uso

**Lições principais:**
- A entropia é crítica para a força das chaves criptográficas — o movimento aleatório do mouse é uma forma simples e eficaz de aumentá-la.
- Containers VeraCrypt são uma solução excelente para backups seguros e transporte de dados sensíveis.
- Em ambientes corporativos, essa técnica pode ser combinada com políticas de senha, keyfiles ou hidden volumes para aumentar ainda mais a segurança.

---

## 📚 Considerações Finais

O volume criado pode ser montado em Linux, Windows e macOS sem problemas, tornando-o uma solução eficiente para:
- Armazenamento seguro de dados sensíveis
- Backups criptografados
- Proteção contra acesso não autorizado em caso de perda ou roubo de dispositivo

Essa competência é essencial para profissionais de segurança da informação.

---

## 🧰 Ferramentas Utilizadas

- VeraCrypt
- Proton Pass
- Linux (ambiente de teste)
