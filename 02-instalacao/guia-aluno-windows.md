# Guia do aluno para Windows

## Oficina: Desenvolvimento de Sites com Inteligência Artificial

Este guia foi preparado para os alunos da oficina que utilizarão **Windows 10** ou **Windows 11** em seus notebooks. O objetivo é deixar o computador pronto para acompanhar as atividades práticas sem depender de configurações avançadas.

## O que você vai instalar

Durante a preparação, você deverá instalar e configurar:

- Visual Studio Code
- Git
- Node.js
- OpenCode
- Conta GitHub
- Pelo menos um provedor de IA com acesso gratuito disponível

Em alguns casos, também poderá configurar:

- 9Router

## Antes de começar

Você precisará de:

- internet funcionando;
- acesso ao seu e-mail;
- permissão para instalar programas no notebook;
- tempo para concluir as etapas sem pressa;
- carregador do notebook.

## Regra principal

Siga as etapas **na ordem**. Não pule etapas, mesmo que pareçam simples.

## Etapa 1 — Identificar seu Windows

1. Pressione `Windows + R`.
2. Digite `winver`.
3. Pressione Enter.
4. Veja se aparece **Windows 10** ou **Windows 11**.
5. Anote essa informação.

Depois:

1. Pressione `Windows + I`.
2. Abra **Sistema**.
3. Entre em **Sobre**.
4. Verifique se o sistema é **64 bits**.

Se aparecer ARM64 ou 32 bits, avise o ministrante.

## Etapa 2 — Entender as permissões

Algumas instalações podem pedir autorização do Windows. Autorize somente quando tiver certeza de que você mesmo iniciou a instalação do programa correto.

Se o notebook pedir uma senha de administrador que você não tem, pare e avise o ministrante antes da oficina.

## Etapa 3 — Abrir o Prompt de Comando

1. Pressione `Windows + R`.
2. Digite `cmd`.
3. Pressione Enter.

Essa janela será usada para os comandos deste guia.

### Vídeo de apoio — opcional

**Título:** WINDOWS 11 INICIANTE #aula15 | PROMPT DE COMANDO  
**Link:** https://www.youtube.com/watch?v=RHHG1dyK2uA

**Para que assistir:** entender melhor o que é o Prompt de Comando e como abri-lo.

**Atenção:** use o vídeo apenas como apoio visual. Os comandos válidos para esta oficina são os que aparecem neste guia.

## Etapa 4 — Instalar o VS Code

1. Acesse o site oficial do Visual Studio Code: https://code.visualstudio.com/
2. Baixe a versão para Windows, preferencialmente **User Installer x64**.
3. Abra o instalador.
4. Avance pelas etapas mantendo as opções padrão.
5. Marque a opção de adicionar ao PATH, se ela aparecer.
6. Conclua a instalação.
7. Abra o VS Code.

### Vídeo de apoio — opcional

**Título:** Como Instalar o Visual Studio Code no Windows 11 em 2026 Passo a Passo  
**Link:** https://www.youtube.com/watch?v=kYb4I6DlYfg

**Para que assistir:** acompanhar visualmente a instalação do VS Code.

**Atenção:** siga a arquitetura e o instalador indicados neste guia. Não instale extensões extras sem necessidade.

## Etapa 5 — Instalar o Git

1. Acesse o site oficial do Git for Windows: https://git-scm.com/download/win
2. Baixe o instalador.
3. Execute o arquivo baixado.
4. Quando aparecer a escolha do editor, selecione o VS Code, se a opção estiver disponível.
5. Quando aparecer a configuração do PATH, escolha a opção que permite usar Git na linha de comando.
6. Conclua a instalação.

Teste no CMD:

```cmd
git --version
```

### Vídeo de apoio — opcional

**Título:** COMO INSTALAR O GIT NO WINDOWS  
**Link:** https://www.youtube.com/watch?v=tEG5CIJhiHw

**Para que assistir:** visualizar a instalação do Git no Windows.

