# 🍀 4chan Media Downloader

Um aplicativo leve, rápido e com interface gráfica nativa para baixar todas as mídias (imagens e vídeos) de uma thread do 4chan/4channel com apenas um clique. Desenvolvido inteiramente em PowerShell.

## ✨ Funcionalidades

- **Interface Gráfica Simples (GUI):** Fácil de usar, sem precisar digitar comandos no terminal.
- **Inteligência de Link:** Basta colar a URL completa da thread e o programa identifica automaticamente o Board e o ID.
- **Velocidade e Estabilidade:** Utiliza a API oficial (`a.4cdn.org`) que garante downloads rápidos e evita bloqueios (sem necessidade de web scraping lento).
- **Leveza:** O executável final tem menos de 1MB e não requer instalação. Roda nativamente no Windows.
- **Feedback Visual:** Acompanhe o progresso do download em tempo real pela barra de progresso.
- **Suporte a Múltiplos Formatos:** Baixa automaticamente arquivos `.png`, `.jpg`, `.jpeg`, `.gif`, `.webm`, `.mp4` e `.mov`.

## 🚀 Como Usar (Para usuários)

1. Vá até a aba **[Releases](https://github.com/SEU-USUARIO/SEU-REPOSITORIO/releases)** aqui no lado direito da página.
2. Baixe a versão mais recente do arquivo `4chan_Downloader.exe`.
3. Coloque o executável em uma pasta da sua escolha (ex: `Downloads/4chan`).
4. Dê um clique duplo para abrir, cole o link da thread desejada e clique em "Baixar Arquivos".
5. Uma pasta será criada automaticamente com as mídias baixadas!

*(Nota: O Windows Defender pode mostrar um aviso na primeira vez por ser um .exe novo. Basta clicar em "Mais informações" e "Executar assim mesmo".)*

## 💻 Para Desenvolvedores (Código Fonte)

Se você quiser rodar o script diretamente ou modificar o código:

1. Clone este repositório ou baixe o arquivo `Interface_4chan.ps1`.
2. Clique com o botão direito no arquivo e selecione **"Executar com o PowerShell"**.
3. *Aviso de Política de Execução:* Caso o Windows bloqueie, abra o PowerShell como Administrador e rode: `Set-ExecutionPolicy RemoteSigned -Scope CurrentUser`.

### 🛠️ Como compilar o seu próprio `.exe`

Este projeto utiliza o módulo `ps2exe` para converter o script PowerShell em um executável com interface gráfica (escondendo a tela preta do console).

No PowerShell, execute:
```powershell
# 1. Instale o módulo (caso não tenha)
Install-Module -Name ps2exe -Scope CurrentUser

# 2. Compile o executável
Invoke-ps2exe -inputFile .\Interface_4chan.ps1 -outputFile .\4chan_Downloader.exe -noConsole
