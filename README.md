# Tutorial: Como Usar a Anthropic e o Claude - Guia Completo para Iniciantes

## Parte 1: Como Criar uma Conta na Anthropic

### O que é a Anthropic?
A Anthropic é a empresa que desenvolveu o Claude, um assistente de IA avançado projetado para ser útil, inofensivo e honesto.

### Passo a passo para criar sua conta:

1. **Acesse o site oficial da Anthropic**
   - Abra seu navegador (Chrome, Safari, Firefox, etc.)
   - Digite na barra de endereço: https://www.anthropic.com
   - Pressione Enter

2. **Procure o botão de registro**
   - No canto superior direito da página, procure um botão como "Sign Up", "Get Started" ou "Try Claude"
   - Clique neste botão

3. **Preencha o formulário de cadastro**
   - Digite seu endereço de e-mail
   - Crie uma senha segura (combine letras maiúsculas, minúsculas, números e símbolos)
   - Confirme sua senha digitando-a novamente
   - Marque as caixas necessárias para aceitar os termos de serviço e política de privacidade
   - Clique no botão "Criar Conta" ou "Sign Up"

4. **Verifique seu e-mail**
   - Abra seu aplicativo de e-mail ou site de webmail
   - Procure por um e-mail da Anthropic (verifique também a pasta de spam ou lixo eletrônico)
   - Abra o e-mail e clique no link de verificação

5. **Complete seu perfil**
   - Após clicar no link de verificação, você será redirecionado para completar seu perfil
   - Preencha as informações solicitadas, como nome e sobrenome
   - Clique em "Concluir" ou "Complete Registration"

6. **Pronto! Sua conta está criada**
   - Agora você tem acesso ao painel da Anthropic e pode começar a usar o Claude

## Parte 2: Como Gerar uma API Key

### O que é uma API Key?
Uma API Key (chave de API) é como uma senha especial que permite que programas de computador acessem os serviços da Anthropic de forma segura.

### Passo a passo para gerar sua API Key:

1. **Faça login na sua conta Anthropic**
   - Acesse https://www.anthropic.com
   - Clique em "Log In" ou "Sign In" no canto superior direito
   - Digite seu e-mail e senha
   - Clique em "Entrar" ou "Sign In"

2. **Acesse a seção de API**
   - Após fazer login, procure por "API" ou "Developer" no menu principal ou no painel de controle
   - Clique nesta opção para acessar a área de desenvolvimento

3. **Crie uma nova API Key**
   - Procure por um botão como "Create New API Key", "New Key" ou "+ API Key"
   - Clique neste botão

4. **Configure sua API Key**
   - Dê um nome à sua API Key (por exemplo, "Meu Projeto Pessoal")
   - Selecione as permissões necessárias (se aplicável)
   - Clique em "Criar" ou "Create Key"

5. **Copie e guarde sua API Key**
   - A API Key será exibida na tela
   - IMPORTANTE: Copie esta chave e guarde-a em um local seguro
   - ATENÇÃO: Esta chave geralmente é mostrada apenas uma vez. Se você não salvá-la, precisará criar uma nova

6. **Proteja sua API Key**
   - Nunca compartilhe sua API Key publicamente
   - Não a inclua diretamente em códigos que serão compartilhados
   - Trate-a como uma senha importante

## Parte 3: Como Instalar o Claude Code (CLI)

### Pré-requisitos: Instalando o Node.js

**Para Windows:**

