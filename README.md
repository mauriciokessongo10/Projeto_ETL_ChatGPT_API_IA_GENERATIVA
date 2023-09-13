# Script de ETL e Geração de Letras de Músicas

Este é um script em Python que realiza operações de ETL (Extract, Transform, Load) em um arquivo Excel contendo letras de músicas de hip-hop e, em seguida, usa a API GPT-3 para gerar letras de músicas para artistas que não têm letras disponíveis.

## Requisitos

    1. Antes de usar este script, certifique-se de ter instalado a biblioteca `openai` executando o seguinte comando:

```
pip install openai
```
    2. Bem como ter todas as dependências e módulos que são necessárias para usar o script, espcificamente como: pandas, random, shutil e re
    3. É crucial que você baixe os arquivos excel que estão na pasta "arquivos de entrada" e inclua eles na raiz do Jupyter Notebook para que o script funcione corretamente, caso não terá que mudar os caminhos.
    4. O projeto foca bastante em inteligência artificial generativa, parte do conteúdo aprendido no Bootcamp de Ciência de Dados com Python da DIO juntamente com o Banco Santander. Sendo assim, esse projeto é um exemplo do uso de IA generativa.
    5. Criei e usei exaustivamente a chave da API do chatGPT que não é grátis. Por isso, sem essa chave fica impossível rodar o script (se não tiver créditos na sua conta de tokens da API do chat GPT).

## Uso

1. **Extract (Extração):**
   - O código começa lendo um arquivo Excel chamado 'genius_hip_hop_lyrics.xlsx' que contém as letras de músicas de hip-hop.
   - Ele remove algumas colunas especificadas do DataFrame.
   - Em seguida, ele limpa o texto nas colunas relevantes, convertendo-o para minúsculas e removendo caracteres especiais.
   - O DataFrame limpo é salvo novamente no arquivo 'genius_hip_hop_lyrics.xlsx'.

2. **Transform (Transformação):**
   - O script usa a API GPT-3 para gerar nomes de músicas, nomes de artistas e letras curtas para artistas que não têm letras disponíveis.
   - Os resultados da API são armazenados em um DataFrame intermediário chamado 'df_meio'.

3. **Load (Carregamento):**
   - O DataFrame intermediário 'df_meio' é combinado com o DataFrame original 'df'.
   - O arquivo Excel 'genius_hip_hop_lyrics.xlsx' é atualizado com os novos registros gerados.
   - Um novo arquivo Excel chamado 'NOVO_ARQUIVO_SAIDA_FINAL.xlsx' é criado na raiz do Jupyter Notebook com os dados atualizados.

## Configuração da API GPT-3
Antes de usar a API GPT-3, você deve inserir sua chave de API na variável `api_key`.

## Notas
- Certifique-se de que os arquivos Excel 'genius_hip_hop_lyrics.xlsx' e 'novo.xlsx' estejam presentes no diretório do seu Jupyter Notebook.
- O script assume que você já tem uma planilha com 378 registros e deseja adicionar 5 novos registros gerados pela API GPT-3.

## Execução
Para executar o script, basta copiar e colar o código em um ambiente Python compatível e certificar-se de que todas as dependências estejam instaladas.

## Autor
Maurício Cawanga Chilombo Kessongo