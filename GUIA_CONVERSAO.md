# GUIA PARA GERAR RELATÓRIO EM PDF E WORD

## 📄 Relatórios Criados

Dois arquivos de relatório foram gerados em sua pasta:

1. **RELATORIO.tex** - Arquivo LaTeX profissional
2. **RELATORIO.txt** - Versão em texto formatado

## 🔄 Opção 1: Converter LaTeX para PDF

### Windows (PowerShell)

Se você tiver MiKTeX ou TeX Live instalado:

```powershell
# Navigate to the folder
cd "c:\Users\GUILHERME\Documents\TeoriaDaComputacaoAutomatos"

# Compile LaTeX to PDF
pdflatex RELATORIO.tex

# Run again for correct references
pdflatex RELATORIO.tex
```

### Método Online (Recomendado - Mais Fácil)

1. Acesse: https://www.overleaf.com
2. Clique em "New Project" → "Upload Project"
3. Faça upload do arquivo `RELATORIO.tex`
4. O Overleaf compila automaticamente
5. Clique em "Download PDF" para baixar

### Método Online Alternativo

1. Acesse: https://www.latex.online/
2. Copie o conteúdo de `RELATORIO.tex`
3. Cole na página
4. Clique em "Render"
5. Baixe o PDF gerado

## 📝 Opção 2: Converter para Word (.docx)

### Usando Pandoc (Recomendado)

Se você tiver Pandoc instalado:

```powershell
cd "c:\Users\GUILHERME\Documents\TeoriaDaComputacaoAutomatos"

# Converter para Word
pandoc RELATORIO.tex -o RELATORIO.docx

# Ou a partir do arquivo txt
pandoc RELATORIO.txt -o RELATORIO.docx --wrap=none
```

### Instalar Pandoc (se necessário)

```powershell
# Usando Chocolatey
choco install pandoc

# Ou download direto em: https://pandoc.org/installing.html
```

### Método Manual

1. Abra o arquivo `RELATORIO.txt` no Word
2. File > Save As > Format: Word Document (.docx)

## 📸 Adicionar Screenshots (IMPORTANTE!)

O relatório refere-se a captura de imagens. Para completar:

1. **Abra cada arquivo .jff no JFLAP:**
   - afd_acesso.jff
   - afnd_entr_variacoes.jff
   - afd_from_afnd_entr_variacoes.jff
   - mt_valida_entrada_codigo.jff
   - mealy_acesso.jff
   - moore_acesso.jff

2. **Capture imagens (Print Screen):**
   - Diagrama do autômato
   - Exemplo de teste aceito
   - Exemplo de teste rejeitado

3. **Crie pasta para as imagens:**
   ```powershell
   mkdir "c:\Users\GUILHERME\Documents\TeoriaDaComputacaoAutomatos\screenshots"
   ```

4. **Edite o documento LaTeX/Word:**
   - Adicione as imagens nas seções apropriadas
   - Use a sintaxe LaTeX: `\includegraphics{screenshots/nome.png}`

## 🚀 Resumo Rápido

| Formato Desejado | Caminho | Ferramenta |
|---|---|---|
| PDF | Overleaf.com | Navegador + Conta Gratuita |
| PDF | Local | MiKTeX/TeX Live + pdflatex |
| Word | Local | Pandoc |
| Word | Manual | Microsoft Word |
| Texto | Já criado | RELATORIO.txt |

## ✅ Próximos Passos

1. ✓ Relatório escrito em LaTeX - CONCLUÍDO
2. ✓ Relatório em texto formatado - CONCLUÍDO
3. ⏳ Converter para PDF (escolha um método acima)
4. ⏳ Adicionar screenshots dos autômatos
5. ⏳ Enviar para: edilsonlima3@gmail.com

## 📧 Entrega Final

Envie para o professor:
- RELATORIO.pdf (ou .docx)
- Pasta com screenshots/ (se houver espaço)
- Todos os arquivos .jff

---

Criado em: 2025-10-22
Para: Prof. Edilson Lima
Disciplina: Teoria da Computação e Compiladores
