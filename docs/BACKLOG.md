# Backlog do Viveiro

> Documento herdado. Escrito ao longo do 1º semestre de 2026 pela equipe anterior.
> Última alteração: 2026-05-28.
>
> **Aviso de quem escreveu:** algumas destas histórias passaram pela revisão do
> cliente e outras não. Não me lembro quais. Boa sorte. — R.M.

---

## Histórias escritas

### V-01 — Página da pessoa

**Como** aluno que encontrou uma ideia interessante,
**quero** ver a página de quem a publicou,
**para** saber se temos interesses em comum antes de procurá-la.

Pronto quando:
- clicar no nome do autor, em qualquer cartão, abre a página dessa pessoa;
- a página mostra nome ,foto de perfil, tipo (aluno ou professor), curso, interesses e descrição sobre a pessoa (Ex.:Universidade que ela se formou ,Linguagem de programação que mais trabalha), Contato como e-mail ou Linkedin;
- a página lista as ideias publicadas por essa pessoa, com o título clicável;
- se a pessoa não publicou nenhuma ideia, aparece a frase "ainda não publicou ideias" no lugar da lista vazia;
- existe um caminho de volta ao mural sem usar o botão do navegador.

---

### V-02 — Filtro por curso

Implementar um filtro por curso na barra lateral do mural, permitindo que o usuário visualize apenas os projetos relacionados ao curso selecionado.

Pronto quando:
- O usuário conseguir selecionar um curso na barra lateral do mural.
- O mural exibir apenas os projetos relacionados ao curso selecionado.
- O usuário conseguir remover o filtro e visualizar novamente todos os projetos.
- O filtro funcionar corretamente sem precisar recarregar a página.

---

### V-03 — Publicar uma ideia

**Como** aluno com uma ideia na cabeça,
**quero** publicá-la sem depender de ninguém,
**para** que ela exista antes de eu esquecer.

Pronto quando:
- existe um formulário com título, resumo e tags;
- ao enviar, a ideia aparece no topo do mural imediatamente, sem recarregar a página;
- a ideia criada traz, como autor, o nome de quem está navegando, e a data de hoje;
- título vazio impede o envio e mostra uma mensagem dizendo o que falta;
- a contagem total de ideias exibida no mural aumenta em um.

---

### V-04 — Encontrar ideias que combinam comigo

**Como** visitante do mural,
**quero** encontrar rapidamente as ideias que combinam comigo,
**para** não perder tempo.

Pronto quando:
- Existir um campo de busca visível no mural.
- O usuário consegue pesquisar ideias por título, resumo ou tags.
- Os resultados exibidos correspondem aos termos pesquisados.
- Quando não houver nenhuma ideia correspondente, o sistema informa que nenhum resultado foi encontrado.
- A busca apresenta os resultados sem necessidade de recarregar a página.
- O usuário consegue limpar a pesquisa e voltar a visualizar todas as ideias.

---

### V-05 — Entrar e sair de um grupo

**Como** aluno que quer se aproximar de um tema,
**quero** entrar num grupo,
**para** acompanhar o que se discute ali.

Pronto quando:
- a lista de grupos mostra, em cada grupo, se estou dentro ou fora;
- entrar acrescenta meu nome à lista de membros e o contador sobe;
- sair remove meu nome e o contador desce;
- a lista mostra os nomes dos membros, não apenas o número;
- trocar a pessoa em "navegando como" muda corretamente o que aparece como "meus grupos".

---

### V-06 — Estados da ideia

**Como** usuário,
**quero** que as ideias tenham estados,
**para** que os estados das ideias fiquem registrados.

Pronto quando:
- Uma nova ideia é criada automaticamente com o estado Semente.
- O autor da ideia consegue alterar manualmente seu estado.
- O autor consegue alterar o estado entre Semente, Germinando e Proposta.
- O estado atual da ideia é exibido de forma clara no mural.
- Após uma alteração, o novo estado é salvo e permanece correto quando a ideia for acessada novamente.
- Usuários que não são responsáveis pela ideia conseguem visualizar o estado, mas não conseguem alterá-lo.

