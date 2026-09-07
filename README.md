# 🏥 Clínica Vitalis — Sistema de Gestão Médica

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)


> Sistema web intuitivo, semântico e responsivo para controle de pacientes, agendamentos, médicos, prontuários e relatórios da **Clínica Vitalis**.

---

## 📖 1. Sobre o Projeto
O **Sistema Clínica Vitalis** é uma aplicação voltada para a gestão e automação do atendimento médico. O projeto integra uma modelagem de banco de dados relacional rigorosa a uma interface web intuitiva, desenvolvida com foco em acessibilidade, semântica HTML5 e layouts responsivos.

---

## 🎯 2. Módulos do Sistema
O sistema é estruturado em 6 módulos fundamentais:
- 👥 **Cadastro de Pacientes:** Gestão de dados pessoais, contatos e histórico.
- 👨‍⚕️ **Cadastro de Médicos:** Registro de profissionais, CRM e especialidades.
- 📅 **Agenda e Agendamento:** Controle de horários e datas com calendário intuitivo.
- 📋 **Prontuário Eletrônico:** Anotações clínicas, sinais vitais e histórico de consultas.
- 💊 **Prescrição Médica:** Emissão de receitas e controle de medicamentos.
- 📊 **Relatórios Clínicos:** Visualização de dados agregados e consultas por período.

---

## 🎨 3. Prototipação e Modelagem (UI/UX)
A fase de prototipação focou na navegabilidade e arquitetura de informação:
* **Telas de Cadastro (CRUD):** Formulários focados na facilidade de preenchimento para Pacientes e Médicos.
* **Fluxo Principal (Transação):** Interface de Agendamento e Tela do Prontuário Médico.
* **Painel de Visualização (Dashboard):** Tela de relatórios e listagens com filtros avançados.

---

## 💻 4. Arquitetura e Tecnologia Front-end
A implementação da interface segue os padrões estritos do HTML5 e CSS3:
- **Semântica HTML5:** Utilização de `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<footer>`, `<aside>` e `<form>`.
- **CSS Grid Layout:** Macro-estruturação dos contêineres principais (menu lateral vs. área de conteúdo).
- **CSS Flexbox:** Alinhamento bidimensional de componentes (cards, botões, itens de menu e formulários).
- **Validação Nativa:** Uso de atributos `required`, `type="email"`, `type="date"`, `min` e `max`.

---

## 🗄️ 5. Banco de Dados (MySQL)
O banco de dados relacional `clinica_vitalis` foi modelado para suportar todas as operações da clínica.

### 📐 Estrutura de Tabelas e Entidades:
* `especialidades`: Registro das áreas médicas.
* `pacientes`: Dados demográficos e contatos dos pacientes.
* `medicos`: Profissionais de saúde vinculados às especialidades.
* `consultas`: Agendamentos e status da consulta.
* `prontuarios`: Registro de leito, sinais vitais, temperatura, SpO2, FC e conduta.
* `prescricoes`: Medicamentos, dosagens e vias de administração.

---

## 🔍 6. Diagnóstico de Integração (Front & Backend)

### 1. Cobertura dos Campos
Os formulários desenhados na UI capturam integralmente todos os campos obrigatórios e opcionais exigidos pelas tabelas (`pacientes`, `medicos`, `consultas`, `prontuarios` e `prescricoes`).

### 2. Mapeamento de Queries e Endpoints Necessários
Para garantir a integridade da aplicação, foram mapeadas as seguintes necessidades adicionais no Backend:
* **Verificação de Disponibilidade:** Query dinâmica para validar se o médico já possui consulta no horário selecionado antes de confirmar o agendamento.
* **Cálculo de Sinais Vitais:** Endpoint para alertar automaticamente alterações de temperatura e pressão arterial no prontuário.
* **Filtros de Relatório:** Queries agregadas com `GROUP BY` e `BETWEEN` para geração de relatórios por período e profissional.

---

## 👥 7. Divisão da Equipe de Desenvolvimento
1. **Modelagem e Integração com Banco:** Estruturação SQL e scripts de banco.
2. **Cadastro de Pacientes:** Interface de registro e gestão de pacientes.
3. **Cadastro de Médicos:** Interface e gerenciamento de médicos e CRM.
4. **Agendamento:** Módulo de calendário e marcação de consultas.
5. **Prontuário Médico:** Interface clínica de anotações e prescrições.
6. **Relatórios e Consultas:** Dashboard e exibição de métricas.
