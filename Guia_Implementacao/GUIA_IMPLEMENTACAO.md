# 📄 GUIA DE IMPLEMENTAÇÃO: Criação do Azure AI Foundry

Este guia detalha o processo "clique a clique" para a criação do recurso **Azure AI Foundry** (Hub) e o projeto inicial (`StudyBuddy`), que é a base para o Agente AZ-900 Study Buddy.

## Etapa 1: Básico (Basics)

Esta etapa define a localização e a nomenclatura dos recursos[cite: 272].

| Campo | Seleção | Detalhe | Fonte/Print |
| :--- | :--- | :--- | :--- |
| **Subscription** (Assinatura) | **Azure for Students** | Utiliza a assinatura de estudante. | [cite: 21, 195, 284] |
| **Resource group** (Grupo de Recursos) | **RG-AZFG-Challenge** | O grupo de recursos existente | [cite: 22, 196, 287] |
| **Name** (Nome do AI Hub) | **Pamela-Huth-Azure-Frontier-Girls-hub** | Nome do recurso principal | [cite: 23, 199, 291] |
| **Region** (Região) | **Sweden Central** | Região selecionada após falha na implantação em West Europe e East US | [cite: 145, 203] |
| **Default project name** (Nome do Projeto Padrão) | **StudyBuddy** | Nome do projeto padrão que o Agente utilizará | [cite: 25, 146, 209] |

## Etapa 2: Rede (Network)

Esta etapa define as regras de acesso de entrada (Inbound Access).

* **Inbound Access** (Acesso de Entrada): Foi selecionada a opção mais permissiva: **"All networks, including the internet, can access this resource"** (Todas as redes, incluindo a internet, podem acessar este recurso).
* **Observação:** Esta configuração foi mantida, pois as APIs de Agentes só suportam injeção de rede para *Standard Agent set-up*, o que não é o foco do desafio.

## Etapa 3: Identidade (Identity)

Esta etapa define como o recurso se autentica em outros serviços do Azure (Managed Identity).

*  **Identity type** (Tipo de Identidade): Foi selecionada a opção **"System assigned"** (Atribuída ao sistema).
*  **Justificativa:** Esta é a opção mais simples, onde o ciclo de vida da identidade é gerenciado pelo próprio Azure e está vinculado ao recurso AI Foundry.

## Etapa 4: Criptografia (Encryption)

Esta etapa define como os dados são criptografados no recurso.

* **Data Encryption** (Criptografia de Dados): A opção padrão **"Microsoft-managed keys"** foi mantida.
* **Alternativa Descartada:** Foi descartada a opção **"Encrypt data using a customer-managed key"** (CMK) para evitar a complexidade desnecessária de configurar um Azure Key Vault.

## Etapa 5: Tags

* **Tags:** Não foram adicionadas Tags, pois não era um requisito obrigatório do desafio.

## Etapa 6: Revisar + Enviar (Review + Submit)

* **Revisão:** Foi realizada uma verificação final dos detalhes da implantação.
* **Implantação:** O botão **"Create"** (Criar) foi acionado.

---

## Resultado da Implantação

* **Status:** A implantação foi concluída com sucesso.
* **Nome da Implantação:** `AlFoundryCreate-20251117221706`.
* **Recursos Criados:** `Pamela-Huth-Azure-Frontier-Girls-hub` (Hub) e `Pamela-Huth-Azure-Frontier-Girls-hub/StudyBuddy` (Projeto/Agente).
* **Localização Final:** A localização final do recurso é **swedencentral**.
* **Próximo Passo:** O Agente `StudyBuddy` foi acessado para a configuração do *System Prompt* e das *Actions* (Tools).
