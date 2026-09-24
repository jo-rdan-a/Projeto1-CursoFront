# 🚀 Guia Rápido de Git e GitHub: Da Configuração ao Pull Request

Guia prático para consulta rápida de comandos essenciais, fluxo de trabalho e boas práticas de versionamento.

---

## 1. Configuração Global de Usuário

> **Para que serve:** Assina todos os commits no computador com a sua identidade para que o Git e o GitHub registrem a autoria das alterações. Executado apenas uma vez na máquina.

```bash
# Define o nome público que aparecerá nos commits
git config --global user.name "Seu Nome"

# Define o e-mail vinculado à sua conta do GitHub
git config --global user.email "seu_email@exemplo.com"

# Inicializa o repositório local (cria a pasta oculta .git)
git init

# Garante que a branch atual se chama 'main'
git branch -M main

# Cria um arquivo inicial de documentação
echo "# Meu Primeiro App" > README.md

# Verifica o estado dos arquivos (aparecerão em vermelho/não rastreados)
git status

# Conecta o repositório local ao repositório remoto criado no GitHub
git remote add origin [https://github.com/seu-usuario/nome-do-repositorio.git]

# Move os arquivos para a área de preparo (Staging Area)
git add .

# Grava permanentemente o snapshot com uma mensagem descritiva
git commit -m "feat: commit inicial do projeto"

# Envia para a nuvem (-u define o rastreamento padrão para os próximos envios)
git push -u origin main


# Baixa o repositório completo com todo o histórico de versões
git clone [https://github.com/seu-usuario/nome-do-repositorio.git]


# 1. Prepara todos os arquivos modificados
git add .

# 2. Registra o commit com uma mensagem clara
git commit -m "feat: modificação da cor do botão"

# 3. Envia as alterações locais para o GitHub
git push


# 1. Garante que está na main e com a versão mais recente da nuvem
git switch main
git pull

# 2. Cria e entra na nova branch de desenvolvimento
git switch -c feature-cadastro-usuario

# 3. Trabalhe no código... quando terminar:
git add .
git commit -m "feat: cria tela de cadastro de usuario"

# 4. Envia a branch para o GitHub pela primeira vez
git push -u origin feature-cadastro-usuario

# 5. Retorna para a branch main local
git switch main

# 6. Baixa as alterações que acabaram de ser mescladas via Pull Request
git pull

# 7. Remove a branch local que já foi integrada e finalizada
git branch -d feature-cadastro-usuario