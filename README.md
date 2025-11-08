# Laboratório de Conscientização em Segurança Cibernética: Análise e Prevenção de Ataques de Phishing

## ⚠️ Aviso Legal e Ética

Este material é **estritamente para fins educacionais e de conscientização**. O objetivo é demonstrar a mecânica de um ataque de phishing para que profissionais de segurança e estudantes possam **entender, identificar e mitigar** ameaças reais.

**É proibido** o uso deste conhecimento para atividades ilegais, maliciosas ou não autorizadas. A realização de testes de penetração ou simulações de ataque deve ser feita **apenas em ambientes controlados e com permissão expressa** dos proprietários do sistema. A responsabilidade pelo uso indevido é **exclusiva do usuário**.

## 🎯 Objetivo do Laboratório

O principal objetivo deste laboratório é:

1.  **Compreender** o ciclo de vida de um ataque de phishing de credenciais.
2.  **Aprender** a configurar ferramentas comuns de teste de penetração (como o Social-Engineer Toolkit - SET) em um ambiente controlado.
3.  **Desenvolver** a capacidade de identificar os indicadores de um ataque de phishing.
4.  **Reforçar** a importância da **higiene cibernética** e das medidas de defesa.

## 🛠️ Ferramentas e Ambiente

| Ferramenta | Descrição | Propósito no Laboratório |
| :--- | :--- | :--- |
| **Kali Linux** | Distribuição Linux focada em testes de penetração e auditoria de segurança. | Ambiente operacional para a execução das ferramentas de teste. |
| **Social-Engineer Toolkit (SET)** | Framework de código aberto projetado para testes de penetração de engenharia social. | Simulação da criação da página de phishing e do servidor de coleta de credenciais. |
| **Máquina Virtual (VM)** | Ambiente isolado e controlado. | Garantir que a simulação não afete sistemas externos ou reais. |

## ⚙️ Configuração do Cenário de Simulação (Passo a Passo Educacional)

Esta seção detalha os comandos e as etapas para configurar o cenário de simulação. **Lembre-se: Este processo deve ser executado APENAS em sua máquina virtual isolada.**

### 1. Acesso e Inicialização

| Passo | Comando | Descrição |
| :--- | :--- | :--- |
| 1.1 | `sudo su` | Eleva os privilégios para o usuário root (necessário para algumas operações do SET). |
| 1.2 | `setoolkit` | Inicia o Social-Engineer Toolkit. |

### 2. Seleção do Vetor de Ataque

O SET apresentará um menu de opções. Para este laboratório, utilizaremos o vetor de ataque mais comum para coleta de credenciais.

| Opção | Nome | Descrição |
| :--- | :--- | :--- |
| **1** | Social-Engineering Attacks | Seleciona a categoria principal de ataques de engenharia social. |
| **2** | Web Site Attack Vectors | Seleciona o vetor de ataque baseado em websites. |
| **3** | Credential Harvester Attack Method | Seleciona o método de ataque que clona um site e captura as credenciais inseridas. |
| **2** | Site Cloner | Seleciona a opção para clonar um site existente. |

### 3. Configuração de Rede e Alvo

| Passo | Comando/Ação | Descrição |
| :--- | :--- | :--- |
| 3.1 | `ifconfig` ou `ip a` | Obtém o endereço IP da máquina Kali Linux. Este IP será o endereço do servidor de phishing simulado dentro da rede de laboratório. |
| 3.2 | **URL para Clone:** `http://www.facebook.com` | O SET irá clonar a página de login do Facebook para usar como isca. **Importante:** A URL clonada é usada apenas como modelo visual. O tráfego e as credenciais serão processados **localmente** pelo SET. |

## 🛡️ Medidas de Prevenção e Defesa (Foco Principal)

O verdadeiro valor deste laboratório reside na compreensão das defesas. Um ataque de phishing bem-sucedido depende da falha humana e da falta de atenção aos detalhes.

| Indicador de Phishing | Medida de Prevenção |
| :--- | :--- |
| **URL Suspeita** | **Sempre** verifique o endereço na barra do navegador. Procure por erros de digitação (typosquatting), subdomínios estranhos ou falta do cadeado HTTPS. |
| **Solicitação Urgente/Inesperada** | Desconfie de e-mails ou mensagens que criam um senso de urgência ("Sua conta será suspensa!") ou que são inesperadas. |
| **Qualidade do Conteúdo** | Erros de gramática, formatação ruim ou logotipos de baixa resolução são sinais de alerta. |
| **Autenticação de Dois Fatores (2FA)** | Habilite o 2FA em todas as suas contas. Mesmo que um atacante obtenha sua senha, ele não conseguirá acessar a conta sem o segundo fator. |
| **Verificação de Fonte** | Se receber um e-mail suspeito de uma empresa, não clique em links. Em vez disso, abra uma nova aba e digite o endereço oficial da empresa no navegador. |

## 📚 Referências e Leitura Adicional

*   **OWASP Top 10:** Lista das 10 vulnerabilidades de segurança mais críticas para aplicações web.
*   **NIST SP 800-63B:** Diretrizes para Autenticação Digital (inclui recomendações sobre senhas e 2FA).
*   **Artigos sobre Engenharia Social:** Para aprofundar a compreensão sobre a manipulação psicológica por trás do phishing.

---

**Autor:** Manus AI (Adaptado para fins educacionais)
**Data:** Novembro de 2025
**Versão:** 1.0 (Foco Educacional e Ético)
