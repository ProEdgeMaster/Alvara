<div align="center">

<h1>Alvará</h1>

<p><strong>Assinatura e validação digital de ficheiros DWFX para Windows</strong></p>

<p>
  <a href="LICENSE"><img src="https://img.shields.io/badge/licen%C3%A7a-MIT-blue.svg" alt="Licença MIT"></a>
  <img src="https://img.shields.io/badge/plataforma-Windows%2010%2F11%20x64-0078D4?logo=windows&logoColor=white" alt="Windows 10/11 x64">
  <img src="https://img.shields.io/badge/.NET-10-512BD4?logo=dotnet&logoColor=white" alt=".NET 10">
</p>

</div>

---

## O que é

O **Alvará** é uma aplicação desktop gratuita para assinar e validar digitalmente ficheiros DWFX (AutoCAD Design Review / Open Packaging Convention) no Windows, com suporte para:

| Método | Descrição |
|---|---|
| **Cartão de Cidadão** | Assinatura qualificada via middleware pteid |
| **Certificado PFX** | Ficheiro `.pfx` / `.p12` protegido por palavra-passe |
| **Windows Certificate Store** | Certificados instalados no Windows, incluindo os da app Autenticação.gov |

A assinatura é incorporada no próprio ficheiro DWFX e é compatível com qualquer leitor que suporte o formato OPC/XPS.

---

## Funcionalidades

- Assinar ficheiros DWFX com Cartão de Cidadão, PFX ou Windows Certificate Store
- Validar assinaturas com verificação de revogação em tempo real (OCSP/CRL)
- Inspecionar certificados de assinatura (sujeito, emissor, validade, número de série)
- Deteção automática de assinatura ao abrir o ficheiro
- Integração com **Enviar Para** do Explorador de Ficheiros
- Entrada por arrastar e largar (*drag & drop*)
- Temas claro e escuro (segue as preferências do sistema)
- Manual do utilizador integrado
- Telemetria anónima opt-in (desativável nas Definições)

---

## Requisitos

| Componente | Versão |
|---|---|
| Windows | 10 x64 ou superior |
| .NET Windows Desktop Runtime | 10.0 — incluído no Setup.exe |
| Software Autenticação.gov | Necessário apenas para assinar com Cartão de Cidadão |

---

## Instalação

### Utilizadores finais

Descarregue o **`Setup.exe`** na [página de releases](../../releases/latest).

O instalador instala automaticamente o .NET 10 Desktop Runtime se necessário, e inclui a opção de instalar o software Autenticação.gov.

### Ambientes empresariais (IT / GPO)

Descarregue o **`MSI`** e distribua via Group Policy ou SCCM:

```
msiexec /i Alvara-x.y.z.msi /qn
```

### Cartão de Cidadão

Instale o middleware pteid em [autenticacao.gov.pt/cc-aplicacao](https://www.autenticacao.gov.pt/cc-aplicacao).

---

## Utilização

### Assinar um ficheiro

1. Abra o ficheiro DWFX — menu **Ficheiro › Abrir DWFX** ou arraste para a janela
2. Selecione o método de assinatura em **Certificado**
3. Clique em **Assinar**

### Validar uma assinatura existente

1. Abra um ficheiro DWFX já assinado
2. Clique no botão **Validar Assinatura**, ou aceda a **Ações › Validar Assinatura**
3. O resultado é apresentado imediatamente — válido, revogado, expirado ou erro de rede

> A validação consulta os servidores OCSP/CRL da autoridade certificadora e requer ligação à internet (timeout: 15 s).

### Send To — assinar a partir do Explorador

Clique com o botão direito num ficheiro `.dwfx` e escolha **Enviar Para › Assinar com Alvará**.

---
## Dependências

| Pacote | Versão | Licença |
|---|---|---|
| [Avalonia UI](https://avaloniaui.net/) | 11.3 | MIT |
| [CommunityToolkit.Mvvm](https://github.com/CommunityToolkit/dotnet) | 8.2 | MIT |
| [Aptabase](https://aptabase.com/) | 0.5 | MIT |
| pteidlib — SDK Cartão de Cidadão | — | AMA / LGPL |

---

## Licença

Distribuído sob a licença **MIT** — consulte [LICENSE](LICENSE) para os termos completos.

O utilizador é o único responsável pela validade legal das assinaturas produzidas face à legislação aplicável (Regulamento eIDAS e legislação nacional).