Obs.: falamos em três estados — semente, germinando, proposta.

---

### V-07 — Registrar interesse em participar

**Como** aluno que quer entrar num projeto,
**quero** declarar interesse numa ideia,
**para** que quem a propôs saiba que pode me chamar.

Pronto quando:
- cada cartão tem um controle "tenho interesse em participar";
- ao acionar, meu nome passa a constar na lista de interessados daquela ideia;
- a mesma pessoa não consegue se registrar duas vezes na mesma ideia;
- é possível desfazer o interesse, e o nome sai da lista;
- o número de interessados exibido no cartão corresponde ao tamanho da lista.

---

### V-08 — Não perder o que foi escrito

**Como** usuário,
**quero** não perder o que escrevi,
**para** não ter que digitar tudo de novo.

Pronto quando:
- os dados forem salvos em `localStorage` usando `JSON.stringify`, e recuperados no carregamento da página.

---

### V-09 — Aviso de novo interessado

**Como** aluno com uma ideia publicada,
**quero** receber uma notificação no celular quando alguém demonstrar interesse,
**para** não perder a chance de formar grupo.

Pronto quando:
- ao registrar interesse, o autor recebe uma notificação no celular em até um minuto;
- a notificação mostra o nome de quem se interessou e o título da ideia;
- tocar na notificação abre a ideia correspondente.

---

## Caixa de entrada

Anotações de conversa. Ninguém escreveu direito ainda.

- **V-10** — ideias paradas
- **V-11** — relatório por curso
- **V-12** — exportar / importar o estado

---

## Defeitos conhecidos

Nenhum destes foi priorizado. Estão aqui para não serem esquecidos.

- **B-01** — depois de clicar numa tag, não há como desfazer o filtro; só recarregando a página.
- **B-02** — quando a busca não encontra nada, o mural fica em branco, sem nenhuma explicação.
- **B-03** — a data aparece como `2026-03-14` em vez de `14/03/2026`.
- **B-04** — buscar `robotica` não encontra "Robótica"; buscar `Musica` não encontra "música".
- **B-05** — o número de apoios no cartão só muda depois que se refaz a busca.
- **B-06** — título comprido vaza para fora do cartão e atravessa o cartão vizinho.

## Registro da triagem — 09/08

Claro. Copie o bloco abaixo inteiro; ele está em Markdown puro:

| História | Situação em que foi recebida | O que foi alterado | Justificativa |
|---|---|---|---|
| História v-01 | Estava até que bem completa | Optamos por não fazer nada nela | O grupo concordou que ela já estava boa |
| História v-02 | Totalmente incompleta e vaga | Os requisitos de pronto e uma melhor explicação de como o filtro deve funcionar | Estava totalmente incompleta e não havia como ter uma forma de saber que o filtro estava pronto |
| História v-03 | Estava muito boa e completa | Nada | O grupo concordou que a ideia já estava concreta e pronta |
| História v-04 | Estava muito vaga | Acrescentamos critérios de pronto que sejam testáveis | Havia poucos detalhes importantes que esse tipo de função deve ter |
| História v-05 | Bem simples, porém direta e bem explicada | Nada | Uma função simples não precisa de muitos detalhes, desde que os que já estão definidos sejam suficientes para os testes |
| História v-06 | Horrível, somente um detalhe muito vago | Acrescentamos as funções que devem ser realizadas, por quem e como cada estado deve ser definido | Não havia detalhes suficientes, então não reaproveitamos nada; somente seguimos o caminho detalhado pela ideia e demos nosso próprio detalhamento |
| História v-07 | A ideia e os detalhamentos já estavam bons e foi uma das mais concretas | Nada | Essa ideia estava muito boa e apresentava todos os requisitos de pronto que foram definidos |
