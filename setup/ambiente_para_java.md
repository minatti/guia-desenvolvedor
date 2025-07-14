# Guia de Configuração do Ambiente de Desenvolvimento Java no Debian

Este guia detalha o processo de configuração de um ambiente de desenvolvimento Java robusto em sistemas Debian, cobrindo a instalação das ferramentas essenciais e o setup da IDE IntelliJ IDEA.

---

## 1. Resumo das Ferramentas Essenciais

Para um desenvolvimento Java eficiente, as seguintes ferramentas são indispensáveis:

### 1.1. Java Development Kit (JDK)

* **Função:** O JDK é o kit de desenvolvimento fundamental para Java. Ele inclui o compilador (`javac`), que transforma seu código-fonte Java em bytecode executável, e o Java Runtime Environment (JRE), que contém a Java Virtual Machine (JVM) para executar aplicações Java. É a base para qualquer desenvolvimento Java.
* **Analogia:** O "motor" e o "construtor" do seu projeto Java.

### 1.2. Maven ou Gradle

* **Função:** Ferramentas de automação de build e gerenciamento de dependências. Elas automatizam e simplificam processos como a compilação do código, execução de testes, empacotamento da aplicação e, crucialmente, o download e gerenciamento de todas as bibliotecas (dependências) de terceiros que seu projeto possa precisar.
* **Analogia:** O "gerente de projetos" que organiza todos os materiais e etapas da construção.

### 1.3. Git

* **Função:** Um sistema de controle de versão distribuído. O Git permite que você registre todas as alterações no seu código ao longo do tempo, colabore eficientemente com outros desenvolvedores, reverta para versões anteriores do projeto e gerencie diferentes linhas de desenvolvimento (branches). Essencial para trabalho em equipe e rastreabilidade.
* **Analogia:** O "historiador" e o "coordenador de equipe" que registra cada ajuste e permite que vários desenvolvedores trabalhem no mesmo projeto.

### 1.4. IntelliJ IDEA

* **Função:** Uma Integrated Development Environment (IDE) poderosa e inteligente. O IntelliJ IDEA oferece um ambiente completo e otimizado para escrever, depurar e testar seu código Java, com recursos avançados como autocompletar inteligente, refatoração de código, análise estática, integração nativa com Git e ferramentas de build (Maven/Gradle), e um depurador visual robusto.
* **Analogia:** Sua "oficina de alta tecnologia" com todas as ferramentas e assistentes inteligentes para construir e aprimorar seu software.

---

## 2. Guia de Instalação Prático (Debian)

Siga os passos abaixo para configurar seu ambiente de desenvolvimento Java no Debian. Recomenda-se executar um `apt update` e `apt upgrade` antes de iniciar.

### 2.1. Atualizar o Sistema

Abra seu terminal e execute os seguintes comandos para garantir que seu sistema esteja atualizado:

```bash
sudo apt update
sudo apt upgrade -y
```

### 2.2 Instalar o Java Development Kit (JDK)

Recomenda-se as instalações de versões com suporte de longo prazo e estabilidade
17(LTS) ou 21(LTS).

```bash 
sudo apt install openjdk-21-jdk -y
```

Verificação:

Após a instalação, confirme a versão do Java:

```bash
java -version
javac -version
```

2.3. Instalar o Maven

```bash
sudo apt install maven -y
```

Verificação:

Confirme a instalação do Maven:

```bash
mvn -v
```

2.4. Instalar o Git

```bash
sudo apt install git -y
```
Verificação e Configuração Inicial:

Verifique a instalação e configure seu nome de usuário e e-mail (essencial para seus commits no Git):

```bash

git --version
git config --global user.name "Seu Nome Completo"
git config --global user.email "seu.email@example.com"

```


### 2.5. Instalar o IntelliJ IDEA
O IntelliJ IDEA não está nos repositórios padrão do Debian. A forma mais recomendada e prática é via JetBrains Toolbox App.

Opção 1: JetBrains Toolbox App (Recomendado)
O Toolbox App simplifica a instalação, atualização e gerenciamento de todas as suas IDEs da JetBrains.

Baixar o Toolbox App:
Acesse o site oficial e baixe o JetBrains Toolbox App:
https://www.jetbrains.com/pt-br/toolbox-app/download/

Extrair o arquivo:
Abra o terminal e navegue até o diretório onde o arquivo foi baixado (geralmente ~/Downloads). Em seguida, extraia-o:

```bash

tar -xzf jetbrains-toolbox-*.tar.gz
```

Executar o instalador:
Entre no diretório extraído e execute o script:


```bash

cd jetbrains-toolbox-*/
./jetbrains-toolbox
```
Instalar o IntelliJ IDEA:
O Toolbox App será iniciado. Ele pode ser adicionado ao seu menu de aplicativos para fácil acesso. Dentro do Toolbox App, localize o IntelliJ IDEA Community Edition (gratuito e suficiente para a maioria dos casos) ou a Ultimate Edition (paga, com recursos avançados) e clique em "Install".







