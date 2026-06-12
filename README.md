# LiftLogic

## 1.Introdução
### 1.1 Propósito do projeto
Este documento especifíca os requisitos funcionais e não funcionais para o Sistema de um Elevador seguindo a norma IEEE 29148:2018

### 1.2 Escopo
O SE permite que usuários do elevador do prédio consigam usar ele de forma segura e organizada. 

### 1.3 Acrônimos
- SE: Sistema de Elevador
- RF : Requisito Funcional
- RNF : Requisito Não Funcional
- RN : Regra de negócio
- Sprint : Uma aula

### Referências
- IEEE 28148:20218 - Engenharia de sistemas e software

## 2. Descrição Geral
### 2.1 Perspectivas do Projeto
O SE será um prompt programado em python rodado em CLI.

### 2.2 Funções principais

- Organização no tráfego de pessoas.
- Mais segurança no trajeto.

## Requisitos Especifícos

### Requisitos Funcionais
**RF-001: Andar Desejado**
**Descrição:** O sesitema deve fornecer uma interface para que possa permitir que o usuário digite o andar que ele deseje ir.
**Critérios de Aceitação**
- []Deve aceitar apenas valores numéricos inteiros no intervalo de 0 (Térreo) a 10.
- []Caso o usuário digite um valor inválido (ex: números negativos, maiores que 10 ou letras), o sistema deve exibir uma mensagem de erro e solicitar a entrada novamente.

**RF-002: Monitorar tudo em tempo real(CLI)**
**Descrição:** Ter uma interface via terminal que mostre a posição exata de cada elevador, quanto do elevador um ou do dois.
**Critérios de Aceitação:**
- [] O painel deve alterar automaticamente a posição do elevador no "painel de controle"
- [] O painel deve exibir claramenta aposição do "Elevador A" e do "Elevador B"

**RF-003: Quantidade de passageiros antes do embarque.**
**Descrição:** Deverá ter uma caixa de reposta para que a pessoa possa digitar quantas pessoas está entrando no elevador, evitando supelotação.
**Critérios de Aceitação:**
- [] O usuário deverá digitar quantas pessoas estará usando o elevador para evitar que o elevador passe do peso ideal.

**RF-004: Alerta Máximo** 
**Descrição:** Caso a RF03 seja descumprida o sistema deverá emitir um alerta.
**Critérios de Avaliação**
- [] Caso o tanto de pessoas seja ultrapassado o sistema deve mostrar um alerta de superlotação e o elevador ficará travado.

**RF-005: Parada de Emergência** 
**Descrição:** Se acontecer algum problema o sistema deverá ter um botão para que o elevador pare automaticamente.
**Critérios de Avaliação**
- [] Deve parar os elevadores e parar no andar mais próximo para que possa ser mais fácil evacuação.

### Regras de Negócio

**RN-001: Controle de Carga Máxima**
**Descrição:** Garantir que a quantidade de passageiros seja aceita pelo sistema, impedindo superlotação ou sobrecarga.
**Critérios de Aceitação:**
- [] Se o número informado no RF03 for maior que a capacidade máxima definida no código, o elevador deve permanecer estático no andar atual.


**RN-002: Elevador mais próximo**
**Descrição:** Para que o tempo de espera fique menor, quando a pessoa chamar o elevador, o sistema deve reconhecer qual elevador está mais próximo e enviar ele para que não haja demora.
**Critérios de Aceitação:**
- [] O sistema deve calcular a distância absoluta de cada elevador até o andar chamado.

**RN-003: Limites do prédio**
**Descrição:** O sistema deve seguir restritamente os limites  arquitetônicos do prédio.
**Critérios de Aceitação:**
- [] [ ] Os elevadores não podem se mover para abaixo do andar 0 (Térreo) e nem acima do 10º andar.


### Requisitos não funcionais

**RNF-001: Interface do Sistema**
**Descrição:** O sistema não tem necessidade de ter uma interface gráica bonita, apenas um ter a função necessária.
**Critérios de Aceitação:**
- [] Apesar de ser um sisema importante ele não deveter uma interface gráfica bonita e sim funcional.

**RNF-002: Estado dos elevadores.**
**Descrição:** Após o desligamento geral do elevador ele deve voltar a posição inicial.
**Critérios de Aceitação:**
- [] Após o desligamento geral o elevador deve voltar a posição inicial ou seja descer ao térreo nnovamente. 
---

## 4. Controle de Versões

### 4.1 Histórico de alterações

| Versão | Data | Autor | Modificação |
|--------|------|-------|-------------|
|1.0 | 2026-03-27 | Álef e João | Versão inicial do documento |
|2.0 | 2026-06-05 | Álef e João | Incrementação do RF-005 e detalhamento nos outros requisitos|
