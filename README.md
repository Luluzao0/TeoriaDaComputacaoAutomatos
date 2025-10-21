# Guia Rápido da Atividade (Aluno)

Aluno: Luis Guilherme Busaglo Lopes  
Matrícula: 20220086977  
Disciplina: Teoria da Computação e Compiladores  
Professor: Edilson Lima

Este é um resumo prático para abrir, simular e gerar os modelos no JFLAP.

## 1) O que abrir
Arquivos na pasta do projeto:
- AFD: `afd_acesso.jff`
- AFND: `afnd_entr_variacoes.jff`
- AFD (conversão do AFND): `afd_from_afnd_entr_variacoes.jff`
- Máquina de Turing: `mt_valida_entrada_codigo.jff`
- Mealy: `mealy_acesso.jff`
- Moore: `moore_acesso.jff`
- GLC: `glc_acesso.txt`

## 2) Como simular no JFLAP
- AFD/AFD convertido/Mealy/Moore:
  1. File > Open > selecione o `.jff`.
  2. Input > Step by State.
  3. Insira as entradas conforme os exemplos abaixo.
- AFND:
  1. File > Open > selecione `afnd_entr_variacoes.jff`.
  2. Input > Step with Closure (considera ε-transições).
- Máquina de Turing:
  1. File > Open > selecione `mt_valida_entrada_codigo.jff`.
  2. Input > Step ou Run; verifique se a fita é aceita.

## 3) Exemplos de entradas
- AFD (`afd_acesso.jff`): sequências por token
  - Aceita: `ENTRA, SAI, ACESSO456`
  - Rejeita: `ENTRA, SAI`
- AFND/AFD convertido (por caractere):
  - Aceita: `ENTRA`, `ENTRAR`, `ENTRO`
  - Rejeita: `ENTRAO`
- Turing (`mt_valida_entrada_codigo.jff`):
  - Aceita: `ENTRAACESSO123`, `ENTRAACESSO456`
  - Rejeita: `ENTRAACESSO124`
- Mealy (`mealy_acesso.jff`):
  - `ENTRA` → saída: `EM_ESPERA`
  - Após isso, `ACESSO123` ou `ACESSO456` → `ACESSO_CONCEDIDO`
  - `SAI` em qualquer momento → `ACESSO_NEGADO`
- Moore (`moore_acesso.jff`):
  - Estados e saídas: `q0: EM_ESPERA`, `q1: PROCESSANDO`, `q2: CONCEDIDO`, `q3: NEGADO`

## 4) O que capturar (screenshots)
- Diagrama de cada modelo aberto.
- Pelo menos um exemplo aceito e um rejeitado por modelo (quando fizer sentido).

## 5) Como montar a entrega
- Preencher `RELATORIO.md` com seus dados e colar as imagens.
- Exportar para PDF (ou entregar `.md` + imagens se aceito).
- Anexar também os `.jff`.

Envio por e-mail:  
- Para: `edilsonlima3@gmail.com`  
- Assunto: `ATIVIDADE PRÁTICA TEORIA DA COMPUTAÇÃO E COMPILADORES – 1BIM`  

- Use `Step by State` para ver o caminho de aceitação passo a passo.
- Em caso de erro “no transition defined”, a palavra é rejeitada.
