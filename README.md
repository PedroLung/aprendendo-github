# aprendendo-github

## O que é Git e Github?
Git é um sistema de controle de versão distribuído e de código aberto, essencial para o gerenciamento moderno de código fonte. Desenvolvido por Linus Torvalds em 2005, o Git permite que múltiplos desenvolvedores trabalhem juntos em um projeto sem conflitos, fornecendo ferramentas para rastrear e mesclar mudanças no código de forma eficiente.

Com o Git, cada desenvolvedor trabalha com uma cópia completa do repositório de código, incluindo todo o histórico de alterações. Isso significa que as operações como commits, visualizações de histórico e comparações de mudanças são rápidas e não dependem de uma conexão com um servidor central.

A importância do Git no controle de versão é imensa:

**Histórico Completo e Rastreabilidade:** Cada alteração no código é rastreada, permitindo que os desenvolvedores voltem a versões anteriores se necessário.

**Colaboração Simplificada:** O Git facilita a colaboração entre equipes distribuídas geograficamente, permitindo que todos contribuam com o projeto simultaneamente.

**Branching e Merging:** O Git oferece um sistema robusto para criar ramificações (branches) e mesclar (merge) essas ramificações, possibilitando o desenvolvimento paralelo de funcionalidades.

**Segurança:** Cada commit é criptograficamente assinado, garantindo a integridade do histórico do código.
Por esses motivos e muitos outros, o Git se tornou a ferramenta padrão para controle de versão em projetos de software ao redor do mundo.

## Instalação do Git

### No Windows

**Baixar o Instalador:** Acesse o site oficial do Git em git-scm.com e baixe o instalador para Windows.

**Executar o Instalador:** Abra o arquivo baixado e execute o instalador. Durante a instalação, você pode aceitar as configurações padrão ou personalizar conforme necessário.

**Verificar a Instalação:** Após a instalação, abra o Prompt de Comando ou o Git Bash e digite:
```
git --version
```
* Para verificar se o Git foi instalado corretamente!

### No Linux
A instalação no Linux pode variar dependendo da distribuição. Aqui estão os comandos para algumas das distribuições mais populares:

**Debian/Ubuntu**
* ```sudo apt-get update```
* ```sudo apt-get install git```

**Fedora**
* ```sudo dnf install git```

**Arch Linux**
* ```sudo pacman -S git```

**Verificar a Instalação**
Em qualquer distribuição Linux, você pode verificar a instalação do Git com o seguinte comando:
```
git --version
```
Após a instalação, você estará pronto para começar a usar o Git para controle de versão dos seus projetos!

## Configuração inicial:
* Após a instalação siga os seguintes passos:

1° abra um terminal

2° Siga esses comandos logo abaixo:

  1° Definir seu nome de usuário:
  ```
  git config --global user.name "Seu Nome"
  ```
  2° Definir seu email:
  ```
  git config --global user.email "seuemail@exemple.com"
  ```
OBS: Isso só será necessário uma vez. Após essas configurações você poderá criar os seus repositórios livremente!

## Comandos:
- Criar um Repositório Local:
```
git init
```
- Conectar com o Repositório Online:
```
git remote add origin <URL_do_repositório>
```
- Clonar Repositório:
```
git clone url-do-git
```
- Ver o Status do Git:
```
git status
```
- Trackear os arquivos:
```
git add <nome do arquivo> ou git add .(adicionar tudo)
```
- Retornar arquivos modificados indevidamente
```
git restore <nome do arquivo>
```
- Commit
```
git commit -m "mensagem"
```
- Subir para o github pela primeira vez na branch
```
git push origin nome da branch
```
- Subir as próximas vezes na branch
```
git push
```
- Criar uma branch
```
git branch nomedabranch ou git checkout -b nomedabranch
```
- Definir a branch main do seu projeto:
```
git branch -M nomedabranchprincipal (Normalmente main)
```

- Desfazer algo numa branch:
```
git stash
```
OBS: Caso queira que essas informações vá para alguma branch separada:
- 1° Troque para a branch desejada
- 2° Digite o seguinte comando:
```
git stash pop
```
- Ver as branchs e ver em que branch você se encontra
```
git branch
```
- Fazer um merge

- Obs: Fique na branch que você quer receber os códigos
```
git merge <nome da branch que você quer pegar o código>
```
- pull request
```
git push -u origin nome_da_branch
```
## .gitignore

O arquivo .gitignore é uma ferramenta vital no Git que permite especificar quais arquivos e diretórios devem ser ignorados pelo sistema de controle de versão. Isso significa que as alterações feitas nesses arquivos não serão rastreadas, e eles não aparecerão como pendentes para commit no seu repositório.

## Como Usar o .gitignore

**Criar o Arquivo:** Crie um arquivo chamado `.gitignore` na raiz do seu repositório Git.

**Especificar Regras:** Dentro do arquivo, adicione as regras para os arquivos e diretórios que você deseja ignorar. 

**Por exemplo:**

* Para ignorar um arquivo específico: arquivo_secreto.txt
* Para ignorar todos os arquivos com uma extensão específica: *.log
* Para ignorar todos os arquivos em um diretório específico: diretorio_temporario/
* Para ignorar arquivos exceto um: *.log !importante.log

**Exemplo de .gitignore**
```
# Ignora todos os arquivos .log
*.log

# Ignora um diretório específico
diretorio_temporario/

# Ignora um arquivo específico
config_local.txt

# Não ignora o arquivo importante.log
!importante.log
```

**Dicas Importantes**
**Comentários:** Linhas começando com # são tratadas como comentários e são ignoradas pelo Git.

**Negando Ignorância:** O prefixo ! é usado para negar a regra, ou seja, para incluir arquivos que seriam ignorados.
Padrões Glob: O Git suporta padrões glob para facilitar a especificação de múltiplos arquivos.

Usando o `.gitignore`, você pode manter seu repositório limpo e livre de arquivos desnecessários, como logs, arquivos temporários ou configurações locais que não devem ser compartilhadas com outros desenvolvedores.