1. **Baixe o instalador do Node.js**
   - Acesse [nodejs.org](https://nodejs.org/en/)
   - Baixe a versão LTS (Long Term Support) recomendada
   - Execute o instalador baixado

2. **Siga as instruções do instalador**
   - Aceite os termos de licença
   - Escolha o diretório de instalação ou mantenha o padrão
   - Na tela de personalização, certifique-se de que "Add to PATH" está marcado
   - Clique em "Install" e aguarde a conclusão

3. **Verifique a instalação**
   - Abra o Prompt de Comando (CMD)
   - Digite os seguintes comandos para verificar se o Node.js e o npm foram instalados corretamente:
     ```
     node --version
     npm --version
     ```
   - Você deve ver os números das versões instaladas

**Para Mac:**

1. **Instale o Node.js usando Homebrew (recomendado)**
   - Abra o Terminal
   - Se você ainda não tem o Homebrew instalado, instale-o com:
     ```
     /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
     ```
   - Depois, instale o Node.js:
     ```
     brew install node
     ```

2. **Alternativa: Baixe o instalador do Node.js**
   - Acesse [nodejs.org](https://nodejs.org/en/)
   - Baixe a versão LTS para macOS
   - Execute o instalador e siga as instruções

3. **Verifique a instalação**
   - Abra o Terminal
   - Digite:
     ```
     node --version
     npm --version
     ```
   - Você deve ver os números das versões instaladas

### Instalando o Claude Code CLI

O Claude Code é uma ferramenta de linha de comando que permite interagir com o Claude diretamente do seu computador, sem precisar abrir um navegador.

1. **Abra o terminal ou prompt de comando**
   - No Windows: pressione a tecla Windows + R, digite "cmd" e pressione Enter
   - No Mac: abra o aplicativo Terminal (usando Spotlight - Command + Espaço, digite "Terminal")

2. **Instale o pacote Claude Code**
   - Digite o seguinte comando:
     ```
     npm install -g @anthropic-ai/claude-code
     ```
   - O que este comando faz:
     - `npm` é o gerenciador de pacotes do Node.js
     - `install` indica que queremos instalar um pacote
     - `-g` significa "global" (instala para todo o computador, não apenas para o projeto atual)
     - `@anthropic-ai/claude-code` é o nome do pacote do Claude Code

3. **Aguarde a instalação**
   - Você verá várias linhas de texto aparecendo durante a instalação
   - Pode levar alguns minutos, dependendo da velocidade da sua internet
   - Aguarde até que o terminal fique disponível para novos comandos

4. **Verifique se a instalação foi bem-sucedida**
   - Digite:
     ```
     claude --version
     ```
   - Você deverá ver o número da versão do Claude Code
   - Se aparecer um erro como "comando não encontrado", tente fechar e reabrir o terminal

5. **Configure sua API Key**
   - Digite:
     ```
     claude auth login
     ```
   - O programa solicitará sua API Key da Anthropic
   - Cole a API Key que você criou na Parte 2 deste tutorial e pressione Enter
   - Se a configuração for bem-sucedida, você verá uma mensagem de confirmação

6. **Teste se está tudo funcionando**
   - Digite:
     ```
     claude ask "Olá, Claude!"
     ```
   - O Claude deve responder com uma saudação
   - Parabéns! O Claude Code está instalado e funcionando corretamente

### Testando o Claude Code

Vamos realizar alguns testes simples para garantir que o Claude Code está funcionando corretamente e para você se familiarizar com os comandos básicos.

1. **Teste uma consulta básica**
   - No terminal ou prompt de comando, digite:
     ```
     claude ask "Qual é a fórmula para calcular a área de um círculo?"
     ```
   - Pressione Enter
   - O Claude irá processar a pergunta e responder com a fórmula (π × r²) e possivelmente algumas explicações adicionais
   - Este é o comando mais básico: `claude ask` seguido de sua pergunta entre aspas

2. **Teste uma consulta com mais contexto**
   - Digite:
     ```
     claude ask "Se eu correr 5 km por dia, 3 vezes por semana, quantos quilômetros vou percorrer em um mês?"
     ```
   - O Claude irá calcular e explicar o resultado
   - Observe como ele pode trabalhar com problemas matemáticos simples

3. **Teste uma consulta com um arquivo de texto**
   - Primeiro, crie um arquivo de texto:
     - No Windows: abra o Bloco de Notas, escreva algum texto e salve como "exemplo.txt" na mesma pasta onde está seu terminal
     - No Mac: abra o TextEdit, escreva algum texto e salve como "exemplo.txt" na mesma pasta onde está seu terminal
   - Depois, no terminal, digite:
     ```
     claude ask "Resuma este arquivo em 3 pontos principais" -f exemplo.txt
     ```
   - O parâmetro `-f` (de "file") indica que estamos enviando um arquivo para o Claude analisar
   - O Claude lerá o arquivo e fornecerá um resumo dos principais pontos

4. **Salvando a resposta em um arquivo**
   - Digite:
     ```
     claude ask "Escreva 5 dicas para economizar energia em casa" -o dicas.txt
     ```
   - O parâmetro `-o` (de "output") salva a resposta em um arquivo
   - Após a execução, você encontrará um arquivo chamado "dicas.txt" com a resposta do Claude

5. **Combinando arquivos de entrada e saída**
   - Digite:
     ```
     claude ask "Corrija a gramática deste texto" -f exemplo.txt -o corrigido.txt
     ```
   - Isto enviará o arquivo "exemplo.txt" para o Claude, pedirá para corrigir a gramática e salvará o resultado em "corrigido.txt"
   
Estes são apenas exemplos básicos. O Claude Code tem muitas outras funcionalidades avançadas que você pode explorar à medida que se torna mais familiarizado com a ferramenta.

## Parte 4: Entendendo o MCP (Messages, Chats, and Prompts)

### O que é MCP?

MCP no contexto da Anthropic e do Claude refere-se a "Messages, Chats, and Prompts" (Mensagens, Conversas e Comandos), que são os três principais métodos de interação com o Claude:

1. **Messages (Mensagens)**
   - Método mais simples de interação
   - Você envia uma única mensagem e recebe uma única resposta
   - Ideal para consultas pontuais ou tarefas isoladas
   - Exemplo: "Qual é a capital da França?"

2. **Chats (Conversas)**
   - Método para interações contínuas
   - Mantém o contexto entre as mensagens
   - Permite conversas naturais com idas e vindas
   - Exemplo: Uma conversa sobre receitas onde você faz várias perguntas relacionadas

3. **Prompts (Comandos)**
   - Instruções específicas que orientam o comportamento do Claude
   - Podem incluir exemplos, formatação desejada ou contexto específico
   - Ideal para tarefas complexas ou personalizadas
   - Exemplo: "Atue como um especialista em marketing e crie uma estratégia para lançamento de produto seguindo estas diretrizes..."

### Como Usar o MCP Efetivamente:

#### Para Mensagens Simples:
- Seja claro e direto
- Faça uma pergunta de cada vez
- Exemplo: "Resuma os benefícios da vitamina D"

#### Para Conversas:
- Comece com contexto claro
- Faça perguntas de acompanhamento
- Refira-se a informações anteriores
- Exemplo: "Estou planejando uma viagem para Portugal" seguido de "Quais cidades devo visitar?" e depois "Qual a melhor época do ano?"

#### Para Comandos Avançados:
- Estruture suas instruções em partes
- Forneça exemplos do resultado desejado
- Especifique o formato, tom ou estilo
- Exemplo:
  ```
  Preciso criar um e-mail para clientes sobre nosso novo produto.
  Detalhes do produto:
  - Nome: SuperGadget X1
  - Preço: R$299
  - Benefícios: economia de tempo, fácil de usar, design moderno
  
  Tom: Amigável mas profissional
  Comprimento: 3 parágrafos curtos
  Deve incluir: chamada para ação no final
  ```

## Parte 5: Trabalhando com Open Strategy Partners (OSP) Marketing Tools

### O que é o OSP Marketing Tools?

O OSP Marketing Tools é uma suíte completa de ferramentas para criação, otimização e posicionamento de conteúdo de marketing técnico baseada nas metodologias comprovadas da [Open Strategy Partners](https://openstrategypartners.com). Este software utiliza o Protocolo de Contexto de Modelo (MCP) que mencionamos anteriormente e pode ser integrado ao Claude para potencializar suas capacidades de marketing.

### Principais Recursos:

1. **Gerador de Mapa de Valor de Produto OSP**
   - Cria taglines eficazes
   - Desenvolve declarações de posicionamento
   - Gera personas com papéis, desafios e necessidades

2. **Gerador de Meta Informações OSP**
   - Títulos de artigos otimizados para SEO
   - Meta descrições com propostas de valor claras
   - URLs amigáveis para mecanismos de busca

3. **Códigos de Edição de Conteúdo OSP**
   - Análise de estrutura narrativa
   - Otimização de fluidez e legibilidade
   - Verificação de escolha de palavras e gramática

4. **Guia de Escrita Técnica OSP**
   - Desenvolvimento de estrutura narrativa
   - Otimização de fluxo
   - Diretrizes de estilo

5. **Guia de SEO On-Page OSP**
   - Otimização de meta conteúdo
   - Aprimoramento da profundidade de conteúdo
   - Implementação técnica de SEO

### Como Instalar e Configurar OSP Marketing Tools para Claude

**Observação importante**: Existem duas formas de configurar o OSP Marketing Tools, dependendo de qual versão do Claude você está usando. Neste tutorial, vamos focar no Claude Code (ferramenta de linha de comando), que é a opção mais flexível e poderosa para uso profissional.

#### Passo 1: Verificar e Instalar os Pré-requisitos

Para usar o OSP Marketing Tools, precisamos instalar algumas ferramentas básicas em seu computador. Vamos configurar tudo passo a passo.

**Para Windows:**

1. **Instale o Python 3.10 ou superior**
   - O Python é uma linguagem de programação que será necessária para executar o OSP Marketing Tools
   - Abra seu navegador e acesse o site oficial: [python.org](https://python.org)
   - Clique em "Downloads" e depois em "Windows"
   - Baixe a versão mais recente (algo como "Python 3.11.X")
   - **IMPORTANTE**: Durante a instalação, marque a caixa "Add Python to PATH" para que o Windows possa encontrar o Python facilmente
   - Clique em "Install Now" e aguarde a instalação ser concluída
   - Para verificar se a instalação foi bem-sucedida:
     - Pressione a tecla Windows + R para abrir o "Executar"
     - Digite "cmd" e pressione Enter para abrir o Prompt de Comando
     - No Prompt de Comando, digite:
       ```
       python --version
       ```
     - Você deverá ver o número da versão do Python (como "Python 3.11.2")

2. **Instale o UV (gerenciador de pacotes Python)**
   - O UV é uma ferramenta que ajuda a instalar outros programas Python de forma mais rápida
   - No Prompt de Comando, digite:
     ```
     pip install --user uv
     ```
   - Pressione Enter e aguarde a instalação ser concluída
   - Para verificar se a instalação foi bem-sucedida, digite:
     ```
     uv --version
     ```
   - Você deverá ver o número da versão do UV

3. **Instale o Node.js**
   - O Node.js é necessário para executar o Claude Code
   - Acesse [nodejs.org](https://nodejs.org/en/)
   - Clique no botão de download da versão LTS (Suporte de Longo Prazo)
   - Execute o arquivo baixado
   - Siga as instruções na tela:
     - Aceite os termos e condições
     - Mantenha as configurações padrão (especialmente "Add to PATH")
     - Clique em "Install" e aguarde
   - Para verificar se a instalação foi bem-sucedida:
     - Abra um novo Prompt de Comando (feche o anterior e abra um novo)
     - Digite:
       ```
       node --version
       ```
     - Você deverá ver o número da versão do Node.js
     - Em seguida, digite:
       ```
       npm --version
       ```
     - Você deverá ver o número da versão do NPM (gerenciador de pacotes do Node.js)

**Para Mac:**

1. **Instale o Homebrew (se ainda não tiver)**
   - O Homebrew é um gerenciador de pacotes que torna mais fácil instalar programas no Mac
   - Abra o aplicativo Terminal (você pode encontrá-lo usando a busca Spotlight - pressione Command + Espaço e digite "Terminal")
   - No Terminal, cole o seguinte comando e pressione Enter:
     ```
     /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
     ```
   - Siga as instruções na tela e digite sua senha quando solicitado
   - Ao final, o Homebrew mostrará alguns comandos adicionais que você pode precisar executar para configurá-lo - execute esses comandos

2. **Instale o Python 3.10 ou superior**
   - Com o Homebrew instalado, agora pode instalar o Python facilmente
   - No Terminal, digite:
     ```
     brew install python
     ```
   - Aguarde a instalação ser concluída
   - Para verificar se a instalação foi bem-sucedida, digite:
     ```
     python3 --version
     ```
   - Você deverá ver o número da versão do Python (como "Python 3.11.2")

3. **Instale o UV (gerenciador de pacotes Python)**
   - Você pode instalar o UV usando o Homebrew ou o pip3
   - Método 1 (usando Homebrew):
     ```
     brew install uv
     ```
   - Método 2 (usando pip3):
     ```
     pip3 install --user uv
     ```
   - Para verificar se a instalação foi bem-sucedida, digite:
     ```
     uv --version
     ```
   - Você deverá ver o número da versão do UV

4. **Instale o Node.js**
   - No Terminal, digite:
     ```
     brew install node
     ```
   - Aguarde a instalação ser concluída
   - Para verificar se a instalação foi bem-sucedida, digite:
     ```
     node --version
     ```
   - Você deverá ver o número da versão do Node.js
   - Em seguida, digite:
     ```
     npm --version
     ```
   - Você deverá ver o número da versão do NPM

#### Passo 2: Configurar o OSP Marketing Tools no Claude Code

Agora que temos todos os pré-requisitos instalados, vamos configurar o OSP Marketing Tools para trabalhar com o Claude Code. O OSP Marketing Tools é uma coleção de ferramentas especializadas que ajudam a criar conteúdo de marketing de alta qualidade.

1. **Verificar a instalação do Claude Code**
   - Antes de começar, vamos confirmar que o Claude Code está instalado corretamente
   - Abra o terminal ou prompt de comando
   - Digite:
     ```
     claude --version
     ```
   - Se você vir o número da versão, significa que está tudo certo para prosseguir

2. **Adicionar o OSP Marketing Tools como servidor MCP**
   - O MCP (Model Context Protocol) é um sistema que permite adicionar funcionalidades extras ao Claude
   - Para adicionar o OSP Marketing Tools, digite o seguinte comando (copie e cole exatamente como está):
     ```
     claude mcp add osp_marketing_tools -s project -- uvx --from git+https://github.com/open-strategy-partners/osp_marketing_tools@main osp_marketing_tools
     ```
   
   - Explicação deste comando para os curiosos:
     - `claude mcp add`: Comando para adicionar um novo servidor MCP
     - `osp_marketing_tools`: Nome que estamos dando a esta ferramenta
     - `-s project`: Define o escopo como o projeto atual
     - `--`: Separa os argumentos do Claude dos argumentos do servidor
     - O restante: Instruções de como baixar e executar o OSP Marketing Tools

3. **Aguarde a instalação**
   - O processo pode levar alguns minutos
   - Você verá várias linhas de texto aparecendo enquanto o sistema baixa e configura a ferramenta
   - Não feche o terminal durante este processo

4. **Verificar se a instalação foi bem-sucedida**
   - Após a conclusão, digite:
     ```
     claude mcp list
     ```
   - Você deverá ver `osp_marketing_tools` na lista de servidores MCP disponíveis
   - Se aparecer na lista, significa que a instalação foi bem-sucedida!

### Como Usar o OSP Marketing Tools

Agora que você instalou e configurou o OSP Marketing Tools, vamos aprender a usá-lo! Esta ferramenta oferece várias funcionalidades poderosas para melhorar seu conteúdo de marketing. Vamos explorar cada uma delas com exemplos práticos.

#### 1. Gerando um Mapa de Valor para seu Produto:

O Mapa de Valor é uma estrutura que ajuda a comunicar claramente o valor do seu produto para diferentes públicos.

**Como usar:**
- Abra o terminal ou prompt de comando
- Digite o comando abaixo, substituindo as informações entre colchetes pelos detalhes do seu produto:

```
claude ask "Generate an OSP value map for [Nome do seu Produto], focusing on [seu público-alvo] with these key features:
- [Característica 1]
- [Característica 2]
- [Característica 3]
- [Característica 4]"
```

**Exemplo prático:**
```
claude ask "Generate an OSP value map for MeuApp, focusing on pequenos empresários with these key features:
- Controle financeiro simplificado
- Emissão de notas fiscais
- Relatórios automáticos
- Integração com bancos"
```

Este comando criará um mapa de valor completo para o seu produto, incluindo:
- Uma tagline atraente
- Declarações de posicionamento
- Personas de usuários
- E muito mais!

#### 2. Criando Meta Informações para SEO:

Esta ferramenta ajuda a otimizar o conteúdo do seu site para mecanismos de busca, criando títulos e descrições eficazes.

**Como usar:**
```
claude ask "Use the OSP meta tool to generate metadata for an article about [seu tópico]. Primary keyword: [palavra-chave principal], audience: [seu público], content type: [tipo de conteúdo]"
```

**Exemplo prático:**
```
claude ask "Use the OSP meta tool to generate metadata for an article about dicas de marketing digital. Primary keyword: 'marketing para pequenas empresas', audience: empreendedores iniciantes, content type: guia básico"
```

O Claude gerará:
- Um título otimizado para SEO
- Uma meta descrição atraente
- Um URL amigável
- E outras recomendações para melhorar o desempenho nos buscadores

#### 3. Analisando e Melhorando Conteúdo Existente:

Esta ferramenta avalia seu conteúdo e sugere melhorias usando os códigos de edição OSP.

**Como usar:**
```
claude ask "Review this technical content using OSP editing codes: [cole seu texto aqui]"
```

**Exemplo prático:**
```
claude ask "Review this technical content using OSP editing codes: Nossa empresa oferece soluções inovadoras para seus problemas. Trabalhamos com tecnologia de ponta. Nossos produtos são os melhores do mercado e você vai adorar."
```

O Claude analisará seu texto e fornecerá recomendações detalhadas sobre:
- Estrutura narrativa
- Fluidez e legibilidade
- Escolha de palavras
- Elementos que podem ser melhorados

#### 4. Criando Conteúdo Técnico de Alta Qualidade:

Esta ferramenta ajuda a criar tutoriais, guias e outros conteúdos técnicos seguindo as melhores práticas.

**Como usar:**
```
claude ask "Apply the OSP writing guide to create a [tipo de documento] about [tópico] for [público-alvo]"
```

**Exemplo prático:**
```
claude ask "Apply the OSP writing guide to create a tutorial about como configurar email marketing para iniciantes em marketing digital"
```

O Claude criará um documento estruturado e detalhado, seguindo as melhores práticas de escrita técnica.

#### Dica Avançada: Salvando o Resultado em um Arquivo

Para salvar a resposta do Claude em um arquivo para uso posterior, adicione `-o nome_do_arquivo.txt` ao final do comando:

```
claude ask "Generate an OSP value map for MeuProduto, focusing on clientes corporativos with these key features:
- Recurso 1
- Recurso 2
- Recurso 3" -o mapa_de_valor.txt
```

Isso salvará toda a resposta no arquivo "mapa_de_valor.txt", que você poderá abrir e editar depois.

### Resolução de Problemas Comuns

Às vezes, podemos encontrar alguns obstáculos ao configurar ou usar o Claude Code e o OSP Marketing Tools. Aqui estão soluções para os problemas mais comuns:

#### 1. "Comando não encontrado" ao executar `claude`

**Problema:** Quando você digita `claude --version` ou qualquer comando do Claude, aparece algo como "comando não encontrado" ou "command not found".

**Soluções:**
- **Verifique a instalação do Node.js**:
  ```
  node --version
  ```
  Se este comando também não funcionar, você precisa reinstalar o Node.js.

- **Reinstale o Claude Code**:
  ```
  npm install -g @anthropic-ai/claude-code
  ```

- **Reinicie o terminal/prompt de comando**: Feche e abra novamente.

- **Windows**: Verifique se o diretório de instalação do npm está no PATH do sistema:
  1. Pressione a tecla Windows + R
  2. Digite "sysdm.cpl" e pressione Enter
  3. Na guia "Avançado", clique em "Variáveis de Ambiente"
  4. Em "Variáveis do Sistema", encontre e selecione "Path" e clique em "Editar"
  5. Verifique se o caminho para os binários do npm está presente (geralmente algo como C:\Users\SeuUsuário\AppData\Roaming\npm)
  6. Se não estiver, clique em "Novo" e adicione-o

#### 2. Erro ao adicionar o servidor MCP do OSP Marketing Tools

**Problema:** Quando você tenta adicionar o OSP Marketing Tools como servidor MCP, ocorre um erro.

**Soluções:**
- **Verifique a instalação do Python e UV**:
  ```
  python --version
  uv --version
  ```
  
- **Tente instalar o UV novamente**:
  ```
  pip install --user --upgrade uv
  ```
  
- **Verifique sua conexão com a internet**: O comando precisa baixar arquivos do GitHub.

- **Tente com permissões de administrador**:
  - Windows: Clique com o botão direito no ícone do Prompt de Comando e selecione "Executar como administrador"
  - Mac: Use `sudo` antes do comando (você precisará digitar sua senha)

#### 3. O OSP Marketing Tools não aparece na lista de servidores MCP

**Problema:** Quando você executa `claude mcp list`, o OSP Marketing Tools não aparece na lista.

**Soluções:**
- **Tente adicionar novamente**:
  ```
  claude mcp add osp_marketing_tools -s project -- uvx --from git+https://github.com/open-strategy-partners/osp_marketing_tools@main osp_marketing_tools
  ```
  
- **Verifique se há erros durante a instalação**: Leia atentamente as mensagens exibidas durante o processo.

- **Verifique o escopo**: O comando acima usa `-s project`, que torna o servidor disponível apenas no diretório atual. Se você estiver em outro diretório, tente usar `-s user` para torná-lo disponível em todo o sistema:
  ```
  claude mcp add osp_marketing_tools -s user -- uvx --from git+https://github.com/open-strategy-partners/osp_marketing_tools@main osp_marketing_tools
  ```

#### 4. O Claude retorna respostas incompletas ou incorretas

**Problema:** O Claude não está fornecendo o tipo de conteúdo que você espera ou está retornando respostas parciais.

**Soluções:**
- **Seja mais específico em seus comandos**: Forneça mais detalhes sobre o que você deseja.

- **Divida tarefas complexas em partes menores**: Em vez de pedir um plano de marketing completo, peça primeiro a análise de público, depois as estratégias, etc.

- **Verifique sua API Key**: Se você está no plano gratuito, pode haver limitações no uso. Considere atualizar para um plano pago se necessário.

- **Experimente um modelo diferente**: Se disponível na sua conta, experimente usar um modelo mais avançado como o Claude 3 Opus:
  ```
  claude ask "sua pergunta" --model claude-3-opus-20240229
  ```

#### 5. Erro "Python não foi encontrado" no Windows

**Problema:** Mesmo após instalar o Python, o sistema não o reconhece.

**Solução:**
- Reinstale o Python e certifique-se de marcar a opção "Add Python to PATH" durante a instalação
- Após a instalação, reinicie o computador para garantir que as alterações no PATH sejam aplicadas

## Recursos Adicionais

- **Documentação Oficial**: https://docs.anthropic.com/
- **Suporte da Anthropic**: https://support.anthropic.com/
- **Blog da Anthropic**: https://www.anthropic.com/blog
- **Repositório OSP Marketing Tools**: https://github.com/open-strategy-partners/osp_marketing_tools
- **Site da Open Strategy Partners**: https://openstrategypartners.com
- **Comunidade**: Procure por grupos no Discord, Reddit ou fóruns dedicados à IA

---

## Glossário de Termos

- **IA**: Inteligência Artificial
- **LLM**: Large Language Model (Modelo de Linguagem de Grande Escala)
- **API**: Application Programming Interface (Interface de Programação de Aplicações)
- **Token**: Unidade básica de texto processada pelo Claude (palavras ou partes de palavras)
- **Prompt**: Instrução ou comando dado ao Claude
- **Fine-tuning**: Processo de personalização de um modelo para necessidades específicas
- **Claude AI**: O assistente de IA desenvolvido pela Anthropic
- **CLI**: Command Line Interface (Interface de Linha de Comando)
- **MCP**: Model Context Protocol (Protocolo de Contexto de Modelo)
- **OSP**: Open Strategy Partners
