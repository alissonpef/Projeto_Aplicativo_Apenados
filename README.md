# Ronda Penal

## 📝 Introdução

Este projeto descreve o desenvolvimento de um **sistema de gerenciamento de apenados**, projetado para facilitar as operações dos policiais de Araranguá. O objetivo é centralizar a gestão e o monitoramento de informações relacionadas aos apenados em liberdade condicional. O sistema oferece aos policiais acesso fácil a dados atualizados, visualização de mapas com a localização dos apenados e registro de visitas de forma organizada.

O aplicativo opera sem internet e sincroniza os dados com o servidor central ao retornar à base.

---

## 👥 Integrantes do Projeto

- **Alisson Pereira Ferreira**
- **Andre Luis da Rosa de Lima**
- **Bernardo Pandolfi Costa**
- **Fernando Doqui Futila**

**Universidade Federal de Santa Catarina (UFSC)**  
**Campus Araranguá**

---

## 🔑 Requisitos do Sistema

### Funcionais

- **RF_01:** Autenticação de policiais para acesso ao sistema.
- **RF_02:** Cadastro e visualização de informações dos apenados.
- **RF_03:** Sincronização de dados entre o aplicativo e o servidor no quartel.
- **RF_04:** Visualização de mapas com a localização dos apenados.
- **RF_05:** Exibição de perfil e grau de perigo do apenado.
- **RF_06:** Registro de visitas aos apenados.

### Não-Funcionais

- **RNF_01:** Garantia de segurança dos dados com acesso restrito.
- **RNF_02:** Interface intuitiva e responsiva.
- **RNF_03:** Compatibilidade com dispositivos móveis e navegadores.
- **RNF_04:** Escalabilidade para expansão futura.
- **RNF_05:** Estabilidade e disponibilidade 24/7.

### Regras de Negócio

- **RN_01:** Sincronização automática de dados.
- **RN_02:** Atualização de dados apenas na base.
- **RN_03:** Acesso aos dados restrito a policiais autorizados e administradores.

---

## 📂 Estrutura do Repositório

- **/App_Mobile:** Código do aplicativo mobile para operações em campo.
- **/Server:** Backend para autenticação, sincronização e gerenciamento de dados.
- **/Database:** Scripts SQL para criação e população do banco de dados.

---

## 🚀 Tecnologias Utilizadas

- **PostgreSQL**: Banco de dados relacional.
- **Flask**: Framework para desenvolvimento do backend.
- **React Native**: Criação do aplicativo mobile.
- **MapLibre**: Biblioteca para visualização de mapas.
- **Material UI**: Interface web intuitiva e responsiva.

---

## 🛠️ Como Executar

### 1. Clonar o Repositório

```bash
git clone https://github.com/alissonpef/Projeto_Aplicativo_Apenados.git
```

### 2. Configurar o Banco de Dados

- Crie um banco de dados PostgreSQL chamado `ronda_penal`.
- Execute o script de criação e população localizado em `Database/schema.sql`:

```bash
psql -U seu_usuario -d ronda_penal -f Database/schema.sql
```

### 3. Iniciar o Backend

- Instale as dependências do servidor:

```bash
pip install -r Server/requirements.txt
```

- Inicie o servidor Flask:

```bash
python Server/app.py
```

### 4. Configurar o App Mobile

- Navegue até o diretório `App_Mobile`.
- Instale as dependências do React Native:

```bash
npm install
```

- Inicie o aplicativo:

```bash
npm start
```

### 5. Testar o Sistema

- Abra o navegador e acesse o backend em `http://localhost:5000`.
- Utilize um emulador ou dispositivo físico para testar o aplicativo mobile.

---

## 📊 Diagramas

### Diagrama de Caso de Uso

Este diagrama descreve as funcionalidades do sistema e como os usuários interagem com ele. O servidor gerencia dados e autenticação de usuários, enquanto o aplicativo permite que os policiais visualizem informações e registrem visitas aos apenados.

<center>
  <img src='https://github.com/Butewbr/App-Apenados/assets/113950309/d172e92c-d8f2-4159-a2f7-1ee32698a0b0' style="width: 500px;">
</center>

*Figura 1: Diagrama de Caso de Uso.*

### 📊 Protótipos de Telas

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

### 📊 Diagrama de Classe

Este diagrama detalha as classes e suas relações dentro do sistema, como a classe **Servidor**, **Policial**, **Apenado**, **Aplicativo**, **Mapa**, entre outras.

<center>
  <img src='https://github.com/Butewbr/App-Apenados/assets/113950309/e36871b9-1d28-4f75-8e1d-cad1b5226e9f' style="width: 500px;">
</center>

*Figura 9: Diagrama de Classe.*

---

## 📊 Modelo de Dados

O modelo de dados descreve as entidades essenciais do sistema e suas interações, incluindo **Pessoa**, **Policial**, **Endereco**, **Crime**, **Apenado**, entre outras.

<center>
  <img src='https://github.com/Butewbr/App-Apenados/assets/113950309/19c3f30d-76c2-4519-8e9b-84429fc5b8d3' style="width: 500px;">
</center>

*Figura 10: Modelo de Dados.*

---

## 📊 Requisitos de Hardware

A arquitetura do sistema envolve dispositivos móveis conectados ao servidor central, responsável por gerenciar e sincronizar os dados. O diagrama de hardware abaixo ilustra essa interação.

<center>
  <img src='https://github.com/Butewbr/App-Apenados/assets/113950309/c3d7f868-0886-47c9-89be-4baded54f768' style="width: 500px;">
</center>

*Figura 11: Requisitos de Hardware.*

---

---

## 🌟 Conclusão

O **Ronda Penal** é uma solução integrada e segura para o gerenciamento de apenados em liberdade condicional. Com funcionalidades de mapa, perfis de apenados e registro de visitas, o sistema otimiza o trabalho dos policiais, garantindo segurança e organização. Futuramente, serão adicionadas funcionalidades como notificações automáticas e relatórios detalhados.

---

