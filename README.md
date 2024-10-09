# Relatório com Análise dos Dados Automatizada

## Descrição
Este projeto tem como objetivo criar um sistema automatizado para análise de dados, gerando um relatório HTML estilizado utilizando Bootstrap. A ferramenta automatiza o processo de análise exploratória, exibindo estatísticas principais e gráficos para facilitar a visualização e compreensão dos dados. O sistema é desenvolvido em Python, utilizando bibliotecas populares como `pandas`, `matplotlib`, `seaborn` e `jinja2`.

## Integrantes
- **Rony Ken Nagai** - RM: 551549
- **Tomáz Versolato Carballo** - RM: 551417

## Funcionalidades
- Geração de um relatório HTML automatizado a partir de um dataset fornecido.
- Estatísticas principais exibidas:
  - Número de linhas e colunas.
  - Número de variáveis e observações.
  - Quantidade de células faltantes e linhas duplicadas.
  - Tipos de variáveis (numéricas e categóricas).
- Geração de gráficos:
  - Histogramas para variáveis numéricas.
  - Gráficos de contagem para variáveis categóricas.
- Estilização do relatório utilizando Bootstrap para garantir responsividade e melhor visualização.

## Estrutura do Código
1. **Template HTML**: Um template criado com Bootstrap é utilizado para exibir os dados de forma organizada e visualmente agradável.
2. **Funções principais**:
   - `resumo_df(df)`: Gera um resumo das estatísticas principais do dataset.
   - `plot_64(fig)`: Converte os gráficos em strings Base64 para serem incorporados ao HTML.
   - `criar_plot(df)`: Gera gráficos para variáveis numéricas e categóricas.
   - `gerar_html(df)`: Renderiza o template HTML com os dados e gráficos gerados e salva o relatório como um arquivo HTML.

## Como Executar

### Pré-requisitos
- Python 3.x
- Google Colab (recomendado para execução rápida e visualização no navegador)
- Bibliotecas Python: `pandas`, `matplotlib`, `seaborn`, `jinja2`, `base64`, `io`, `os`

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
- **Sumário**: Informações básicas como o número de linhas, colunas, variáveis e observações, além de células faltantes e duplicadas.
- **Tipos de Dados**: Lista de colunas e seus tipos de dados.
- **Tipos de Variáveis**: Número de variáveis numéricas e categóricas.
- **Valores Faltantes**: Quantidade de valores ausentes em cada coluna.
- **Gráficos**: Histogramas e gráficos de contagem organizados em um layout responsivo.

## Exemplo de Uso
Se você quiser testar o código, basta usar um dataset padrão, como o exemplo abaixo:
```python
df = pd.read_csv('/content/Diabetes.csv')
report_path = gerar_html(df)
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

## Possíveis Melhorias Futuras
- Adicionar opções interativas no relatório, como filtragem de dados e gráficos interativos.
- Implementar exportação do relatório para formatos como PDF.
- Integrar a ferramenta com uma interface web para que usuários possam subir datasets e gerar relatórios diretamente.

## Contato
Caso tenha dúvidas ou sugestões, entre em contato com os autores:
- Rony Ken Nagai - [LinkdIn]([mailto:ronyken@example.com](https://www.linkedin.com/in/rony-nagai/))
- Tomáz Versolato Carballo - [LinkedIn]([mailto:tomascarballo@example.com](https://www.linkedin.com/in/tomazcarballo/))

```
