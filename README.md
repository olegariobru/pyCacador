# Caçador de Duplicatas

Ferramenta desktop em Python para localizar arquivos duplicados por conteúdo e apoiar a organização de diretórios.

A busca agrupa arquivos pelo tamanho e calcula SHA-256 dos candidatos. A interface apresenta os grupos e uma estimativa do espaço recuperável.

## Funcionalidades

- Seleção da pasta de pesquisa.
- Filtros por tamanho mínimo, em bytes, e extensão.
- Varredura de subdiretórios com exclusões predefinidas.
- Processamento em uma thread com acompanhamento de progresso e cancelamento.
- Agrupamento por tamanho e hash SHA-256.
- Exportação de relatórios TXT e CSV.
- Registro dos arquivos que falham durante o cálculo de hash.
- Exclusão dos arquivos selecionados após confirmação.

## Tecnologias

Python, Tkinter, `hashlib`, `threading`, `csv` e módulos da biblioteca padrão.

## Como executar

Pré-requisitos: Python 3 com Tkinter e uma sessão gráfica. Algumas ações de abertura de pasta utilizam recursos específicos do Windows.

```bash
git clone https://github.com/olegariobru/pyCacador.git
cd pyCacador
python -m tkinter
python pyCacador.txt
```

O código-fonte está atualmente salvo em `pyCacador.txt`. O interpretador Python consegue executá-lo mesmo com essa extensão.

## Como utilizar

1. Selecione uma pasta de teste.
2. Ajuste o tamanho mínimo e, se necessário, a extensão.
3. Inicie a varredura e aguarde a apresentação dos grupos.
4. Exporte o relatório e revise os resultados.
5. Para exclusão, selecione somente as cópias que pretende remover.

A exclusão utiliza remoção direta de arquivos. Preserve uma cópia de cada conteúdo e valide inicialmente em uma pasta descartável com arquivos de teste.

## Limitações e próximos passos

- O repositório ainda não possui testes automatizados.
- A ação de ordenação da tabela está prevista, mas não implementada.
- A compatibilidade histórica com Python 2/Windows 7 mencionada no código não foi validada nesta documentação.
- Renomear o arquivo-fonte para uma extensão `.py` e organizar lógica e interface em módulos.
- Adicionar testes para agrupamento, filtros e exportação.
- Melhorar tratamento de erros e recuperação de arquivos removidos.

## Como contribuir

Abra uma issue com o problema ou a melhoria proposta. Para enviar código, crie um fork e uma branch, mantenha a alteração focada e abra um pull request explicando o resultado e como verificou o funcionamento.

## Licença

Este repositório ainda não contém um arquivo `LICENSE`. A licença de uso e redistribuição precisa ser formalizada pelo autor.

## Autor

[Bruno Olegário](https://github.com/olegariobru) · [LinkedIn](https://www.linkedin.com/in/bolgarimacedo/)
