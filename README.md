# Mineração de Repositórios - Foco em UX

Este projeto aplica técnicas de mineração de repositórios de software para investigar práticas de Experiência do Usuário (UX) em projetos de software. O objetivo é identificar e analisar padrões de UX, contribuindo para que equipes de desenvolvimento criem produtos mais eficientes, acessíveis e com usabilidade aprimorada.

Este trabalho faz parte da disciplina **Tópicos em Engenharia de Sistemas de Software 1**.

## Objetivo

A mineração de repositórios possibilita a análise de grandes volumes de dados de projetos de software, permitindo a extração de informações valiosas. Neste projeto, buscamos compreender como as práticas de UX são integradas aos projetos de software e identificar insights que ajudem no desenvolvimento de produtos mais eficazes.

## Funcionalidades

- **Coleta de Dados**: Extração de dados de repositórios hospedados no GitHub.
- **Análise de UX**: Identificação de práticas relacionadas à UX em commits, arquivos de protótipos, documentação de interfaces, entre outros.
- **Insights e Relatórios**: Geração de visualizações e relatórios sobre o impacto de práticas de UX.
- **Classificação e Organização**: Agrupamento dos repositórios conforme categorias de UX, facilitando análises específicas.

## Estrutura do Projeto

O projeto está organizado em três diretórios principais:
- `Code`: Contém os scripts para mineração de repositórios.
- `Database`: Armazena os arquivos CSV gerados durante a análise.
- `Image`: Contém imagens geradas pelos scripts para visualização dos resultados.

## Ordem de Execução

Para realizar a mineração e análise de repositórios com foco em UX, siga a ordem de execução dos scripts abaixo:

1. **`01-pesquisa.ipynb`**  
   Executa a busca inicial de repositórios no GitHub usando palavras-chave relacionadas à UI/UX.

2. **`02-detectar-idioma.ipynb`**  
   Detecta o idioma de cada repositório e filtra apenas os que estão em inglês.

3. **`03-filtros-aplicados.ipynb`**  
   Aplica filtros adicionais nos repositórios coletados para refinar os dados com base em critérios definidos.

4. **`04-filtros-por-arquivo-config.ipynb`**  
   Verifica a presença de arquivos específicos, como `package.json` e `composer.json`, para categorizar os repositórios.

5. **`05-categorizar-repositórios.ipynb`**  
   Classifica os repositórios nas categorias **Ferramenta UI**, **Aplicação UI**, **Componente UI**, ou **Não Classificado**. Gera dois arquivos CSV: um para repositórios classificados e outro para os não classificados.

6. **`06-data.ipynb`**  
   Organiza o conjunto de dados para análise, incluindo formatação de datas.

7. **`07-primeiras-analise.ipynb`**  
   Realiza uma análise preliminar, como distribuição de repositórios por ano.

8. **`08-busca-pelo-arquivo-config.ipynb`**  
   Realiza a busca e armazena o conteúdo dos arquivos de configuração presentes nos repositórios filtrados.

9. **`09-separar-dataset.ipynb`**  
   Segrega o dataset com base nos arquivos de configuração, criando CSVs específicos para cada tipo, como `package.json` e `composer.json`.

10. **`10-ranking.ipynb`**  
   Identifica e armazena os principais componentes de UI usados nos arquivos de configuração dos repositórios.

11. **`11-repositorios-frequencia.ipynb`**  
   A partir dos dados anteriores, realiza uma análise da frequência de uso de componentes de UI e configuração em diferentes repositórios.
