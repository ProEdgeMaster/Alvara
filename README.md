<div align="center">

<h1>Alvará</h1>

<p><strong>Assinatura e validação digital de ficheiros DWFX, IFC e PDF para Windows</strong></p>

<p>
  <a href="https://github.com/ProEdgeMaster/Alvara/releases/latest"><img src="https://img.shields.io/github/v/release/ProEdgeMaster/Alvara?label=vers%C3%A3o&color=4C6EF5" alt="Última versão"></a>
  <a href="LICENSE"><img src="https://img.shields.io/badge/licen%C3%A7a-MIT-blue.svg" alt="Licença MIT"></a>
  <img src="https://img.shields.io/badge/plataforma-Windows%2010%2F11%20x64-0078D4?logo=windows&logoColor=white" alt="Windows 10/11 x64">
  <img src="https://img.shields.io/badge/.NET-10-512BD4?logo=dotnet&logoColor=white" alt=".NET 10">
</p>

</div>

---

## O que é

O **Alvará** é uma aplicação desktop gratuita para assinar e validar digitalmente ficheiros de projeto de construção — **DWFX**, **IFC** e **PDF** — em conformidade com o **DL 10/2024**, a **Portaria 71-A/2024** e o **Regulamento eIDAS**.

Suporta múltiplos métodos de assinatura:

| Método | Descrição |
|---|---|
| **Cartão de Cidadão** | Assinatura qualificada via middleware pteid |
| **Certificado PFX** | Ficheiro `.pfx` / `.p12` protegido por palavra-passe |
| **Windows Certificate Store** | Certificados instalados no Windows, incluindo os da app Autenticação.gov |

---

## Funcionalidades

### Formatos suportados

| Formato | Modo de assinatura |
|---|---|
| **DWFX** | Assinatura nativa no pacote (compatível com Autodesk Design Review) ou XAdES-LT + ASiC-S |
| **IFC** | Contentor ASiC-S com XAdES-LT (Carimbo do Tempo + LTV) |
| **PDF** | PAdES com assinatura visível (posicionamento livre por página) ou invisível |
| **DOCX / DOC** | Convertidos automaticamente para PDF antes de assinar |

### Assinatura e validação

- Validação de revogação em tempo real (OCSP/CRL) com resultado imediato
- Relatório de validação em PDF para entrega à Câmara Municipal
- Verificação automática de integridade ao abrir ficheiros
- LTV — incorporação de provas de não revogação para validação futura offline
- TSA configurável — AMA, Multicert, DigitalSign, ou qualquer RFC 3161

### Interface

- Zona de largagem com reconhecimento de todos os formatos suportados
- Indicador de progresso durante a conversão de documentos
- Seletor visível/invisível para assinaturas PDF
- Temas claro e escuro (segue as preferências do sistema)
- Interface disponível em 24 idiomas
- Integração com **Enviar Para** do Explorador de Ficheiros
- Manual do utilizador integrado

### Empresarial

- Registo de auditoria estruturado (ISO 27001 A.8.15)
- Integração SIEM — NDJSON/CLEF, Syslog UDP/TCP, Windows Event Log
- Definições cifradas em repouso (Windows DPAPI)
- Distribuição via MSI / GPO / SCCM

---

## Requisitos

| Componente | Versão |
|---|---|
| Windows | 10 x64 ou superior |
| .NET Windows Desktop Runtime | 10.0.5 — incluído no Setup.exe |
| Software Autenticação.gov | Necessário apenas para assinar com Cartão de Cidadão |

---

## Instalação

### Utilizadores finais

Descarregue o **`Setup.exe`** na [página de releases](../../releases/latest).

O instalador inclui o .NET 10 Desktop Runtime e a opção de instalar o software Autenticação.gov.

### Ambientes empresariais (IT / GPO)

Descarregue o **`MSI`** e distribua via Group Policy ou SCCM:

```cmd
msiexec /i Alvara-x.y.z.msi /qn
```

---

## Conformidade legal

As assinaturas produzidas pelo Alvará utilizam:

- **SHA-256** para todos os digests XAdES e PAdES
- **Carimbos do tempo RFC 3161** de TSA qualificada (AMA por defeito)
- **OCSP/CRL embebidos** para validação a longo prazo (XAdES-LT / PAdES-LT)

Em conformidade com **DL 10/2024**, **Portaria 71-A/2024**, e **eIDAS Art. 26 / Art. 42**.

---

## Licença

Distribuído sob a licença MIT. Consulte o ficheiro [LICENSE](LICENSE) para mais detalhes.

---

<sub><strong>Aviso Legal:</strong> O Alvará é uma ferramenta técnica. O utilizador é o único responsável pela validade jurídica das assinaturas produzidas face à legislação aplicável.</sub>

---

<div align="center">

<br>

Feito em Portugal 🇵🇹 · Gratuito · Licença MIT

<br>

<sub>Se o Alvará te poupou tempo ou uma dor de cabeça na Câmara, considera deixar uma ⭐ no repositório — ajuda outros a encontrá-lo.</sub>

<br>

</div>
