# Relatório com Análise dos Dados Automatizada

## Descrição
Este projeto tem como objetivo criar um sistema automatizado para análise de dados, gerando um relatório HTML estilizado utilizando **Bootstrap**. A ferramenta automatiza o processo de análise exploratória, exibindo estatísticas principais e gráficos para facilitar a visualização e compreensão dos dados. O sistema é desenvolvido em **Python**, utilizando bibliotecas populares como `pandas`, `matplotlib`, `seaborn` e `jinja2`.

## Integrantes
- **Rony Ken Nagai** - RM: 551549
- **Tomáz Versolato Carballo** - RM: 551417

## Funcionalidades
- Geração de um relatório HTML automatizado a partir de um dataset fornecido.
- Estatísticas principais exibidas:
  - Número de linhas, colunas, variáveis e observações.
  - Quantidade de células faltantes e linhas duplicadas.
  - Tipos de variáveis (numéricas e categóricas) e seus detalhes.
- Geração de gráficos detalhados:
  - **Histogramas** para variáveis numéricas.
  - **Gráficos de dispersão** para visualização de relações entre variáveis.
  - **Regressão linear** para identificar tendências em variáveis numéricas correlacionadas.
  - **Boxplots** para mostrar a distribuição dos dados e outliers.
  - **Mapas de calor** para visualização de correlações entre variáveis.
- Estilização do relatório utilizando **Bootstrap** para garantir responsividade e uma apresentação visual clara.

## Estrutura do Código
1. **Template HTML**: 
   - Um template criado com **Bootstrap** é utilizado para exibir os dados de forma organizada e visualmente agradável. 
   - Inclui seções detalhadas para estatísticas e gráficos, além de considerações finais automáticas geradas com base nos dados analisados.
2. **Funções principais**:
   - `resumo_df(df)`: Gera um resumo das estatísticas principais do dataset, incluindo variáveis, observações, valores faltantes e linhas duplicadas.
   - `gerar_conclusao(df)`: Analisa correlações e padrões nos dados, gerando conclusões automáticas sobre outliers e assimetrias nas variáveis.
   - `plot_64(fig)`: Converte gráficos em strings Base64 para serem incorporados ao HTML diretamente, garantindo visualização independente do ambiente.
   - `criar_plot(df)`: Gera diversos gráficos (histogramas, dispersão, boxplots, regressão linear e mapas de calor) para explorar diferentes aspectos do dataset.
   - `gerar_html(df)`: Renderiza o template HTML com os dados, gráficos e conclusões gerados, salvando o relatório como um arquivo HTML no Google Colab.

## Como Executar

### Pré-requisitos
- **Python 3.x**
- **Google Colab** (recomendado para execução rápida e visualização no navegador)
- Bibliotecas Python:
  - `pandas`
  - `matplotlib`
  - `seaborn`
  - `jinja2`
  - `base64`
  - `os`
  - `io`

### Passo a Passo
1. Faça o upload do dataset que você deseja analisar no Google Colab.
2. Certifique-se de que todas as bibliotecas necessárias estão instaladas. Utilize os comandos:
   ```python
   !pip install pandas matplotlib seaborn jinja2
   ```
3. Execute o código no notebook Colab e carregue o dataset desejado com:
   ```python
   df = pd.read_csv('/content/Diabetes.csv')
   ```
4. O relatório será gerado automaticamente e exibido no Colab em um `IFrame` para fácil visualização.

## Estrutura do Relatório
O relatório gerado inclui as seguintes seções:
- **Sumário**: 
  - Informações básicas como o número de linhas, colunas, variáveis, observações, células faltantes e linhas duplicadas, com explicações claras sobre cada item.
- **Tipos de Dados**: 
  - Lista de colunas e seus tipos de dados, detalhando a estrutura das variáveis presentes.
- **Estatísticas Descritivas**: 
  - Exibe medidas estatísticas (média, mediana, desvio padrão, valores mínimos e máximos) com explicações para ajudar na interpretação dos dados.
- **Valores Faltantes**: 
  - Quantidade de valores ausentes em cada coluna e orientações sobre a importância de tratá-los.
- **Gráficos**: 
  - Histogramas, gráficos de dispersão, regressão linear, boxplots e mapas de calor organizados em um layout responsivo para facilitar a visualização.
- **Conclusões das Análises**: 
  - Lista conclusões automáticas sobre correlações significativas, outliers e assimetrias observadas nas variáveis.
- **Considerações Finais**: 
  - Um resumo do projeto e das análises feitas, sugerindo etapas futuras para melhorar e aprofundar as análises com base nos dados.

## Exemplo de Uso
Se você quiser testar o código, basta usar um dataset padrão, como o exemplo abaixo:
```python
df = pd.read_csv('/content/Diabetes.csv')
report_path = gerar_html(df, 'Diabetes.csv')
```

O relatório será gerado e salvo em `/content/relatorio.html`. Você pode visualizar o relatório diretamente no Colab utilizando:
```python
from IPython.display import IFrame
IFrame(report_path, width=800, height=600)
```

## Tecnologias Utilizadas
- **Python**
- **Google Colab**
- **Bootstrap** para estilização do relatório
- **pandas**, **matplotlib**, **seaborn** para análise e visualização dos dados
- **jinja2** para renderização de templates HTML

## Contato
Caso tenha dúvidas ou sugestões, entre em contato com os autores:
- **Rony Ken Nagai** - [LinkedIn](https://www.linkedin.com/in/rony-nagai/)
- **Tomáz Versolato Carballo** - [LinkedIn](https://www.linkedin.com/in/tomazcarballo/)

---
