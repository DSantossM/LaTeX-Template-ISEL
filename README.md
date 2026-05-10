# Template LaTeX — Relatório de Trabalhos (ISEL)

> [!NOTE]  
> **Aviso:** Este projeto não é um modelo oficial fornecido pelo Instituto Superior de Engenharia de Lisboa (ISEL). É um projeto desenvolvido de forma independente, com o intuito de facilitar a escrita de relatórios em LaTeX.

Viva! Neste repositório encontras um template genérico em LaTeX para relatórios de trabalhos feitos no ISEL, compatível com qualquer cadeira.
Este template pode ser alterado para qualquer circustância necessária, e pode sofrer alterações.
<!-- Basta preencher as variáveis no topo do ficheiro e substituir o conteúdo placeholder pelo teu -->
Para começares a fazer relatórios encontras as instruções e guias em baixo para conseguires trabalhar com a ferramenta LaTeX.

---

## Como Começar:

### 1. Abre no Overleaf ou no Prism

> Não precisas de instalar nada — compila diretamente no browser. No entanto tens opções com o  `TexStudio` que te permite trabalhar diretamenta na tua máquina.

1. Faz download do ficheiro `.tex` e das imagens da pasta `/images`
2. Acede a [overleaf.com](https://www.overleaf.com) ou ao [prism.openai.com](https://prism.openai.com/) e cria uma conta gratuita
3. Clica em **New Project → Upload Project** e faz upload do ficheiro
4. Compila com **Ctrl + Enter** (duas vezes para o índice ficar correto)

### 2. Preenche os teus dados

No topo do ficheiro `.tex` encontras o bloco de variáveis — é o único sítio que tens de editar para personalizar a capa e o cabeçalho:

```latex
\newcommand{\relCadeira}{Nome da Cadeira}
\newcommand{\relAnoLetivo}{20XX / 20XX Verão/Inverno}
\newcommand{\relTitulo}{Título do Relatório}
\newcommand{\relSubtitulo}{Subtítulo do Relatório}
\newcommand{\relLicenciatura}{Licenciatura/Mestrado em ...}
\newcommand{\relAlunoA}{Aluno n.º XXXXX Nome Completo}
\newcommand{\relAlunoB}{Aluno n.º XXXXX Nome Completo}
\newcommand{\relDocente}{Nome do Docente}
```

---

## Estrutura do Repositório

```
template-latex-isel
 ┣ template_relatorio.tex     ← ficheiro principal do template
 ┣ guia_recursos_latex.tex    ← guia de recursos em LaTeX (opcional)
 ┣ README.md                  ← este ficheiro
 ┗ images/
    ┣ logo-isel.png           ← logo do ISEL (Aconselhado a não substituir)
	┣ newsmallogo.png           ← logo mini do ISEL (Aconselhado a não substituir)     
    ┗ sampleimage.jpg         ← imagem de exemplo (substitui pelas tuas)
```

---

## Estrutura do Template

| Bloco | Descrição |
|-------|-----------|
| `[0]` | Variáveis do relatório — preenche aqui |
| `[A]` | Pacotes e configurações globais |
| `[B]` | Cabeçalho e rodapé com linha vermelha |
| `[C]` | Página de título |
| `[D]` | Índice com numeração romana |
| `[E]` | Corpo do relatório — substitui pelo teu conteúdo |
| `[F]` | Referências bibliográficas |
| `[G]` | Anexos |

---

## Snippets Úteis

### Figura
```latex
\begin{figure}[h]
    \centering
    \includegraphics[width=0.8\textwidth]{images/nome.png}
    \caption{Descrição da figura.}
    \label{fig:nome}
\end{figure}
```

### Tabela
```latex
\begin{table}[h]
    \centering
    \begin{tabular}{|l|c|r|}
        \hline
        \textbf{Coluna A} & \textbf{Coluna B} & \textbf{Coluna C} \\ \hline
        Valor 1           & Valor 2           & Valor 3           \\ \hline
    \end{tabular}
    \caption{Descrição da tabela.}
    \label{tab:nome}
\end{table}
```

### Lista com pontos
```latex
\begin{itemize}
    \item Primeiro item.
    \item Segundo item.
\end{itemize}
```

### Lista numerada
```latex
\begin{enumerate}
    \item Primeiro item.
    \item Segundo item.
\end{enumerate}
```

### Equação
```latex
\begin{equation}
    f(x) = ax^2 + bx + c
    \label{eq:nome}
\end{equation}
```

### Referenciar figura / tabela / equação
```latex
Ver Figura~\ref{fig:nome}
Ver Tabela~\ref{tab:nome}
Ver Equação~\eqref{eq:nome}
```

### Comandos de formatação
```latex
\textbf{negrito}        % negrito
\textit{itálico}        % itálico
\texttt{código}         % monospace
\underline{sublinhado}  % sublinhado
\newpage                % nova página
\clearpage              % nova página + flush de figuras
```

---

## Recursos para Aprender LaTeX

### Editores Online
| Recurso | Descrição |
|---------|-----------|
| [Overleaf](https://www.overleaf.com) | Editor LaTeX online, colaborativo e gratuito — **começa aqui** |
| [Overleaf Templates](https://www.overleaf.com/latex/templates) | Galeria de centenas de templates prontos |
| [Prism - OpenAI](https://www.prism.openai.com) | Editor LaTeX online, colaborativo e gratuito disponibilizado pela OpenAI — **Podes começar aqui também** |

### Documentação
| Recurso | Descrição |
|---------|-----------|
| [Overleaf Learn](https://www.overleaf.com/learn) | Tutoriais do básico ao avançado — recomendado para iniciantes |
| [LaTeX Wikibook](https://en.wikibooks.org/wiki/LaTeX) | Referência completa e gratuita |
| [CTAN](https://ctan.org) | Documentação oficial de todos os pacotes LaTeX |
| [Detexify](https://detexify.kirelabs.org) | Desenha um símbolo e obtém o comando LaTeX |

### Comunidade e Ajuda
| Recurso | Descrição |
|---------|-----------|
| [TeX Stack Exchange](https://tex.stackexchange.com) | Fórum de perguntas e respostas — pesquisa antes de perguntar |
| [Reddit r/LaTeX](https://www.reddit.com/r/LaTeX) | Comunidade ativa com exemplos e ajuda |

### Templates e Código
| Recurso | Descrição |
|---------|-----------|
| [LaTeX Templates](https://www.latextemplates.com) | Coleção de templates gratuitos por categoria |
| [GitHub — latex-template](https://github.com/topics/latex-template) | Templates públicos no GitHub |
| [Awesome LaTeX](https://github.com/egeerardyn/awesome-LaTeX) | Lista curada de ferramentas e recursos |

### Ferramentas
| Recurso | Descrição |
|---------|-----------|
| [Tables Generator](https://www.tablesgenerator.com) | Cria tabelas visualmente e gera o código LaTeX |
| [Mathcha](https://www.mathcha.io) | Editor visual de equações com exportação LaTeX |
| [doi2bib](https://www.doi2bib.org) | Cola um DOI e gera a referência BibTeX automaticamente |
| [PDF24](https://www.pdf24.org) | Converter e editar imagens para incluir no LaTeX |

---

## ⌨️ Atalhos no Overleaf

| Atalho | Ação |
|--------|------|
| `Ctrl + Enter` | Compilar |
| `Ctrl + /` | Comentar / descomentar linha |
| `Ctrl + Z` | Desfazer |
| `Ctrl + F` | Pesquisar no código |
| `Ctrl + G` | Ir para linha |

---

## Dúvidas

Pesquisa primeiro em [tex.stackexchange.com](https://tex.stackexchange.com) — é muito provável que a tua pergunta já tenha resposta.

---

*Template criado por alunos do ISEL*
