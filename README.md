
# Pytest

Seja bem-vindo ao meu teste que acabou se tornando um guia de primeira viagem ao uso da biblioteca Python 'Pytest'!

**Avisos:** 

* Este READ.ME é direcionado aos iniciantes e a utilizadores de Pytest de primeira viagem como eu fui neste mini projeto.
* Eu sou iniciante nestes testes e em Pytest. Se estou passando uma informação falsa, por favor me corrija!

## Primeiro passo
Para a execução destes testes, faça o download da pasta 'proj_files'.
## Instalação do Pytest

Obviamente, precisaremos da biblioteca Pytest. Faça a instalação:

```cmd
  pip install pytest
```

Nestes testes foi usada a versão 8.2.2. Para instalar esta versão específica, execute:

```cmd
  pip install pytest==8.2.2
```
## Uso simples e puro do Pytest

Navegue até o diretório da pasta com os arquivos baixados e execute:

```cmd
pytest
```

Isso é o suficiente para você ver as primeiras informações:

```cmd
========================================================= test session starts =========================================================
platform win32 -- Python 3.12.4, pytest-8.2.2, pluggy-1.5.0
rootdir: C:\Seu\diretório\para\pasta
plugins: cov-5.0.0
collected 15 items                                                                                                                                                                                                                                                                                                            

test_case_0%.py FFFFF
test_case_100%.py .....
test_case_65%.py ...FF  
```

Na frente de cada nome de arquivo você pode ver 'F' ou '.'

Os '.' referem-se a testes com sucesso e 'F' aos testes com falha.

E seguimos na seção "FAILURES". Você pode ver as falhas que aconteceram, incluindo as respectivas informações:

* Sub-seção por arquivo testado;
* Função onde ocorreu o erro;
* O conteúdo da linha em que o erro foi apontado;
* Qual foi o erro;
* Mais uma vez, o nome do arquivo;
* E por fim, o número da linha em que ocorreu o erro.

```cmd
================================================================ FAILURES ================================================================
_______________________________________________________________ test_find1 _______________________________________________________________

    def test_find1():
>       assert find_proportion(16, 4, 8, 'x') == 1
E       AssertionError: assert 2 == 1
E        +  where 2 = find_proportion(16, 4, 8, 'x')

test_case_0%.py:5: AssertionError

# [...] (Os resultados prosseguem)
```

Na última seção, "short test summary info", é apresentado um resumo com todos os erros ocorridos:

```cmd
======================================================== short test summary info =========================================================
FAILED test_case_0%.py::test_find1 - AssertionError: assert 2 == 1
FAILED test_case_0%.py::test_find2 - AssertionError: assert 8 == 1
FAILED test_case_0%.py::test_find3 - AssertionError: assert 1 == 2
FAILED test_case_0%.py::test_find4 - AssertionError: assert 0 == 1
FAILED test_case_0%.py::test_find5 - AssertionError: assert 0 == 1
FAILED test_case_65%.py::test_find4 - AssertionError: assert 0 == 1
FAILED test_case_65%.py::test_find5 - AssertionError: assert 0 == 1
```

## Resultados em HTML

### Sobre a biblioteca/plugin

Existem diversas bibliotecas, eu testei: a "[pytest-html](https://github.com/pytest-dev/pytest-html)" e "[pytest-cov](https://github.com/pytest-dev/pytest-cov)". 

### Pytest-html

#### Instalação

Para usar este plugin, primeiramente instale-o:

```cmd
pip install pytest-html
```

Para a versão específica:

```cmd
pip install pytest-html==4.1.1
```

#### Uso básico

Rode o seguinte comando:

```cmd
pytest --html=report.html
```

Como já pôde ser observado, este comando tem <parâmetro>:

```cmd
pytest --html=<arquivo>.html
```

Ele indica o nome do arquivo HTML que o plugin deve gerar com seus resultados.

### Pytest-cov

#### Instalação

Para utilizar, primeiramente instale-o:

```cmd
pip install pytest-cov
```

Nestes testes foi usada a versão 5.0. Para instalar a versão específica, execute:

```cmd
pip install pytest-cov==5.0.0
```

#### Uso básico

Para execução **neste** projeto:

```cmd
pytest --cov=proj_files --cov-report=html
```

Este comando também têm <parâmetros>. São eles:

```cmd
pytest --cov=<modulo> --cov-report=<formato>
```

Aqui está uma descrição desses parâmetros e de suas opções mais comuns:

* 'modulo': Especifica o módulo ou pacote para o qual você deseja medir a cobertura. Você pode fornecer múltiplos módulos, se necessário;
* 'formato': Especifica o formato do relatório de cobertura. Os formatos mais comuns incluem:
    - term: Exibe um resumo da cobertura no terminal;
    - html: Gera um relatório HTML detalhado que pode ser visualizado no navegador;
    - xml: Gera um relatório XML, útil para integração com ferramentas de CI/CD;
    - annotate: Cria arquivos anotados, adicionando comentários às linhas do código fonte que foram executadas.

## Autor

- [@antthLuca - Luca Anthony](https://www.github.com/antth-luca)

## Agradecimentos

Obrigado à você por ter chego até aqui, espero ter ajudado em algo.

Obrigado ao Prof. Dr. [Yuri Feitosa](https://www.linkedin.com/in/yurifeitosa/) por ter proposto a atividade de testes do software no componente Engenharia de Software II no IFPR - Campus Astorga.

[Python 3.12](https://docs.python.org/pt-br/3.12) - [Pytest](https://docs.pytest.org/en/8.2.x) - [Pytest-html](https://github.com/pytest-dev/pytest-html) - [Pytest-cov](https://github.com/pytest-dev/pytest-cov)

-- *Astorga, 16 de julho de 2024* --
