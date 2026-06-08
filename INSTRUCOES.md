# Guia de Configuração: Jogo da Cobrinha no Perfil do GitHub 🐍

Siga os passos abaixo para ativar a animação do jogo da cobrinha no seu perfil do GitHub.

---

## Passo 1: Enviar os arquivos locais para o GitHub
Abra o seu terminal na pasta atual (`c:\Users\gabri\OneDrive\Área de Trabalho\git`) e execute os comandos a seguir para associar o repositório local ao seu repositório remoto e enviar os arquivos:

```bash
# Associa o repositório local ao seu repositório do GitHub
git remote add origin https://github.com/Gabriel-SDA/personaliza-o.git

# Adiciona todos os arquivos criados
git add .

# Cria o commit inicial
git commit -m "feat: adicionar workflow do jogo da cobrinha e README"

# Renomeia a branch padrão para main (caso esteja como master)
git branch -M main

# Envia os arquivos para o GitHub
git push -u origin main
```

*(Nota: se o repositório remoto já tiver commits, você pode precisar fazer um `git pull origin main --rebase` antes do push ou fazer `git push -u origin main --force` se puder sobrescrevê-lo).*

---

## Passo 2: Habilitar as permissões da GitHub Action ⚠️ (Muito Importante!)
Por padrão, o GitHub bloqueia as Actions de criarem novos commits/branches por questões de segurança. Para liberar o acesso para que a cobrinha seja gerada:

1. Acesse a página do seu repositório recém-criado no site do GitHub.
2. Clique na aba **Settings** (Configurações) no topo do repositório.
3. No menu lateral esquerdo, sob a seção "Actions", clique em **General**.
4. Role a página até o final até encontrar a seção **Workflow permissions** (Permissões de fluxo de trabalho).
5. Selecione a opção **Read and write permissions** (Permissões de leitura e escrita).
6. Clique no botão **Save** (Salvar) logo abaixo.

---

## Passo 3: Executar a Action pela primeira vez
A Action está programada para rodar a cada 12 horas, mas você pode iniciá-la manualmente agora para ver o resultado na hora:

1. No seu repositório no site do GitHub, clique na aba **Actions** no menu superior.
2. No menu lateral esquerdo, clique em **Generate Snake**.
3. No lado direito, clique no menu suspenso **Run workflow**.
4. Clique no botão verde **Run workflow**.
5. Aguarde cerca de 1 a 2 minutos. A Action ficará com um ícone verde de sucesso.
6. Atualize a página inicial do seu perfil do GitHub e pronto! O jogo da cobrinha estará animado em cima do seu gráfico de contribuições.

---

*Se precisar de ajuda com algum desses passos, estou aqui para te auxiliar!*
