# 🎂 Sistema de Aniversariantes TCI

Sistema completo e responsivo para exibição dos aniversariantes do mês atual ou de todo o ano, com design moderno baseado na paleta de cores TCI.

---

## 📁 Estrutura de Arquivos

```
sistema-aniversariantes/
├── index.html                # Página principal: aniversariantes do mês atual
├── todos_aniversariantes.html # Página alternativa: exibe todos os aniversariantes do ano
├── aniversariantes.csv       # Planilha modelo com dados
└── README.md                 # Este arquivo de instruções
```

---

## 🚀 Como Usar

### 1. Preparação
- Baixe todos os arquivos e mantenha-os na mesma pasta.
- Não altere os nomes dos arquivos principais, exceto se ajustar no código.

### 2. Configuração da Planilha
- Edite o arquivo `aniversariantes.csv` com seus próprios dados.
- O sistema aceita `.csv` com colunas:

```csv
Nome,Departamento,Cargo,Data,Foto
```

- Foto é opcional. Se não houver, será gerado um avatar com as iniciais.

### 3. Formatos de Data Aceitos
- `DD/MM`
- `DD/MM/AAAA`

---

## 🖥️ Executando o Sistema

### Opção 1: Servidor Local (Recomendado)
```bash
# Python 3
python -m http.server 8000

# Python 2
python -m SimpleHTTPServer 8000

# Node.js
npx http-server
```
Acesse via: `http://localhost:8000`

### Opção 2: Live Server (VS Code)
- Instale a extensão “Live Server”
- Clique com o botão direito no `index.html` ou `todos_aniversariantes.html`
- Selecione “Open with Live Server”

### Opção 3: Servidor Web
- Envie os arquivos para seu servidor
- Acesse via navegador

---

## 🎨 Funcionalidades

### 🗓️ `index.html`
- Mostra **apenas aniversariantes do mês atual**
- Estatísticas com total de aniversariantes
- Design com animações e efeitos hover

### 📋 `todos_aniversariantes.html`
- Lista todos os aniversariantes do ano inteiro
- Ordenação cronológica por data
- Permite visão completa e busca manual

---

## 📝 Exemplo CSV

```csv
Nome,Departamento,Cargo,Data,Foto
João Silva,Tecnologia,Dev,15/07/1990,https://exemplo.com/joao.jpg
Maria Santos,Recursos Humanos,Analista,22/12,
Pedro Costa,Vendas,Gerente,05/03/1985,https://exemplo.com/pedro.jpg
```

---

## 🎨 Cores TCI (CSS)

```css
:root {
  --primary-dark: #2B3D7A;
  --primary-medium: #4A90E2;
  --primary-light: #7BB3F0;
  --accent-aqua: #5DCBDC;
}
```

---

## 🧠 Dicas de Personalização

- Adicione mais arquivos `.csv` no JavaScript:
```js
const nomesPlanilha = [
  'aniversariantes.csv',
  'dados.csv',
  'colaboradores.csv'
];
```

---

## 🐛 Solução de Problemas

| Problema | Solução |
|---------|---------|
| Nenhuma planilha encontrada | Verifique nome do arquivo e use servidor local |
| Colunas obrigatórias não encontradas | Confirme cabeçalhos e ortografia |
| Fotos não aparecem | Use URLs públicas e válidas |
| Datas não aparecem | Use formato DD/MM ou DD/MM/AAAA |

---

## 📞 Suporte

- Leia este README com atenção
- Teste com o arquivo `aniversariantes.csv` fornecido
- Verifique erros no console do navegador (`F12`)

---

## ✅ Pronto para Usar

O sistema está funcional com dados de exemplo. Basta abrir localmente com servidor e personalizar como quiser!

**Versão**: 1.0  
**Compatibilidade**: Navegadores modernos  
**Licença**: Uso interno