**Atenção:** nas telas de configuração, siga as escolhas descritas neste guia, mesmo que o vídeo passe rapidamente por elas.

## Etapa 6 — Instalar o Node.js

1. Acesse o site oficial do Node.js: https://nodejs.org/
2. Baixe a versão **LTS** aprovada para a oficina.
3. Abra o instalador `.msi`.
4. Mantenha Node.js e npm selecionados.
5. Não instale ferramentas adicionais de compilação nesta etapa inicial.
6. Finalize a instalação.

Teste no CMD:

```cmd
node --version
```

```cmd
npm --version
```

### Vídeo de apoio — opcional

**Título:** Node.js - Como baixar e instalar  
**Link:** https://www.youtube.com/watch?v=DbJlrkW63XU

**Para que assistir:** ver o processo de instalação do Node.js no Windows.

**Atenção:** a versão exibida no vídeo pode ser diferente. Use a versão LTS indicada para a oficina.

## Etapa 7 — Criar conta no GitHub

1. Acesse https://github.com/
2. Clique em criar conta.
3. Informe seu e-mail.
4. Escolha uma senha segura.
5. Conclua a confirmação da conta.
6. Entre no GitHub.

Se você já possui conta, apenas confirme que consegue entrar nela.

## Etapa 8 — Configurar seu nome e e-mail no Git

No CMD, substitua pelos seus dados:

```cmd
git config --global user.name "Seu Nome"
```

```cmd
git config --global user.email "seu-email@example.com"
```

Depois teste:

```cmd
git config --global user.name
```

```cmd
git config --global user.email
```

## Etapa 9 — Criar uma pasta de teste

No CMD:

```cmd
if not exist "%USERPROFILE%\oficina-ia" mkdir "%USERPROFILE%\oficina-ia"
```

```cmd
if not exist "%USERPROFILE%\oficina-ia\teste-ambiente" mkdir "%USERPROFILE%\oficina-ia\teste-ambiente"
```

```cmd
cd /d "%USERPROFILE%\oficina-ia\teste-ambiente"
```

Depois:

```cmd
code .
```

## Etapa 10 — Instalar o OpenCode

No CMD, execute apenas a versão homologada pelo ministrante. Exemplo:

```cmd
npm install -g opencode-ai@1.19.3
```

Depois teste:

```cmd
opencode --version
```

Para abrir o OpenCode na pasta de teste:

```cmd
cd /d "%USERPROFILE%\oficina-ia\teste-ambiente"
```

```cmd
opencode
```

### Vídeo de apoio — opcional

**Título:** OpenCode no Windows com VS Code +IA Local/cloud  
**Link:** https://www.youtube.com/watch?v=I7Q7TY_wMrc

**Para que assistir:** conhecer visualmente a ferramenta OpenCode no Windows.

**Atenção:** não siga partes do vídeo que instalem Ollama ou modelos locais. Nesta oficina o foco é usar provedores por API.

## Etapa 11 — Escolher um provedor de IA

Você deverá preparar pelo menos um provedor. O ideal é também ter uma segunda opção de contingência.

As plataformas possíveis incluem:

- NVIDIA Build
- Google Gemini API
- GroqCloud
- OpenRouter
- Mistral Studio
- Cloudflare Workers AI

Siga apenas as orientações do ministrante sobre quais opções priorizar.

## Etapa 12 — NVIDIA Build

1. Acesse o portal da NVIDIA Build: https://build.nvidia.com/
2. Crie sua conta ou faça login.
3. Localize a área de API.
4. Gere uma chave para uso na oficina.
5. Guarde essa chave com segurança.

No OpenCode, use `/connect` para conectar esse provedor.

### Vídeo de apoio — opcional

**Título:** Como Usar os Modelos de IA Mais Fortes DE GRAÇA e Sem Cartão  
**Link:** https://www.youtube.com/watch?v=O_lQBkqq7lQ

**Para que assistir:** visualizar a criação de conta e chave no ecossistema NVIDIA Build.

