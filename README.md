# Ronda Penal 

## Introdução

Este relatório descreve o desenvolvimento de um sistema de gerenciamento de apenados, projetado para facilitar as operações dos policiais de Araranguá. O sistema tem como objetivo centralizar a gestão e o monitoramento de informações relacionadas aos apenados em liberdade condicional. A necessidade desse sistema surgiu devido à demanda por uma gestão mais eficiente e segura das informações dos apenados, permitindo aos policiais um acesso fácil a dados atualizados, a visualização de mapas com a localização dos apenados, e o registro de visitas de forma organizada. Para isso, será desenvolvido um aplicativo móvel, destinado ao uso durante o patrulhamento, onde os policiais poderão acessar as informações e registrar visitas. O sistema contará com autenticação, garantindo segurança e operará sem internet, com dados sendo atualizados quando a viatura retornar ao quartel.

### Integrantes do Projeto
- **Alisson Pereira Ferreira**
- **Andre Luis da Rosa de Lima**
- **Bernardo Pandolfi Costa**
- **Fernando Doqui Futila**

---

## Requisitos do Sistema

### Requisitos Funcionais

**RF_01** - O sistema deve permitir que os policiais se autentiquem com suas credenciais para acessar as informações.

**RF_02** - O sistema deve permitir que os policiais cadastrem e visualizem as informações de apenados.

**RF_03** - O sistema deve permitir que o aplicativo sincronize dados com o servidor no quartel da polícia.

**RF_04** - O aplicativo deve permitir que os policiais visualizem um mapa da região com a localização dos apenados.

**RF_05** - O aplicativo deve permitir visualizar o perfil do apenado e seu grau de perigo.

**RF_06** - O aplicativo deve permitir que os policiais registrem visitas aos apenados.

### Requisitos Não-Funcionais

**RNF_01** - O sistema deve garantir a segurança dos dados, permitindo acesso somente a policiais autenticados.

**RNF_02** - A interface do sistema deve ser intuitiva e fácil de usar.

**RNF_03** - O sistema deve ser compatível com diferentes dispositivos e navegadores.

**RNF_04** - O sistema deve ser escalável para suportar o crescimento de dados no futuro.

**RNF_05** - O sistema deve ser estável e disponível 24/7, já que os policiais podem precisar a qualquer momento.

### Regras de Negócio

**RN_01** - O sistema deve sincronizar dados automaticamente para manter as informações atualizadas.

**RN_02** - A atualização de dados deve ocorrer apenas no quartel da polícia.

**RN_03** - Apenas policiais autorizados e administradores podem acessar os dados dos apenados.

---

## Diagramas

### Diagrama de Caso de Uso

Este diagrama descreve as funcionalidades do sistema e como os usuários interagem com ele. O servidor gerencia dados e autenticação de usuários, enquanto o aplicativo permite que os policiais visualizem informações e registrem visitas aos apenados.

<center>
  <img src='https://github.com/Butewbr/App-Apenados/assets/113950309/d172e92c-d8f2-4159-a2f7-1ee32698a0b0' style="width: 500px;">
</center>

*Figura 1: Diagrama de Caso de Uso.*

### Protótipos de Telas

1. **Login Servidor**  
   <center>
     <img src='https://github.com/Butewbr/App-Apenados/assets/113950309/40efcadf-cfbb-4b86-b303-1d2fb4209022' style="width: 500px;">
   </center>
   
   *Figura 3: Tela de Login do Servidor.*

2. **Banco de Apenados**  
   <center>
     <img src='https://github.com/Butewbr/App-Apenados/assets/113950309/5873ed15-6b21-4526-b8be-9e712c7b65b9' style="width: 500px;">
   </center>
   
   *Figura 4: Tela de Banco de Apenados.*

3. **Perfil do Apenado**  
   <center>
     <img src='https://github.com/Butewbr/App-Apenados/assets/113950309/398efcb7-e82e-433b-b963-8161e9384fbb' style="width: 500px;">
   </center>
   
   *Figura 5: Tela de Perfil do Apenado.*

4. **Cadastro de Apenado**  
   <center>
     <img src='https://github.com/Butewbr/App-Apenados/assets/113950309/a39f4f57-66b7-4a62-b781-baf9e2aa77bb' style="width: 500px;">
   </center>
   
   *Figura 6: Tela de Cadastro de Apenado.*

5. **Cadastro de Policial**  
   <center>
     <img src='https://github.com/Butewbr/App-Apenados/assets/113950309/8a9ebec0-cc3e-4332-9776-62d1242eb506' style="width: 500px;">
   </center>
   
   *Figura 7: Tela de Cadastro de Policial.*

6. **Login no Aplicativo Mobile**  
   <center>
     <img src='https://github.com/Butewbr/App-Apenados/assets/113950309/5d0c8332-4f12-43e3-8f2e-f61ddc24dd8f' style="width: 250px;">
   </center>
   
   *Figura 8: Tela de Login no Aplicativo Mobile.*

### Diagrama de Classe

Este diagrama detalha as classes e suas relações dentro do sistema, como a classe **Servidor**, **Policial**, **Apenado**, **Aplicativo**, **Mapa**, entre outras.

<center>
  <img src='https://github.com/Butewbr/App-Apenados/assets/113950309/e36871b9-1d28-4f75-8e1d-cad1b5226e9f' style="width: 500px;">
</center>

*Figura 9: Diagrama de Classe.*

---

## Modelo de Dados

O modelo de dados descreve as entidades essenciais do sistema e suas interações, incluindo **Pessoa**, **Policial**, **Endereco**, **Crime**, **Apenado**, entre outras.

<center>
  <img src='https://github.com/Butewbr/App-Apenados/assets/113950309/19c3f30d-76c2-4519-8e9b-84429fc5b8d3' style="width: 500px;">
</center>

*Figura 10: Modelo de Dados.*

---

## Requisitos de Hardware

A arquitetura do sistema envolve dispositivos móveis conectados ao servidor central, responsável por gerenciar e sincronizar os dados. O diagrama de hardware abaixo ilustra essa interação.

<center>
  <img src='https://github.com/Butewbr/App-Apenados/assets/113950309/c3d7f868-0886-47c9-89be-4baded54f768' style="width: 500px;">
</center>

*Figura 11: Requisitos de Hardware.*

---

## Tecnologias Utilizadas

O projeto utilizou uma combinação de tecnologias, incluindo **PostgreSQL**, **Flask**, **Node.js**, **ReactJS**, **Material UI**, **Styled Components**, **MapLibre**, e **GitHub**, para garantir uma solução eficiente e robusta.

---

## Possíveis Erros

Erros comuns incluem falhas de conexão ou problemas com versões desatualizadas das tecnologias. Recomenda-se garantir as versões adequadas e instalar extensões específicas, como o **React Native Tools** no Visual Studio Code.

---

## Conclusão

O desenvolvimento deste projeto foi uma experiência rica que nos proporcionou uma compreensão profunda das tecnologias envolvidas. A solução criada atende às necessidades dos policiais de Araranguá, com um sistema seguro e eficiente para o gerenciamento de apenados. Continuaremos a aprimorar o sistema, incluindo novas funcionalidades, como a listagem de PMs, notificações de visitas e melhorias na interface.
