# Azure Cognitive Search: Utilizando AI Search para Indexação e Análise de Dados

## Introdução

O objetivo deste projeto é explorar as funcionalidades do **Azure Cognitive Search** para indexação e consulta de dados, com foco em análise de sentimentos e extração de informações relevantes. Essa atividade foi realizada como parte do Bootcamp **Microsoft Azure AI Fundamentals**, da DIO.

Neste projeto, utilizamos técnicas de Document Intelligence para analisar **avaliações de consumidores** sobre um produto fictício, um café. A análise é realizada por meio da construção de um índice no **Azure AI Search**, que permite buscar e obter insights valiosos a partir de avaliações textuais.

## Objetivo

- Testar as ferramentas de **indexação** e **pesquisa** oferecidas pelo **Azure AI Search**.
- Aplicar **Document Intelligence** para enriquecer os dados com insights, como análise de sentimentos e extração de frases-chave.
- Analisar avaliações de consumidores para identificar tendências e sentimentos sobre um produto específico.

## Recursos do Azure necessários
- Um recurso do Azure AI Search , que gerenciará a indexação e a consulta.

- Um recurso de serviços de IA do Azure , que fornece serviços de IA para habilidades que sua solução de pesquisa pode usar para enriquecer os dados na fonte de dados com insights gerados por IA.

- Uma conta de armazenamento com contêineres de blobs, que armazenarão documentos brutos e outras coleções de tabelas, objetos ou arquivos.

### Configuração do Azure AI Search

#### Criando o Recurso no Azure

Siga os passos abaixo para configurar o **Azure AI Search** no portal do Azure:

1. **Acesse o Portal do Azure** ([portal.azure.com](https://portal.azure.com)).
2. Clique no botão **"+ Criar um recurso"**.

3. No campo de pesquisa, digite **"Azure AI Search"** e selecione a opção correspondente.
    ![Image 01](/assets/img/image01.png)

4. Configure o recurso com os seguintes parâmetros:
   - **Assinatura:** Selecione sua assinatura do Azure.
   - **Grupo de Recursos:** Escolha um grupo existente ou crie um novo com um nome exclusivo.
   - **Nome do Serviço:** Defina um nome único para o recurso.
   - **Localização:** Selecione qualquer região disponível. Caso esteja no **Leste dos EUA**, escolha `"East US 2"`.
   - **Nível de Preço:** Selecione **Básico**.

    ![Image 02 - Criando um recurso](/assets/img/image02.png)

5. Clique em **"Revisar + Criar"**.


6. Aguarde a validação e, ao ver a mensagem **"Validação bem-sucedida"**, clique em **"Criar"**.

    ![Image 03](/assets/img/image03.png)

### Envio de Dados e Criação do Índice

As avaliações que serão analisadas neste projeto estão disponíveis [aqui](https://aka.ms/mslearn-coffee-reviews).

  ![Image 07](/assets/img/image07.png)

Após configurar o container de armazenamento, os dados foram enviados para essa área, garantindo que fiquem acessíveis para o processamento.

  ![Image 12](/assets/img/image12.png)

Com os arquivos devidamente armazenados, o próximo passo é utilizar o Azure AI Search para construir um índice e extrair insights valiosos dos documentos. Esse processo pode ser feito por meio de um assistente integrado ao portal Azure, disponível na página principal do recurso.

### Consultas no Índice

O Azure AI Search também conta com um assistente para executar pesquisas diretamente no índice recém-criado, retornando os resultados no formato JSON.

   ![Image 12](/assets/img/image12.png)

Na imagem a seguir, é possível visualizar um exemplo de consulta que filtra resultados baseados na localização dos registros, neste caso, Chicago.

   ![Image 11](/assets/img/image11.png)

Além disso, podemos aprofundar a análise buscando avaliações com sentimento negativo, utilizando a extração automática de emoções contida nos documentos.

   ![Image 10](/assets/img/image10.png)



## Conclusão e Insights

Com a enorme quantidade de dados gerados todos os dias, organizar e extrair informações relevantes se tornou um grande desafio. Utilizando o Azure AI Search junto com técnicas de Document Intelligence, é possível transformar textos brutos em insights úteis, facilitando a análise e a tomada de decisões.
