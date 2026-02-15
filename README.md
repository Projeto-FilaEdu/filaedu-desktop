# FilaEdu Desktop

Aplicação desktop do sistema FilaEdu, responsável por exibir, gerenciar e acompanhar filas de forma local, enviando dados através da API REST do backend.

## Descrição

O FilaEdu Desktop é um cliente desktop desenvolvido em Java, utilizado para visualização em tempo real, controle e análise das filas.
A aplicação se comunica diretamente com o FilaEdu Backend por meio de requisições HTTP, consumindo endpoints REST para exibir registros, estatísticas e informações gerais da fila.

## Tecnologias

- Java 17
- Java Swing
- Maven
- OpenCV 4.8
- Consumo de API REST
- Git

## Pré-requisitos

Antes de rodar o projeto localmente, certifique-se de ter instalado:

- Java JDK 17
- Maven
- Git
- Backend FilaEdu em execução
- OpenCV 4.8 configurado corretamente

Verifique no terminal:

    java -version

## Clonando o repositório

    git clone https://github.com/Projeto-FilaEdu/filaedu-desktop.git

## Configuração do OpenCV

ATENÇÃO: etapa obrigatória para executar o projeto

Este projeto foi desenvolvido e testado utilizando OpenCV versão 4.8.
O uso de versões diferentes pode causar erros no carregamento das bibliotecas nativas.

Passo a passo:

1. Faça o download do OpenCV 4.8 no site oficial:
   https://opencv.org/releases/

2. Extraia o arquivo .zip

3. Renomeie a pasta extraída para opencv (se necessário)

4. Copie a pasta opencv para a raiz do sistema operacional

   Exemplo (Windows):

       C:\opencv

5. Verifique se o caminho das bibliotecas Java do OpenCV existe:

       C:\opencv\build\java\x64

6. Adicione o caminho abaixo à variável de ambiente PATH do sistema:

       C:\opencv\build\java\x64

7. Reinicie o computador para que as alterações tenham efeito.

Observações importantes:

- A ausência do OpenCV ou uma versão incompatível pode gerar erros como:
  - UnsatisfiedLinkError
  - Falha ao carregar biblioteca nativa
  - Aplicação não inicia

## Configuração da API

O projeto desktop consome a API do FilaEdu Backend.
Certifique-se de que o backend esteja rodando em:

    http://localhost:8080

## Importando o projeto no Eclipse

1. Abra o Eclipse
2. Vá em File > Import
3. Selecione Maven > Existing Maven Projects
4. Clique em Next
5. Em Root Directory, selecione a pasta do projeto (filaedu-desktop)
6. Aguarde o Eclipse carregar o projeto
7. Clique em Finish

## Baixando as dependências do projeto

Após importar o projeto na IDE, é necessário baixar as dependências definidas no Maven.

No Eclipse, isso acontece automaticamente ao importar o projeto como **Existing Maven Project**.  
Caso as dependências não sejam baixadas:

1. Clique com o botão direito no projeto  
2. Selecione **Maven > Update Project**  
3. Marque a opção **Force Update of Snapshots/Releases**  
4. Clique em **OK**

Aguarde até que o Maven finalize o download das dependências antes de executar a aplicação.

## Executando a aplicação na IDE

No Eclipse:

1. Localize a classe principal da aplicação em: `src/main/java/tela/TelaInicial.java`
2. Clique com o botão direito sobre a classe `TelaInicial`
3. Selecione **Run As > Java Application**

A aplicação desktop será iniciada e conectada ao backend.


## Integração

Este projeto faz parte do ecossistema FilaEdu e depende de:

- FilaEdu Backend (Spring Boot / REST API)
- FilaEdu Frontend (Angular)
- FilaEdu Desktop (Java)
