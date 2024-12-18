# 2024.2 Avaliação do 1o período de Sistemas Operacionais

## Informações gerais
- **Objetivo do repositório**: Avaliação do 1o bimestre da Disciplina de sistemas operacionais do curso de TADS do IFRN-CNAT
- **Público alvo**: alunos da disciplina de SO (Sistemas Operacionais) do curso de TADS (Superior em Tecnologia em Análise e Desenvolvimento de Sistemas) no CNAT-IFRN (Instituto Federal de Educação, Ciência e Tecnologia do Rio Grande do Norte - Campus Natal-Central).
- disciplina: **SO** Sistemas Operacionais
- professor: [Leonardo A. Minora](https://github.com/leonardo-minora)

## Avaliação
- **Lembre de fazer o fork deste repositório**
- As questões foram construídas com o auxílio do [copilot](https://copilot.microsoft.com/)

  Aluno: Larissa Samara Xavier Pedro de Lima
  Matricula: 20211014040070

## Respostas 

## Questão 1: Introdução a Sistemas Operacionais
Os sistemas operacionais são responsáveis por gerenciar eficientemente os recursos de hardware e software de um computador, garantindo que eles sejam utilizados de maneira segura e otimizada.

Gerenciamento de Processos:
O sistema operacional organiza a execução de processos através de escalonadores, que determinam qual processo será executado e por quanto tempo. Por exemplo, em um ambiente multitarefa, o SO utiliza algoritmos como Round Robin para distribuir tempo de CPU entre processos, garantindo que todos tenham acesso justo aos recursos.

Gerenciamento de Memória:
Os sistemas operacionais gerenciam a alocação de memória principal (RAM) para processos em execução, utilizando técnicas como paginação e segmentação. Isso garante que diferentes programas não sobrescrevam os dados uns dos outros, evitando falhas no sistema. Por exemplo, ao abrir múltiplas abas em um navegador, cada aba recebe sua própria região de memória virtual.

Gerenciamento de Dispositivos de Entrada e Saída:
O SO usa drivers para intermediar a comunicação entre o hardware e os processos. Ele organiza filas para dispositivos compartilhados, como impressoras, e realiza operações de leitura/escrita de forma eficiente. Por exemplo, ao conectar um pendrive, o SO monta o dispositivo e gerencia as operações de acesso.

Gerenciamento de Arquivos:
Os sistemas operacionais fornecem sistemas de arquivos que organizam e armazenam dados de maneira hierárquica, com suporte a operações como criação, leitura e exclusão de arquivos. Por exemplo, ao salvar um documento, o SO garante que ele seja armazenado em local acessível e seguro, utilizando sistemas como NTFS no Windows ou ext4 no Linux.

## Questão 2: Estrutura de Sistemas Operacionais
Impacto das Arquiteturas nos Custos e na Segurança:

Arquitetura Monolítica:

Complexidade de Implementação e Manutenção: É mais fácil de implementar inicialmente, mas as mudanças tornam-se complexas, pois todos os componentes são interdependentes.
Necessidade de Especialização da Equipe: Menor no início, mas desafios surgem durante a manutenção.
Potenciais Vulnerabilidades de Segurança: Falhas em um módulo podem comprometer o sistema inteiro.
Facilidade de Atualização e Correção de Falhas: Baixa, pois qualquer alteração exige testes extensivos.
Exemplo: Unix tradicional.
Arquitetura Microkernel:

Complexidade de Implementação e Manutenção: Alta na implementação inicial, mas fácil de manter, devido ao isolamento dos módulos.
Necessidade de Especialização da Equipe: Alta, pois exige conhecimento profundo de comunicação interprocessos.
Potenciais Vulnerabilidades de Segurança: Menores, pois falhas são isoladas em componentes separados.
Facilidade de Atualização e Correção de Falhas: Alta, pois módulos podem ser atualizados individualmente.
Exemplo: Minix e QNX.
Arquitetura em Camadas:

Complexidade de Implementação e Manutenção: Moderada, com camadas bem definidas facilitando a organização.
Necessidade de Especialização da Equipe: Moderada, pois o foco pode ser dividido por camadas.
Potenciais Vulnerabilidades de Segurança: Moderadas, pois cada camada pode implementar medidas de segurança específicas.
Facilidade de Atualização e Correção de Falhas: Alta, devido ao isolamento das camadas.
Exemplo: THE Operating System.

## Questão 3: Introdução à Segurança de Sistemas Operacionais
Controle de Acesso:
Benefícios: Garante que apenas usuários autorizados acessem recursos.
Desafios: Pode ser complexo configurar políticas de acesso granular.
Impacto na Usabilidade: Um sistema com controle de acesso inadequado pode dificultar tarefas legítimas, como transferir arquivos entre usuários.
Exemplo: O sistema de permissões do Linux.

Criptografia:
Benefícios: Protege dados sensíveis, garantindo confidencialidade e integridade.
Desafios: Impacta a performance devido ao custo computacional do processo.
Impacto na Usabilidade: Pode causar atrasos em operações intensivas, como transferência de grandes volumes de dados.
Exemplo: O uso de BitLocker no Windows para criptografar discos.

## Questão 4: Custo de Processamento versus Algoritmo Ótimo de Escalonamento
First-Come, First-Served (FCFS):

Vantagens: Simplicidade e baixa sobrecarga de processamento.
Desvantagens: Pode levar ao problema de "convoy effect", onde processos curtos esperam por longos processos.
Exemplo: Aplicável em sistemas de loteria ou tarefas em lote.
Shortest Job Next (SJN):

Vantagens: Reduz o tempo médio de espera.
Desvantagens: Exige previsão precisa do tempo de execução dos processos, o que nem sempre é viável.
Exemplo: Usado em sistemas com tarefas previsíveis, como impressão de documentos de tamanhos conhecidos.
Impacto do Custo de Processamento:
Algoritmos simples, como FCFS, são mais rápidos de executar, enquanto algoritmos mais complexos, como SJN, demandam maior custo de processamento para cálculos, mas oferecem melhores resultados em termos de eficiência.

## Questão 5: Aplicativo em Python vs Aplicativo em C
Python (Interpretado):

Código-fonte é processado por um interpretador como CPython.
As instruções são convertidas para bytecode, que é executado pela máquina virtual Python (PVM).
O kernel do SO gerencia os recursos necessários e comunica-se com os drivers.
As instruções são traduzidas para linguagem de máquina, executada pelo hardware.
C (Compilado):

Código-fonte é compilado para código binário diretamente executável.
O binário interage com o kernel, que gerencia os recursos e a comunicação com os drivers.
O hardware executa o binário diretamente.
Comparação:

Python oferece flexibilidade e facilidade de uso, mas é mais lento devido ao overhead do interpretador.
C é mais eficiente em termos de performance, mas exige maior esforço na codificação e compilação.
Exemplos: Scripts para automação (Python) vs sistemas embarcados (C).
