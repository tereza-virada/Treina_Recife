<head>
    <style>
        h1 {
            color: lightblue;
        }
        h2 {
            color: grey;
        }
        p {
            color: black;
        }
    </style>
</head>

<h1 style="font-color: blue;">Git workflow</h1>

<h2>1. Iniciando o Trabalho (Sincronizando e ramificando)</h2>
<p>Antes de escrever qualquer código, é fundamental garantir que você está com a versão mais recente do projeto e em um ambiente seguro para testar suas ideias.</p>
<b></b>
<p><b>git pull</b>: Atualiza seu repositório local com as alterações mais recentes do repositório remoto. Faça isso na branch principal (geralmente main ou master) antes de criar uma nova ramificação para evitar conflitos futuros.</p>

<p><b>git checkout -b <nome-da-branch>:</b> Cria uma nova branch e muda imediatamente para ela. É aqui que você desenvolverá sua nova funcionalidade ou corrigirá um bug de forma isolada. (Nota: O comando mais moderno para isso é git switch -c <nome-da-branch>).</p>

<h2>2. Escrevendo o Código (Verificando e preparando)</h2>
<p>Enquanto você programa, precisará monitorar o que foi alterado e escolher exatamente o que fará parte do seu próximo salvamento.</p>

<p><b>git status:</b> O comando mais usado. Ele mostra o estado atual do seu repositório: quais arquivos foram modificados, quais são novos (untracked) e quais já estão prontos para serem salvos (staged).</p>

<p><b>git add <nome-do-arquivo>:</b> Adiciona uma modificação específica à "área de preparação" (Staging Area).</p>

<p><b>git add .:</b> Um atalho rápido que adiciona todas as modificações do diretório atual à área de preparação. Use com cuidado para não adicionar arquivos indesejados.</p>

<h2>3. Salvando o Histórico (O Commit)</h2>
<p>Com as alterações na área de preparação, é hora de empacotá-las com uma mensagem descritiva.</p>

<p><b>git commit -m "Sua mensagem descritiva aqui":</b> Salva as alterações no histórico do seu repositório local. Uma boa prática é usar mensagens claras no imperativo (ex: "Adiciona validação de email no login" em vez de "Adicionado validação").</p>

<h2>4. Compartilhando o Código (Enviando para o remoto)</h2>
<p>Após finalizar seus commits locais, você precisa enviar esse trabalho para o servidor (GitHub, GitLab, Bitbucket, etc.) para que a equipe possa revisar.</p>

<p><b>git push origin <nome-da-branch>: </b>Envia sua branch local e todos os commits dela para o repositório remoto. A partir daqui, você geralmente abre um Pull Request (PR) ou Merge Request (MR) na interface web.</p>

<h2>5. Integrando Mudanças (Lidando com o código dos outros)</h2>
<p>Se a branch principal for atualizada por outro desenvolvedor enquanto você estiver trabalhando, você precisará trazer essas novidades para a sua branch.</p>

<p><b>git merge <nome-da-branch>:</b> Pega o histórico de uma branch (como a main atualizada) e mescla com a branch em que você está no momento.</p>
