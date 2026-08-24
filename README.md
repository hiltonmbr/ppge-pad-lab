# 📋 Atividades avaliativas do curso de Programação e Análise de Dados com Python

**Programação e Análise de Dados com Python** · PPGE/UFPB · 2026.2

Prof. Dr. Hilton Ramalho

Este repositório é **seu**: você o criou clicando em **"Use this template"**
na página do repositório da disciplina no GitHub. É aqui que as atividades
avaliativas são entregues — não há upload de arquivo em lugar nenhum. A
entrega oficial, porém, só acontece quando o **link do seu repositório** é
enviado no Google Sala de Aula (veja "Como entregar" abaixo).

As atividades compõem o instrumento **"Exercícios práticos por bloco"**, que
vale **30% da nota final**.

Cada relatório tem o seu próprio tema, mas todos seguem a mesma estrutura descrita a seguir.

---

## 🗂️ As atividades

| #   | Relatório                                                                                 | Aulas | Unidade | Prazo         |
| --- | ----------------------------------------------------------------------------------------- | ----- | ------- | ------------- |
| 01  | [A Régua do Observatório Econômico Municipal](atividade-01-a-regua-do-observatorio.ipynb) | 1–2   | U1      | dom **30/08** |
| 02  | *em breve*                                                                                 | 3–4   | U1      | dom **06/09** |
| 03  | *em breve*                                                                                 | 5–6   | U1      | dom **20/09** |

> As demais atividades são publicadas ao longo do semestre. Quando uma nova
> for liberada, o professor avisa e você sincroniza o repositório com o
> template (as instruções vêm no aviso).

---

## 🎯 Como funciona

### Os seus dados são só seus

No **Passo 0** de cada notebook você digita a sua matrícula. Ela passa por um
resumo criptográfico **SHA-256** que semeia o gerador de dados: todo o
cenário da atividade — o município, o ativo, o jogo, o consumidor, depende
do relatório — sai dali.

Trocar um único dígito da matrícula produz um cenário inteiramente diferente.
Isso tem duas consequências práticas:

- **o notebook do colega não serve para você**, mesmo que o código dele esteja
  perfeito — os números são outros;
- **o professor confere qualquer entrega** recalculando os dados a partir da
  sua matrícula.

Discutir a _lógica_ com os colegas continua sendo bem-vindo e recomendado. O
que não transfere é a resposta.

### O que vale ponto

| Critério                                | Pontos |
| --------------------------------------- | ------ |
| Correção técnica dos exercícios         | 4,0    |
| Previsão e rastreamento (Parte 1)       | 1,5    |
| Questão autoral                         | 2,0    |
| Diário de bordo + relato do obstáculo   | 1,5    |
| Reflexão obrigatória + declaração de IA | 1,0    |

O código vale **menos da metade**. Os outros 6,0 pontos estão em coisas que só
você pode produzir: o que você previu antes de rodar, o obstáculo que
realmente te travou, a questão que você inventou, a reflexão sobre o que foi
difícil.

