
---

## Guia Rápido de Utilização

### 1. Assinar um projeto
1. Abra o **Alvará**.
2. Arraste o ficheiro **.dwfx** ou **.ifc** para dentro da janela.
3. Escolha o seu certificado (Cartão de Cidadão ou Chave Móvel Digital via Autenticação.gov).
4. Clique em **Assinar**.
5. O ficheiro assinado será guardado na mesma pasta do original.

### 2. Validar uma assinatura
1. Arraste um ficheiro já assinado para a janela.
2. A barra de estado mudará de cor:
   - 🟢 **Verde:** Assinatura Válida e Legal.
   - 🔴 **Vermelho:** Ficheiro alterado ou certificado revogado.
   - 🟡 **Amarelo:** Assinatura tecnicamente válida, mas requer atenção (ex: certificado não qualificado).
3. Clique em **"Ver Detalhes"** para consultar a data e o autor da assinatura.

---

## Requisitos

| Componente | Versão |
msiexec /i Alvara-x.y.z.msi /qn