**Atenção:** use apenas o trecho relacionado ao cadastro e à chave. O título do vídeo é promocional; a disponibilidade gratuita depende da sua conta e do serviço.

## Etapa 13 — Google Gemini API

1. Acesse o Google AI Studio: https://aistudio.google.com/
2. Faça login com sua conta Google.
3. Procure a área de chaves de API.
4. Crie uma chave no projeto correto.
5. Guarde a chave com segurança.

No OpenCode, use `/connect` para conectar o provedor Gemini.

### Vídeo de apoio — opcional

**Título:** Como Criar Chave API Key no Google AI Studio para Gemini  
**Link:** https://www.youtube.com/watch?v=7bgWVbZUxfI

**Para que assistir:** visualizar o processo de criação da chave Gemini.

**Atenção:** ignore partes do vídeo que tratem de Android Studio ou outros ambientes não usados nesta oficina.

## Etapa 14 — GroqCloud

1. Acesse o console da Groq: https://console.groq.com/
2. Crie sua conta.
3. Localize a área de API Keys.
4. Gere uma nova chave.
5. Guarde essa chave.

No OpenCode, use `/connect` para conectar o provedor Groq.

### Vídeo de apoio — opcional

**Título:** Groq: Como Usar IA Grátis nas Suas Automações no Make  
**Link:** https://www.youtube.com/watch?v=e5q8LffKPXY

**Para que assistir:** visualizar a criação da chave Groq.

**Atenção:** não crie automações no Make para esta oficina. Use apenas a parte referente ao cadastro e à API Key.

## Etapa 15 — OpenRouter

1. Acesse o OpenRouter: https://openrouter.ai/
2. Crie sua conta.
3. Localize a área de chaves.
4. Gere uma chave de API.
5. Escolha apenas modelos gratuitos indicados pelo ministrante.

No OpenCode, use `/connect` para ligar o OpenRouter.

### Vídeo de apoio — opcional

**Título:** Open Router: LLMs avançados e de graça para seus agentes de I.A.  
**Link:** https://www.youtube.com/watch?v=nnTeW4lVD0c

**Para que assistir:** visualizar a criação da conta, da chave e a identificação de modelos gratuitos.

**Atenção:** não interprete o título como garantia de gratuidade permanente. Verifique sempre o modelo indicado no momento da oficina.

## Etapa 16 — Testar o OpenCode com um arquivo HTML

Na pasta de teste, abra o OpenCode e envie um prompt simples como este:

```text
Crie um arquivo index.html simples, em português, com um título e um parágrafo informando que meu ambiente está pronto para a oficina.
```

Depois confira se o arquivo foi realmente criado dentro da pasta.

## Etapa 17 — Instalar o 9Router (somente se o ministrante orientar)

No CMD, exemplo de instalação:

```cmd
npm install -g 9router@0.5.104
```

Depois poderá ser necessário iniciar o 9Router conforme a orientação do ministrante.

## Etapa 18 — Checklist rápido antes da oficina

Você deverá chegar com:

- VS Code funcionando;
- Git funcionando;
- Node.js funcionando;
- OpenCode funcionando;
- conta GitHub acessível;
- pelo menos um provedor de IA configurado;
- pasta de teste criada;
- primeiro teste realizado.

## Problemas comuns

### `git` não é reconhecido

Feche o CMD e abra novamente. Se continuar, a instalação do Git deverá ser revisada.

### `node` ou `npm` não funcionam

Feche o CMD e abra novamente. Se o erro continuar, confira se o Node.js foi instalado corretamente.

### `opencode` não abre

Confira se a instalação foi concluída e se o comando foi executado em uma nova janela CMD.

### O provedor não aceita a chave

Verifique se a chave foi copiada corretamente e se o serviço escolhido está realmente disponível na sua conta.

## Recomendações finais

- Não compartilhe suas chaves de API.
- Não publique senhas em grupos de mensagens.
- Não mude várias configurações por conta própria quando aparecer um erro.
- Anote a etapa em que o problema aconteceu para facilitar o suporte.
