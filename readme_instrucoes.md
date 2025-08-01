# 🎂 Sistema de Aniversariantes TCI

Sistema completo para exibição dos aniversariantes do mês atual com design moderno seguindo a paleta de cores TCI.

## 📁 Estrutura dos Arquivos

```
sistema-aniversariantes/
├── index.html              # Sistema principal
├── aniversariantes.csv     # Planilha modelo com dados
└── README.md              # Este arquivo de instruções
```

## 🚀 Como Usar

### 1. **Preparação dos Arquivos**
- Baixe todos os arquivos para uma pasta
- Mantenha a estrutura de arquivos conforme mostrada acima

### 2. **Configuração da Planilha**
- O arquivo `aniversariantes.csv` já vem com dados de exemplo
- Para usar seus próprios dados, edite este arquivo ou crie um novo com o mesmo nome
- **Formatos de arquivo aceitos**: `.csv`

### 3. **Estrutura da Planilha**
A planilha deve conter exatamente estas colunas (nesta ordem):

```csv
Nome,Departamento,Cargo,Data,Foto
```

#### Colunas Obrigatórias:
- **Nome**: Nome completo do colaborador
- **Departamento**: Setor/Departamento
- **Cargo**: Função/Cargo
- **Data**: Data de aniversário (formato DD/MM ou DD/MM/AAAA)

#### Coluna Opcional:
- **Foto**: URL da foto do colaborador (deixe em branco se não tiver)

### 4. **Formatos de Data Aceitos**
- `15/07` (dia e mês)
- `15/07/1990` (dia, mês e ano)
- `03/12/1985` (sempre com 2 dígitos para dia e mês)

### 5. **Nomes de Arquivo Suportados**
O sistema busca automaticamente por estes arquivos:
- `aniversariantes.csv` ⭐ (recomendado)
- `dados.csv`
- `colaboradores.csv`
- `funcionarios.csv`
- `pessoas.csv`

## 🖥️ Executando o Sistema

### Opção 1: Servidor Local (Recomendado)
1. Abra o terminal/prompt na pasta do sistema
2. Execute um servidor local:
   - **Python 3**: `python -m http.server 8000`
   - **Python 2**: `python -m SimpleHTTPServer 8000`
   - **Node.js**: `npx http-server`
3. Acesse: `http://localhost:8000`

### Opção 2: Extensão Live Server (VS Code)
1. Instale a extensão "Live Server" no VS Code
2. Clique com botão direito no `index.html`
3. Selecione "Open with Live Server"

### Opção 3: Servidor Web
- Faça upload dos arquivos para seu servidor web
- Acesse via URL do servidor

## 🎨 Características do Sistema

### ✨ Funcionalidades
- **Carregamento Automático**: Busca e carrega a planilha automaticamente
- **Responsivo**: Funciona em desktop, tablet e mobile
- **Fotos Automáticas**: Se não houver foto, gera avatar com iniciais
- **Ordenação**: Aniversariantes ordenados por dia do mês
- **Estatísticas**: Mostra total de colaboradores e aniversariantes do mês
- **Design Moderno**: Interface limpa com paleta TCI

### 🎯 Exibição
- Mostra apenas os aniversariantes do **mês atual**
- Cards elegantes com foto, nome, departamento, cargo e data
- Animações suaves e efeitos hover
- Indicador visual quando não há aniversariantes no mês

## 📝 Exemplo de Dados CSV

```csv
Nome,Departamento,Cargo,Data,Foto
João Silva,Tecnologia da Informação,Desenvolvedor,15/07/1990,https://exemplo.com/foto.jpg
Maria Santos,Recursos Humanos,Analista,22/12,
Pedro Costa,Vendas,Gerente,05/03/1985,https://exemplo.com/pedro.jpg
```

## 🔧 Personalização

### Alterando Cores
As cores TCI estão definidas no CSS nas variáveis:
```css
:root {
    --primary-dark: #2B3D7A;
    --primary-medium: #4A90E2;
    --primary-light: #7BB3F0;
    --accent-aqua: #5DCBDC;
    /* ... */
}
```

### Adicionando Mais Nomes de Arquivo
No JavaScript, edite o array `nomesPlanilha`:
```javascript
const nomesPlanilha = [
    'aniversariantes.csv',
    'dados.csv',
    'seu-arquivo.csv'  // Adicione aqui
];
```

## 🐛 Solução de Problemas

### Problema: "Nenhuma planilha encontrada"
**Soluções:**
- Verifique se o arquivo CSV está na mesma pasta do HTML
- Confirme se o nome do arquivo está na lista suportada
- Use um servidor local (não abra direto no navegador)

### Problema: "Colunas obrigatórias não encontradas"
**Soluções:**
- Verifique se as colunas estão nomeadas corretamente: Nome, Departamento, Cargo, Data
- Certifique-se de que a primeira linha é o cabeçalho
- Verifique se não há caracteres especiais nos nomes das colunas

### Problema: Fotos não aparecem
**Soluções:**
- Use URLs completas (https://...)
- Certifique-se de que as imagens são acessíveis publicamente
- Se vazio, o sistema gerará automaticamente um avatar com iniciais

### Problema: Datas não aparecem corretamente
**Soluções:**
- Use formato DD/MM ou DD/MM/AAAA
- Exemplos corretos: 15/07, 03/12/1990
- Evite formatos como 15-07 ou 2023/07/15

## 📞 Suporte

Para dúvidas ou problemas:
1. Verifique se seguiu todas as instruções
2. Confira os exemplos fornecidos
3. Teste com a planilha modelo incluída
4. Verifique o console do navegador (F12) para erros

## 🎉 Pronto para Usar!

O sistema já vem com dados de exemplo e está pronto para uso. Basta abrir em um servidor local e personalizar com seus dados!

---

**Versão**: 1.0  
**Compatibilidade**: Todos os navegadores modernos  
**Licença**: Uso interno