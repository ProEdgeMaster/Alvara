<div align="center">

<h1>Alvará</h1>

<p><strong>Assinatura e validação digital de ficheiros DWFX e IFC para Windows</strong></p>

<p>
  <a href="LICENSE"><img src="https://img.shields.io/badge/licen%C3%A7a-MIT-blue.svg" alt="Licença MIT"></a>
  <img src="https://img.shields.io/badge/plataforma-Windows%2010%2F11%20x64-0078D4?logo=windows&logoColor=white" alt="Windows 10/11 x64">
  <img src="https://img.shields.io/badge/.NET-10-512BD4?logo=dotnet&logoColor=white" alt=".NET 10">
</p>

</div>

---

## O que é

O **Alvará** é uma aplicação desktop gratuita para assinar e validar digitalmente ficheiros de projeto de construção — **DWFX** e **OpenBIM / IFC** — em conformidade com o **DL 10/2024**, a **Portaria 71-A/2024** e o **Regulamento eIDAS**.

Suporte a múltiplos métodos de assinatura:

| Método | Descrição |
|---|---|
| **Cartão de Cidadão** | Assinatura qualificada via middleware pteid |
| **Certificado PFX** | Ficheiro `.pfx` / `.p12` protegido por palavra-passe |
| **Windows Certificate Store** | Certificados instalados no Windows, incluindo os da app Autenticação.gov |

A aplicação suporta tanto o mecanismo nativo (para DWFX compatível com Autodesk Design Review) como o formato **XAdES-LT + ASiC-S** (para IFC e DWFX, garantindo conformidade legal plena e validação a longo prazo).

---

## Funcionalidades

- **Assinatura DWFX**: Suporte nativo e XAdES+ASiC-S
- **Assinatura OpenBIM / IFC**: encapsulamento ASiC-S com XAdES-LT (Carimbo do Tempo + LTV)
- **Validação**: Verificação de revogação em tempo real (OCSP/CRL) e integridade
- **Conformidade Legal**: Preparado para os requisitos dos portais de licenciamento urbanístico (DL 10/2024)
- **LTV (Long Term Validation)**: Incorporação de provas de não revogação para validação futura offline
- **TSA Configurável**: Suporte para selo temporal AMA / ARTE, Multicert, DigitalSign, etc.
- Integração com **Enviar Para** do Explorador de Ficheiros Windows
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

Descarregue o **`Setup.exe`** na página de releases.

O instalador instala automaticamente o .NET 10 Desktop Runtime se necessário, e inclui a opção de instalar o software Autenticação.gov.

### Ambientes empresariais (IT / GPO)

Descarregue o **`MSI`** e distribua via Group Policy ou SCCM:

```cmd
msiexec /i Alvara-x.y.z.msi /qn
```

## ⚖️ Licença

Este projeto é distribuído sob a licença MIT. Consulte o ficheiro LICENSE para mais detalhes.

---

**Aviso Legal**: O Alvará é uma ferramenta técnica. O utilizador é o único responsável pela validade jurídica das assinaturas produzidas face à legislação aplicável.
