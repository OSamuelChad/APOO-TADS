# Relatório de Levantamento de Requisitos: Projeto CasaSegura

Este documento detalha as diretrizes, funcionalidades e critérios de qualidade para o sistema de gerenciamento doméstico da CPI Corporation

---

## 1. Regras de Negócio (RN)
As Regras de Negócio definem as políticas e restrições operacionais que o sistema deve obedecer para atender aos objetivos da empresa

| ID | Regra de Negócio | Descrição |
| :--- | :--- | :--- |
| **RN01** | **Protocolo de Alerta Crítico** | Ao detectar invasão, incêndio ou riscos ambientais, o sistema deve notificar imediatamente o proprietário ou órgãos de vigilância. |
| **RN02** | **Compatibilidade de Hardware** | A comunicação entre a central e os sensores deve ocorrer obrigatoriamente via protocolo 802.11n. |
| **RN03** | **Continuidade Operacional** | O sistema deve possuir autonomia energética, comutando para bateria reserva em caso de falha na rede elétrica. |
| **RN04** | **Gestão de Privilégios** | O acesso deve ser segmentado por níveis de permissão, impedindo que usuários comuns alterem configurações críticas do administrador. |
| **RN05** | **Segurança de Identidade** | Exigência de autenticação multifator e reconhecimento de identidade por proximidade de dispositivo móvel cadastrado. |
| **RN06** | **Priorização de Tráfego** | Eventos de segurança (alarmes) possuem prioridade de processamento sobre funções de automação (luzes). |

---

## 2. Requisitos Funcionais (RF)
Os Requisitos Funcionais descrevem as ações e comportamentos que o software deve executar para o usuário.

| ID | Funcionalidade | Descrição | Prioridade |
| :--- | :--- | :--- | :--- |
| **RF01** | **Monitoramento de Sensores** | Interface para monitorar sensores de intrusão, fumaça, inundação e monóxido de carbono em tempo real. | Alta |
| **RF02** | **Gestão Remota de Zonas** | Permitir o armamento, desarmamento e reconfiguração de zonas de segurança via ambiente web ou app. | Alta |
| **RF03** | **Controle de Monitoramento de Vídeo** | Visualização de miniaturas de câmeras com suporte a comandos remotos de pan e zoom. | Alta |
| **RF04** | **Automação de Dispositivos** | Controle de iluminação, eletrodomésticos e ajuste remoto de temperatura (climatização). | Média |
| **RF05** | **Simulador de Presença** | Programação de rotinas aleatórias de iluminação para simular atividade humana durante viagens. | Baixa |
| **RF06** | **Configuração Visual da Planta** | Ferramenta interativa para desenhar a planta da residência e posicionar dispositivos via "arrastar e soltar". | Média |
| **RF07** | **Acesso Automatizado** | Desarmamento do alarme e abertura de portões baseado na geolocalização (GPS) do smartphone do usuário. | Média |
| **RF08** | **Notificações de Diagnóstico** | Reportar imediatamente ao usuário qualquer falha de comunicação ou interrupção de energia no hardware. | Alta |

---

## 3. Requisitos Não Funcionais (RNF)
Os Requisitos Não Funcionais especificam as propriedades de qualidade, desempenho e segurança do sistema.

| ID | Categoria | Especificação | Rigor |
| :--- | :--- | :--- | :--- |
| **RNF01** | **Desempenho** | O tempo de resposta entre a ativação de um sensor e o reconhecimento pelo sistema deve ser inferior a 1 segundo. | Obrigatório |
| **RNF02** | **Segurança** | Toda comunicação externa deve ser criptografada, garantindo invulnerabilidade contra intrusões via internet. | Crítico |
| **RNF03** | **Usabilidade** | A interface deve ser autoexplicativa e consistente, eliminando a necessidade de manuais de instrução complexos. | Desejável |
| **RNF04** | **Disponibilidade** | O monitoramento dos sensores deve operar de forma ininterrupta (24/7). | Crítico |
| **RNF05** | **Eficiência** | O aplicativo móvel deve ser otimizado para minimizar o consumo da bateria do dispositivo do usuário. | Obrigatório |
| **RNF06** | **Escalabilidade** | Suporte para múltiplos acessos simultâneos de membros da família com diferentes perfis de visualização. | Obrigatório |
| **RNF07** | **Interface** | O sistema deve ser responsivo e acessível via navegadores web, tablets e smartphones. | Obrigatório |