Automação com Selenium e Preenchimento de Formulários

Este projeto é uma aplicação em Python que automatiza o preenchimento de formulários em um site utilizando dados provenientes de planilhas Excel. A automação é feita com a biblioteca Selenium, enquanto os dados são manipulados com OpenPyXL e Datetime.

📋 Funcionalidades

Login Automático: Insere as credenciais e autentica no site.
Preenchimento de Formulários: Lê os dados de planilhas e insere nos campos do formulário no site.
Formatação de Dados: Trata datas e valores monetários antes de enviar para o site.
Execução Headless: Suporte para execução do navegador sem interface gráfica.

📂 Estrutura do Projeto
.
├── main.py            # Código principal da aplicação

├── A RECEBER 1.xlsx   # Planilha de entrada (opcional)

├── TRANSFERENCIA 1.xlsx # Planilha de entrada com os dados a serem enviados

└── README.md          # Documentação do projeto

🔧 Tecnologias Utilizadas
* Python 3.10+
* Selenium
* OpenPyXL
* Pandas (não diretamente usado no código atual, mas disponível)
* WebDriver Chrome
  
🚀 Como Executar o Projeto
Pré-requisitos
1- Ter o Python instalado.
2- Instalar os pacotes necessários:
    pip install selenium openpyxl pandas
3- Fazer o download do ChromeDriver correspondente à versão do seu navegador e adicioná-lo ao PATH do sistema.

Execução
1- Clone este repositório:
  git clone https://github.com/seuusuario/nome-do-repositorio.git
  cd nome-do-repositorio
  
2- Certifique-se de ter as planilhas A RECEBER 1.xlsx e TRANSFERENCIA 1.xlsx na mesma pasta que o arquivo principal.
3- Execute o script:
    python main.py
    
⚙️ Configuração do Código
* URL do site: Substitua "SEU_SITE_AQUI" na função main() pela URL do site que será automatizado.
* Credenciais de Login: Substitua os valores de user e password pela sua conta.
* Planilhas: Certifique-se de que os dados nas colunas estão organizados da seguinte forma:
  * Coluna A: Proprietário
  * Coluna B: Devedor
  * Coluna C: Descrição
  * Colunas D e E: Datas (Emissão e Vencimento)
  * Coluna F: Valor Bruto
  * Colunas I a L: Outras informações como plano de contas, unidade de custeio, conta corrente, etc.

📝 Melhorias Futuras
* Adicionar suporte para múltiplas linhas de entrada.
* Implementar tratamento de erros mais robusto.
* Modularizar o código para maior reutilização.
* Adicionar suporte para logs detalhados das operações realizadas.

🛠️ Contribuição
1- Faça um fork do repositório.
2- Crie sua branch para novas funcionalidades:
  git checkout -b minha-nova-funcionalidade
3- Faça o commit das suas alterações:
  git commit -m "Adiciona nova funcionalidade"
4- Envie suas alterações:
  git push origin minha-nova-funcionalidade
5- Abra um Pull Request.