Essa distribuição é deliberada, e a razão está dita abertamente na seção
[🤖 Sobre IA](#-sobre-ia).

### As funções do kit

Cada atividade traz o seu kit em `scripts/kit_rNN.py`. A interface é sempre a
mesma:

| Função                     | Para quê                                         |
| -------------------------- | ------------------------------------------------ |
| `iniciar(matricula, nome)` | liga o kit e cria os seus dados                  |
| `prever(...)`              | carimba a sua previsão **antes** de você revelar |
| `registrar(etapa, nota)`   | marca uma etapa no seu diário de bordo           |
| `conferir(etapa, ...)`     | devolve um retorno sobre o que você resolveu     |
| `diario()`                 | mostra o seu ritmo de trabalho                   |
| `assinatura()`             | emite a linha de entrega                         |

**O `conferir()` não tira ponto e não quebra o notebook.** Ele olha o que você
respondeu e diz, item a item, o que ainda não fecha — dando uma **pista**,
nunca a resposta. Rode quantas vezes quiser: errar ali não custa nada, é
exatamente para isso que ele existe.

**O diário de bordo é seu e está à vista.** Ele fica em `diario-rNN.json`, ao
lado do notebook, e você lê quando quiser com `diario()`. Nada é coletado às
escondidas. Na correção, o que conta são as **notas** que você escreveu em
cada `registrar()` — uma nota específica ("travei no `elif`, tinha esquecido os
dois-pontos") vale mais que dez registros vazios.

---

## 📤 Como entregar

A entrega tem duas partes — o `git push` guarda o seu trabalho, mas **só
conta como entregue depois que o link do repositório for enviado no Google
Sala de Aula**.

1. Preencha **todas** as células `# TODO` e todos os campos de texto.
2. Rode o notebook **inteiro, de cima para baixo**, e **salve**. As saídas
   precisam estar visíveis no arquivo — é isso que o professor lê.
3. Rode a última célula, `assinatura()`, e copie a linha impressa.
4. Faça o commit final usando essa linha como mensagem, e dê push para a
   branch `main` do **seu** repositório:

```bash
git add atividade-01-a-regua-do-observatorio.ipynb
git commit -m "ASSINATURA: <cole aqui a linha impressa>"
git push
```

5. Vá ao **Google Sala de Aula**, abra a atividade correspondente e cole o
   endereço do seu repositório no GitHub. **É esse link que registra a
   entrega** — sem ele o professor não sabe que você terminou, mesmo que o
   push tenha funcionado.

Confira na página do repositório no GitHub se o notebook aparece com as
saídas.

> 💡 **Commits durante o trabalho são bem-vindos.** Commit a cada exercício
> resolvido, se quiser. O histórico é o registro mais honesto do seu processo,
> e nada nele é penalizado: um `git log` com idas e vindas é exatamente o que
> se espera de quem está aprendendo.
>
> ⏰ Vale o **último commit antes do prazo**. Você só precisa colar o link uma
> vez — se enviar antes de terminar, continue commitando e dando push até o
> prazo: é o último commit que entra na correção.

A correção volta como **nota e comentário no Google Sala de Aula** — é lá que
a conversa continua, e é lá que você responde se discordar de algum ponto.

### Rodando o notebook

Qualquer uma das três formas serve. Em todas, o diretório de trabalho precisa
ser a **raiz do seu repositório** (onde ficam o notebook e a pasta
`scripts/`) — é dali que o `import scripts.kit_rNN` enxerga o kit.

- **Local** — VS Code ou Jupyter, com a `venv` da disciplina.
- **GitHub Codespaces** — botão _Code → Codespaces_ na página do repositório.
- **Google Colab** — abra pelo GitHub (_File → Open notebook → GitHub_),
  lembrando de subir também a pasta `scripts/`, e de **baixar o `.ipynb` e
  commitá-lo** no fim: o Colab não faz push sozinho.

Os notebooks não usam rede, não pedem upload e não dependem do Drive. Só
Python puro até a Aula 13.

---

## 🤖 Sobre IA

A política por unidade é a do programa (§5.2):

| Unidade                         | Aulas | Política                        |
| ------------------------------- | ----- | ------------------------------- |
| **U1** — Fundamentos de lógica  | 1–10  | IA generativa **não permitida** |
| **U2** — Estruturas e dados     | 11–20 | permitida **com declaração**    |
| **U3** — Análise e visualização | 21–30 | permitida **com declaração**    |

A declaração é obrigatória em todas as atividades: de **não-uso** na U1, e em
formato de tabela na U2 e na U3 —

| ferramenta | o que pedi (prompt literal) | o que aceitei | o que rejeitei e por quê |

A coluna _"o que rejeitei"_ é a que interessa: ela exige que você tenha julgado
a saída, e não apenas colado.

### O desenho é honesto com você

Nenhuma parte desta disciplina tenta **impedir** o uso de IA — isso não
funciona e todo mundo sabe. O que estas atividades fazem é outra coisa:
**tornar o uso dela pouco útil para a nota**.

Uma LLM resolve os exercícios de código de qualquer notebook introdutório em
segundos. Por isso o código vale no máximo 4,0 de 10,0. Os outros 6,0 estão em
artefatos que ela não consegue produzir no seu lugar: dados que só existem
para a sua matrícula, o registro do seu próprio processo, o obstáculo que
_você_ enfrentou, a questão que _você_ inventou.

Quem terceirizar o código para a IA e **declarar isso honestamente** ainda
tira nota — só não tira nota alta. E o professor conversa com essa pessoa,
porque é o que faz sentido fazer.

**Os limites também são ditos abertamente:** o diário de bordo é falsificável
por quem se der o trabalho, e nenhum sinal levantado automaticamente vira
penalidade. Esses sinais servem para o professor **saber com quem conversar** —
nada além disso. As âncoras reais de verificação continuam sendo presenciais:
os **Checkpoints** (30%) e a **defesa oral** do projeto final.

A declaração honesta de uso, mesmo contrariando a política da unidade, é
tratada como questão pedagógica — a ser conversada. A declaração falsa é outra
coisa, e cai no regimento da UFPB.

---

## 🆘 Problemas comuns

**"Matrícula não parece válida"** — o `"..."` do template continua lá. Use a
sua matrícula completa do SIGAA, só dígitos, entre aspas.

**`ModuleNotFoundError: No module named 'scripts'`** — o notebook está sendo
rodado de outro diretório. Abra-o a partir da raiz do seu repositório (onde
ficam o notebook e a pasta `scripts/`).

**`unsupported format string passed to ellipsis.__format__`** — algum `...` de
`# TODO` ainda não foi preenchido, e um `print()` mais abaixo tentou formatá-lo.
Procure o `...` que sobrou na célula.

**"Apaguei meu diário sem querer"** — `limpar_diario()` recomeça do zero. Não é
o fim do mundo: conte o que aconteceu no campo do obstáculo, com as suas
palavras. Honestidade nunca custou ponto aqui.

**Travei de verdade** — use o fórum da turma no Google Sala de Aula, ou traga
para a aula. Pedir ajuda de forma bem descrita é uma habilidade avaliada, não
um demérito.
