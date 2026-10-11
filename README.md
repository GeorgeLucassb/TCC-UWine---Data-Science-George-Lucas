# TCC UWine: Parte 1

Projeto Integrador do curso de Ciência de Dados da UVV, desenvolvido por **George Lucas**. O notebook analisa as vendas da
vinícola fictícia **UWine** (cerca de 1,12 milhão de notas fiscais) e responde às atividades da Parte 1:

- **A1:** tamanho ideal da amostra estratificada (bootstrap e alocação de Neyman), outliers e testes de hipóteses;
- **A2:** estatística descritiva das variáveis quantitativas e qualitativas;
- **A3:** resultado da pesquisa de satisfação.

O notebook já está salvo com todos os resultados. Para só ler a análise, abra
[`TCC_UWine_Parte1_George_Lucas.ipynb`](TCC_UWine_Parte1_George_Lucas.ipynb) aqui no GitHub. Para reproduzir os cálculos, siga os passos abaixo.

## Conteúdo

| Arquivo | Descrição |
|---|---|
| `TCC_UWine_Parte1_George_Lucas.ipynb` | Notebook com o código, os gráficos e as conclusões |
| `table26.csv` | Base de dados (~400 MB, armazenada com Git LFS) |
| `requirements.txt` | Bibliotecas Python e versões usadas |

## Pré-requisitos

- [Python 3.12](https://www.python.org/downloads/)
- [Git](https://git-scm.com/downloads) e [Git LFS](https://git-lfs.com/), necessário para baixar a base de dados
- Pelo menos 4 GB de memória RAM livre

## Como executar

**1. Clone o repositório**

```bash
git lfs install
git clone https://github.com/RaphaelNorris/tcc-uwine.git
cd tcc-uwine
```

Confira se a base veio completa: `table26.csv` deve ter cerca de 400 MB. Se tiver poucos bytes,
o Git LFS não estava instalado no momento do clone. Nesse caso, rode `git lfs pull`.

**2. Crie um ambiente virtual e instale as dependências**

Linux / macOS:

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt jupyter
```

Windows (PowerShell):

```powershell
py -3.12 -m venv .venv
.venv\Scripts\Activate.ps1
pip install -r requirements.txt jupyter
```

**3. Abra o notebook**

```bash
jupyter notebook TCC_UWine_Parte1_George_Lucas.ipynb
```

No Jupyter, use **Kernel → Restart & Run All**. A execução completa leva alguns minutos.

O notebook também pode ser executado direto no terminal, sem abrir o navegador:

```bash
jupyter nbconvert --to notebook --execute --inplace TCC_UWine_Parte1_George_Lucas.ipynb
```

## Observações

- A base é lida da pasta do projeto (`table26.csv`), então execute o notebook a partir dela.
- As versões em `requirements.txt` são as usadas na execução salva. Outras versões podem gerar
  pequenas diferenças nos números.
- Os sorteios usam semente fixa, então a execução reproduz os mesmos resultados.
