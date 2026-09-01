# 📋 Minha Rota

## 1. A Empresa

* **Nome da empresa:** Minha Rota.
* **Segmento de atuação:** Software B2B para Mobilidade e Logística Corporativa.
* **Missão:** Modernizar a gestão de transporte fretado, substituindo controles manuais inseguros por uma plataforma ágil e confiável.
* **Visão:** Ser a plataforma de referência em gestão de fretamento corporativo, transformando a mobilidade B2B por meio da inovação, eficiência operacional e conectividade em tempo real.
* **Valores:** Inovação, Eficiência Operacional, Transparência, Foco no Cliente e Compromisso com a Segurança da Informação.
* **Produtos/serviços:** Plataforma Minha Rota (Painel Web para gestão e App para motoristas).
* **Clientes:** Transportadoras parceiras e setores de RH de empresas contratantes.
* **Fornecedores e parceiros:** Provedores de nuvem para hospedagem do banco de dados e serviços de mapas/geolocalização.
* **Organograma:** 
  * Diretoria
  * Equipe de Desenvolvimento (Web, Mobile e Dados)
  * Suporte Técnico
* **Principais processos:** Gestão do cadastro de frotas, roteirização de passageiros, fluxo de aprovação de embarques pelo RH e manutenção da segurança do sistema.
* **Objetivos estratégicos:** Substituir as planilhas de Excel das empresas parceiras, agilizar a comunicação entre RH e Transportadora e garantir a conformidade legal no trato das informações dos passageiros.


## 2. O Projeto de Software

* **Quais dados o sistema produz e utiliza:**
  * **Utiliza:** Dados pessoais dos colaboradores (nome, endereço residencial, bairro, empresa e turno) e dados da operação (placas, capacidade dos veículos e motoristas).
  * **Produz:** Listas de embarque diárias estruturadas, rotas com horários e relatórios/logs de quem aprovou ou recusou passageiros.
* **Quem utiliza esses dados:**
  * **Administradores e RH:** Possuem acesso amplo para visualizar, editar e gerenciar as listas e roteiros.
  * **Motoristas:** Possuem acesso restrito; visualizam apenas as informações estritamente necessárias (nome do passageiro e ponto de apanha) para a viagem do dia.
* **Onde os dados são armazenados:**
  * Em um banco de dados relacional em nuvem, protegido por criptografia e com rotinas de backup para evitar perda de informações.
* **Dados sensíveis:**
  * Nomes dos passageiros, endereços residenciais exatos, geolocalização dos pontos de embarque, horários e turnos e empresa vinculada (vínculo empregatício).
* **Problemas relacionados aos dados:**
  * O uso de planilhas (modelo antigo) gera descontrole. Os arquivos circulam livremente por e-mail e WhatsApp, sem rastreabilidade de quem acessou ou alterou os dados, ferindo os princípios de segurança da LGPD.
* **Riscos:**
  * Vazamento de dados pessoais dos colaboradores.
  * Acesso indevido de um motorista ao banco de dados geral (ver passageiros de rotas que não são dele).
  * Falta de base legal ou consentimento adequado entre a empresa (RH) e o colaborador para o compartilhamento de seu endereço com a transportadora.
* **Necessidades do negócio:**
  * **Controle de Acesso:** Implementar níveis de permissão rigorosos para garantir que cada usuário só veja o que precisa (*Princípio da Minimização da LGPD*).
  * **Trilha de Auditoria:** Registrar no banco de dados quem inseriu, alterou ou excluiu informações.
  * **Descarte Seguro:** Criar uma funcionalidade para anonimizar ou excluir permanentemente os dados de um colaborador quando ele for desligado da empresa, respeitando o direito do titular.
