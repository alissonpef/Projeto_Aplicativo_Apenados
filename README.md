Segue o **README** final do projeto **Ronda Penal**, formatado no mesmo estilo dos projetos anteriores (como “Sistema de Controle de Acesso a Salas” e “Smart Box”):

---

# **Ronda Penal**

Este projeto descreve o desenvolvimento de um **sistema de gerenciamento de apenados**, projetado para facilitar as operações dos policiais em Araranguá. O objetivo é **centralizar** o monitoramento de apenados em liberdade condicional, fornecendo acesso fácil a dados atualizados, visualização de mapas e registro de visitas de maneira organizada.

> O **Ronda Penal** funciona **sem internet em campo**, sincronizando todos os dados quando o policial retorna à base e se conecta ao **servidor central**.

---

## **Sumário**

1. [Introdução](#introdução)  
2. [Equipe Responsável](#equipe-responsável)  
3. [Requisitos do Sistema](#requisitos-do-sistema)  
4. [Estrutura do Repositório](#estrutura-do-repositório)  
5. [Tecnologias Utilizadas](#tecnologias-utilizadas)  
6. [Como Executar](#como-executar)  
7. [Diagramas](#diagramas)  
8. [Conclusão](#conclusão)

---

## **Introdução**

O **Ronda Penal** foi idealizado para auxiliar os policiais no **gerenciamento de apenados** sob liberdade condicional. O sistema permite:

- **Visualizar mapas** com localização dos apenados.  
- **Registrar visitas** aos apenados e suas ocorrências.  
- **Manter dados atualizados** mesmo sem conexão, com sincronização posterior.

---

## **Equipe Responsável**

- **Alisson Pereira Ferreira**
- **Andre Luis da Rosa de Lima**
- **Bernardo Pandolfi Costa**
- **Fernando Doqui Futila**

**Universidade Federal de Santa Catarina (UFSC) – Campus Araranguá**

---

## **Requisitos do Sistema**

### **Requisitos Funcionais**

1. **RF_01**: Autenticação de policiais para acesso ao sistema.  
2. **RF_02**: Cadastro e visualização de informações dos apenados.  
3. **RF_03**: Sincronização de dados entre o aplicativo (em campo) e o servidor (no quartel).  
4. **RF_04**: Visualização de mapas com a localização dos apenados.  
5. **RF_05**: Exibição de perfil e grau de periculosidade de cada apenado.  
6. **RF_06**: Registro de visitas e histórico de ocorrências.

### **Requisitos Não-Funcionais**

1. **RNF_01**: Garantia de **segurança** dos dados e acesso restrito a usuários autorizados.  
2. **RNF_02**: **Interface intuitiva** e compatível com dispositivos móveis e navegadores.  
3. **RNF_03**: **Escalabilidade** para expansão futura e suporte a um grande número de registros.  
4. **RNF_04**: **Alta disponibilidade** (24/7) e estabilidade do sistema.

### **Regras de Negócio**

1. **RN_01**: Sincronização automática de dados ao retornar ao quartel.  
2. **RN_02**: Somente policiais autorizados e administradores podem atualizar os dados.  
3. **RN_03**: As alterações realizadas no campo ficam armazenadas localmente até a sincronização.

---

## **Estrutura do Repositório**

```bash
/Projeto_Ronda_Penal
├── .vscode            # Configurações do VSCode
├── 2023               # Arquivos e recursos relacionados ao ano projeto no ano de 2-23
├── db                 # Scripts de banco de dados
├── frontend-web       # Código da aplicação web (frontend)
├── login_stuff        # Implementações relacionadas ao sistema de login
├── node_modules       # Dependências do Node.js
├── server             # Código do servidor (backend)
└── web                # Outros arquivos ou recursos do frontend

```

---

## **Tecnologias Utilizadas**

- **PostgreSQL**: Banco de dados relacional para armazenamento de informações dos apenados.  
- **Flask**: Framework Python para desenvolvimento do backend.  
- **React Native**: Desenvolvimento do aplicativo mobile para operações em campo.  
- **MapLibre**: Biblioteca de mapas para visualização das localizações dos apenados.  
- **Material UI**: Criação de interface web responsiva e intuitiva.

---

## **Como Executar**

### 1. Clonar o Repositório

```bash
git clone https://github.com/alissonpef/Projeto_FullStack_Aplicativo_Apenados/tree/main
```

### 2. Configurar o Banco de Dados

1. Crie um banco de dados **PostgreSQL** chamado `ronda_penal`.  
2. Execute o script de criação e população localizado em `Database/schema.sql`:

   ```bash
   psql -U seu_usuario -d ronda_penal -f Database/schema.sql
   ```

### 3. Iniciar o Backend

1. Acesse a pasta `Server` e instale as dependências:

   ```bash
   pip install -r requirements.txt
   ```
2. Inicie o servidor Flask:
   ```bash
   python app.py
   ```
3. O backend estará acessível em `http://localhost:5000`.

### 4. Configurar o App Mobile

1. Acesse a pasta `App_Mobile`.
2. Instale as dependências do React Native:
   ```bash
   npm install
   ```
3. Inicie o aplicativo:
   ```bash
   npm start
   ```
4. Use um emulador ou dispositivo físico para testar o aplicativo mobile.

### 5. Testar o Sistema

- Acesse `http://localhost:5000` para verificar o backend.  
- No aplicativo mobile, faça login e realize cadastros/visitas para simular o fluxo de trabalho offline.  
- Ao retornar à base, verifique a **sincronização** dos dados com o servidor.

---

## **Diagramas**

### **Diagrama de Caso de Uso**

Descreve funcionalidades do sistema e como os usuários (policiais) interagem com as entidades do sistema (aplicativo, servidor, banco de dados).

![Diagrama de Caso de Uso](https://github.com/Butewbr/App-Apenados/assets/113950309/d172e92c-d8f2-4159-a2f7-1ee32698a0b0)

*Figura 1: Diagrama de Caso de Uso.*

### **Protótipos de Telas**

1. **Login Servidor**  
   ![Tela de Login Servidor](https://github.com/Butewbr/App-Apenados/assets/113950309/40efcadf-cfbb-4b86-b303-1d2fb4209022)

2. **Banco de Apenados**  
   ![Banco de Apenados](https://github.com/Butewbr/App-Apenados/assets/113950309/5873ed15-6b21-4526-b8be-9e712c7b65b9)

3. **Perfil do Apenado**  
   ![Perfil do Apenado](https://github.com/Butewbr/App-Apenados/assets/113950309/398efcb7-e82e-433b-b963-8161e9384fbb)

4. **Cadastro de Apenado**  
   ![Cadastro de Apenado](https://github.com/Butewbr/App-Apenados/assets/113950309/a39f4f57-66b7-4a62-b781-baf9e2aa77bb)

5. **Cadastro de Policial**  
   ![Cadastro de Policial](https://github.com/Butewbr/App-Apenados/assets/113950309/8a9ebec0-cc3e-4332-9776-62d1242eb506)

6. **Login no Aplicativo Mobile**  
   ![Login App Mobile](https://github.com/Butewbr/App-Apenados/assets/113950309/5d0c8332-4f12-43e3-8f2e-f61ddc24dd8f)

### **Diagrama de Classe**

![Diagrama de Classe](https://github.com/Butewbr/App-Apenados/assets/113950309/e36871b9-1d28-4f75-8e1d-cad1b5226e9f)

*Figura 9: Diagrama de Classe.*

### **Modelo de Dados**

![Modelo de Dados](https://github.com/Butewbr/App-Apenados/assets/113950309/19c3f30d-76c2-4519-8e9b-84429fc5b8d3)

*Figura 10: Modelo de Dados.*

### **Requisitos de Hardware**

![Requisitos de Hardware](https://github.com/Butewbr/App-Apenados/assets/113950309/c3d7f868-0886-47c9-89be-4baded54f768)

*Figura 11: Diagrama de Hardware.*

---

## **Conclusão**

O **Ronda Penal** é uma **solução integrada** e **segura** para o gerenciamento de apenados em liberdade condicional. A funcionalidade offline permite que policiais atuem em campo mesmo sem conexão, sincronizando dados ao retornar à base. Isso **otimiza** o trabalho policial e **centraliza** informações sensíveis, garantindo **segurança** e **praticidade**. Futuras implementações podem incluir **notificações automáticas**, **relatórios detalhados** e maior integração com sistemas de segurança pública.

---
