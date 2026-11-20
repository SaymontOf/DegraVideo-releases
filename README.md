# DegraVideo

Análise e degravação de vídeo e áudio com integridade pericial, para Windows 10/11 (64 bits).

Criado por **Saymont Carvalho Figueiredo**.

> Este repositório contém **somente os arquivos de instalação e o manual**. O código-fonte não é distribuído.

## Download
Baixe a versão mais recente na página de **[Releases](../../releases/latest)**:

| Arquivo | Uso |
|---|---|
| `DegraVideo_Setup_v<versão>.exe` | **Instalador** (recomendado). Instala por padrão em Arquivos de Programas, para todos os usuários. |
| `DegraVideo_v<versão>_win64.zip` | **Versão portátil**: descompacte e execute `DegraVideo.exe`. |
| `Manual_DegraVideo.pdf` | Manual do usuário (também em **Ajuda → Manual**, F1, dentro do programa). |
| `*.sha256` | Resumo SHA-256 de cada arquivo, para conferir o download. |

Não é preciso instalar Python nem FFmpeg. O modelo de transcrição automática já vem embutido e funciona sem
internet: nenhum áudio é enviado para fora do computador.

### Conferir o download
No PowerShell, compare o resultado com o conteúdo do arquivo `.sha256` correspondente:
```
Get-FileHash .\DegraVideo_Setup_v0.3.0.exe -Algorithm SHA256
```

### Aviso do Windows (SmartScreen)
O instalador ainda não tem assinatura digital de código. Por isso, o Windows pode exibir “O Windows protegeu o
computador”. Depois de conferir o SHA-256, clique em **Mais informações → Executar assim mesmo**.

## Funcionalidades
- **Casos, peritos e analistas**
  - Responsável e participantes (Perito ou Analista), com assinatura de todos.
  - Operador registrado na auditoria.
- **Importação**: as evidências são copiadas para dentro do caso, com SHA-256 conferido.
  - Caracterização completa (FFmpeg) e contagem real de quadros.
- **Visualizador quadro-exato**, que nunca descarta quadros
  - Data e hora do DVR em `.dav`.
  - Melhoria de imagem ao vivo.
- **Capturas** em PNG sem perdas, com SHA-256 e comentários
  - Melhoria de imagem: modelos prontos ou ajuste manual.
  - Marcações (seta, retângulo e círculo).
  - Régua de precisão relativa.
  - Recorte.
  - Tarja e desfoque de dados de terceiros (LGPD).
- **Relatório em PDF e/ou DOCX**
  - Sumário com links.
  - 1 ou 2 imagens por página.
  - Anexo de melhorias e medições.
  - Degravações.
  - Divisão em partes de até 5 MB para o PJe.
  - **Assinatura digital ICP-Brasil** (opcional), com verificação de assinaturas.
- **Degravação de áudio**: manual ou automática local (Whisper), com filtros de escuta e velocidade sem alterar o tom.
- **Exportação de trechos** em MP4 e **conversor para o PJe** (partes de até 85 MB), cada um com relatório.
- **Pacote do caso**: exporta o caso inteiro em um .zip conferível, com senha opcional.
- **Aviso de nova versão**: só informa, nunca baixa nada sozinho.
- **Auditoria** encadeada por hashes, **verificação de integridade** do caso e **proteção da instalação** contra
  adulteração.

O histórico de cada versão está nas notas da página de Releases.
