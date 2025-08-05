# 🤖 EmissaoNF - Automação para Emissão de Notas Fiscais

Sistema de automação desenvolvido em Python usando Selenium WebDriver para automatizar o processo de emissão de notas fiscais através de formulários web.

## 📋 Sobre o Projeto

Este projeto consiste em uma automação que:
- Faz login automaticamente em sistema de emissão de NF
- Preenche formulários web com dados de nota fiscal
- Gera arquivos XML com os dados da nota fiscal
- Utiliza interface web simples para coleta de dados

## 🚀 Funcionalidades

- ✅ **Automação de Login**: Login automático no sistema web
- 📝 **Preenchimento Automático**: Preenchimento de todos os campos da NF
- 🌐 **Interface Web**: Formulário HTML para inserção de dados
- 📄 **Geração de XML**: Criação automática de arquivo XML da nota
- 🔄 **Selenium WebDriver**: Automação completa do navegador
- 📱 **Interface Responsiva**: Formulário adaptável para diferentes telas

## 🛠️ Tecnologias Utilizadas

### Backend/Automação
- **Python 3.12.2** - Linguagem principal
- **Selenium WebDriver** - Automação do navegador
- **ChromeDriver** - Driver para Google Chrome
- **webdriver-manager** - Gerenciamento automático do driver

### Frontend
- **HTML5** - Estrutura das páginas
- **CSS3** - Estilização dos formulários
- **JavaScript** - Geração do XML e interatividade

### Arquivos do Projeto
- `emissaoNF.ipynb` - Jupyter Notebook com código de automação
- `login.html` - Página de login do sistema
- `index.html` - Formulário principal de emissão da NF
- `nota.xml` - Arquivo XML gerado automaticamente

## 📋 Pré-requisitos

Antes de executar o projeto, certifique-se de ter instalado:

```bash
- Python 3.12 ou superior
- Google Chrome (versão atualizada)
- Jupyter Notebook ou Jupyter Lab
```

## 🔧 Instalação

### 1. Clone o repositório
```bash
git clone https://github.com/Laviniamadeira/EmissaoNF.git
cd EmissaoNF
```

### 2. Instale as dependências Python
```bash
pip install selenium webdriver-manager
```

### 3. Para usar Jupyter Notebook
```bash
pip install jupyter
```

### 4. Execute o Jupyter Notebook
```bash
jupyter notebook
```

### 5. Abra o arquivo
Navegue até `emissaoNF.ipynb` e execute as células

## 📚 Como Usar

### Método 1: Automação Completa (Jupyter Notebook)

1. **Abra o Jupyter Notebook**:
   ```bash
   jupyter notebook emissaoNF.ipynb
   ```

2. **Execute as células sequencialmente**:
   - A automação irá abrir o Chrome automaticamente
   - Fará login com credenciais pré-definidas
   - Preencherá todos os campos da nota fiscal
   - Clicará no botão "Emitir nota"

### Método 2: Interface Web Manual

1. **Abra o arquivo `login.html`** no navegador
2. **Faça login** (qualquer credencial será aceita)
3. **Preencha o formulário** com os dados da NF:
   - Dados do destinatário
   - Descrição do produto/serviço
   - Valores e quantidades
4. **Clique em "Emitir nota"** para gerar o XML

### Dados de Exemplo (usados na automação)
```
Login: lucas@gmail.com
Senha: 12345
Nome: Lucas
Endereço: Endereço
Bairro: Bairro
Município: Município
CEP: CEP
UF: SP
CNPJ: 11999
Inscrição: olá
Descrição: produto
Quantidade: 10
Valor Unitário: 5
Total: 300
```

## 🏗️ Estrutura do Projeto

```
EmissaoNF/
├── emissaoNF.ipynb      # Script principal de automação
├── login.html           # Página de login
├── index.html           # Formulário de emissão da NF
├── nota.xml             # XML gerado automaticamente
├── .gitattributes       # Configurações do Git
└── README.md            # Este arquivo
```

## 🔍 Detalhes Técnicos

### Selenium WebDriver
O script utiliza:
- **ChromeDriverManager**: Gerencia automaticamente a versão do driver
- **Localização por XPATH**: Para encontrar elementos específicos
- **Localização por NAME**: Para campos de formulário
- **Localização por ID**: Para elementos únicos

### Geração de XML
- JavaScript nativo para criar estrutura XML
- Download automático do arquivo gerado
- Estrutura de dados compatível com padrões fiscais

### Campos Automatizados
- ✅ Nome/Razão Social
- ✅ Endereço completo (Endereço, Bairro, Município, CEP, UF)
- ✅ CNPJ/CPF
- ✅ Inscrição Estadual
- ✅ Descrição do produto/serviço
- ✅ Quantidade, valor unitário e total

## ⚠️ Observações Importantes

### Personalização Necessária
- **Credenciais**: Altere o login e senha no código
- **Dados da NF**: Modifique os dados conforme necessário
- **XPaths**: Podem precisar de ajuste conforme o site alvo

### Limitações
- Funciona especificamente com a estrutura HTML fornecida
- Requer ajustes para diferentes sistemas de NF
- Depende da estabilidade da interface web

## 🛠️ Customização

### Para alterar os dados da automação:
```python
# No arquivo emissaoNF.ipynb, modifique as linhas:
navegador.find_element(By.XPATH,'/html/body/div/form/input[1]').send_keys('SEU_EMAIL')
navegador.find_element(By.XPATH,'/html/body/div/form/input[2]').send_keys('SUA_SENHA')
# ... outros campos
```

### Para usar com outro sistema:
1. Analise a estrutura HTML do sistema alvo
2. Ajuste os XPaths e seletores
3. Modifique os dados conforme necessário

## 🧪 Testando o Projeto

### Teste Manual
1. Execute o notebook célula por célula
2. Observe se o navegador abre corretamente
3. Verifique se todos os campos são preenchidos
4. Confirme a geração do arquivo XML

### Resolução de Problemas
- **Chrome não abre**: Verifique se o Chrome está instalado
- **Elementos não encontrados**: XPaths podem ter mudado
- **Selenium não funciona**: Atualize as dependências

## 🤝 Contribuindo

Contribuições são bem-vindas! Para contribuir:

1. Fork o projeto
2. Crie uma branch para sua feature (`git checkout -b feature/NovaFuncionalidade`)
3. Commit suas mudanças (`git commit -m 'Adiciona nova funcionalidade'`)
4. Push para a branch (`git push origin feature/NovaFuncionalidade`)
5. Abra um Pull Request


## ⚖️ Disclaimer

Este projeto é para fins educacionais e de automação de processos internos. Certifique-se de seguir as regulamentações fiscais aplicáveis ao usar sistemas de emissão de notas fiscais.

---

⭐ **Se este projeto foi útil para você, considere dar uma estrela no repositório!**
