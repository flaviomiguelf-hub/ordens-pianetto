# 📦 Sistema de Ordens de Coleta — Pianetto Transportes e Logística

## Sobre o Projeto

Sistema web para criação, gerenciamento e histórico das **Ordens de Coleta** da Pianetto Transportes e Logística. Desenvolvido para uso no navegador Chrome, com suporte a impressão/PDF e banco de dados persistente.

---

## 📁 Estrutura de Arquivos

```
index.html          → Formulário de criação da Ordem de Coleta
historico.html      → Painel de histórico com filtros
print.html          → Página de impressão/PDF da ordem
images/
  logo.png          → Logo da Pianetto Transportes
README.md           → Este arquivo
```

---

## ✅ Funcionalidades Implementadas

- **Campo PEDIDO** editável com sugestão automática (`PEDIDO-2026-0001`)
- **Campo O.C** com numeração sequencial automática (`OC-2026-0001`)
- **Data de emissão** preenchida automaticamente com a data de hoje
- **Cálculo automático** de Total Frete e Saldo a Pagar
- **Máscaras** de CPF e celular
- **Salvar no histórico** (banco de dados persistente)
- **Gerar PDF / Imprimir** (layout A4)
- **Duplicar ordem** com nova O.C automática e bloqueio de campos sensíveis
- **Painel de histórico** com filtros por data, status e busca textual
- **Exportar CSV** do histórico filtrado
- **Botão PDF** direto no histórico para reimprimir qualquer ordem
- **Logo da Pianetto** no cabeçalho, rodapé e impressão
- **Status da ordem**: Pendente, Em Transporte, Entregue, Cancelada

---

## 🚀 Como Subir no GitHub Pages

### Passo 1 — Criar repositório no GitHub
1. Acesse [github.com/new](https://github.com/new)
2. Nomeie o repositório (ex: `pianetto-ordens`)
3. Defina como **Público** (necessário para GitHub Pages grátis)
4. Clique em **Create repository**

### Passo 2 — Fazer upload dos arquivos
1. No repositório criado, clique em **Add file → Upload files**
2. Arraste os seguintes arquivos:
   - `index.html`
   - `historico.html`
   - `print.html`
   - `README.md`
3. Crie a pasta `images/` e suba o arquivo `logo.png` dentro dela
4. Clique em **Commit changes**

### Passo 3 — Ativar GitHub Pages
1. Vá em **Settings → Pages**
2. Em **Source**, selecione: **Deploy from a branch**
3. Branch: **main** (ou **master**) | Pasta: **/ (root)**
4. Clique em **Save**
5. Aguarde 2-3 minutos

### Passo 4 — Acessar o link
Após ativado, seu link será:
```
https://SEU_USUARIO.github.io/pianetto-ordens/
```

---

## ⚠️ Importante sobre o Banco de Dados

O banco de dados (`tables/ordens`) **funciona apenas quando o sistema está publicado na plataforma Genspark**.

No GitHub Pages (apenas arquivos estáticos), o histórico **não funcionará** porque o GitHub não oferece backend.

**Recomendação:**
- Use a **plataforma Genspark** (aba Publish) para uso com histórico completo
- Use o **GitHub** apenas para **backup e versionamento** dos arquivos

---

## 📋 Páginas e Rotas

| Página | URL | Descrição |
|---|---|---|
| Nova Ordem | `/index.html` | Formulário de criação |
| Histórico | `/historico.html` | Painel com filtros |
| Impressão/PDF | `/print.html?id=ID` | Visualização para impressão |

---

## 🗄️ Modelo de Dados (tabela `ordens`)

| Campo | Tipo | Descrição |
|---|---|---|
| `oc` | text | Número da O.C (automático) |
| `pedido` | text | Número do pedido (editável) |
| `dataEmissao` | text | Data de emissão |
| `status` | text | Pendente / Em Transporte / Entregue / Cancelada |
| `remetente` | text | Nome do remetente |
| `cidadeOrigem` | text | Cidade de origem |
| `recebedor` | text | Nome do recebedor |
| `destino` | text | Cidade de destino |
| `mercadoria` | text | Tipo de mercadoria |
| `pesoBruto` | text | Peso em kg |
| `modVeiculo` | text | Modalidade do veículo |
| `terminal` | text | Terminal de origem |
| `dataAgend` | text | Data de agendamento |
| `placaCav` | text | Placa do cavalo |
| `placaCar1` | text | Placa carreta 1 |
| `dolly` | text | Placa dolly |
| `placaCar3` | text | Placa carreta 3 |
| `ufVeiculo` | text | UF do veículo |
| `nomeMotorista` | text | Nome do motorista |
| `celularMotorista` | text | Celular do motorista |
| `cpfMotorista` | text | CPF do motorista |
| `rgMotorista` | text | RG do motorista |
| `cnhMotorista` | text | CNH do motorista |
| `localColeta` | text | Local de coleta |
| `observacoes` | text | Observações |
| `valorTon` | text | Valor por tonelada |
| `pedagio` | text | Valor do pedágio |
| `adiantamento` | text | Adiantamento |
| `totalFrete` | text | Total calculado |
| `saldoPagar` | text | Saldo a pagar |
| `assinaturaMotorista` | text | Nome na assinatura do motorista |
| `assinaturaAnalista` | text | Nome do analista |

---

## 📞 Informações da Empresa

**Pianetto Transportes e Logística**  
CNPJ: 43.976.512/0001-09 | INSC. EST: 20.101.161-1  
ROD. BR 060 KM 388 SALA 139 — RIO VERDE/GO  
E-mail: comercial.goianesia@pianettotransportes.com.br
