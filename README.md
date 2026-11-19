# Sorteio EJUD/TJAM — Encerramento do Ano Letivo 2026

Página de sorteio por **número** ou por **nome** para a palestra *“O Mérito de Servir”*.
É um site estático (HTML + CSS + JS, sem dependências): basta abrir o `index.html` ou publicar no GitHub Pages.

## Como usar
1. Escolha **Por número** (intervalo + números excluídos) ou **Por nome** (um nome por linha, ou importe um `.txt`/`.csv`).
2. Defina a **quantidade por sorteio**. Com mais de 1, escolha **Todos de uma vez** ou **Um de cada vez** (cada clique revela o próximo da rodada).
3. Opcional: marque **Limitar o total de sorteados** e defina o número de vagas. Ao preencher as vagas, o sorteio encerra; marcar um ausente libera a vaga (−1 +1).
4. Clique em **Sortear** (ou tecle `Espaço`/`Enter`). `F` abre o modo apresentação em tela cheia.
5. Se a pessoa sorteada não estiver presente, clique em **Ausente**. Dá para marcar vários e depois clicar em **Sortear** para sortear os substitutos: todos juntos ou um de cada vez, conforme o modo. Enquanto o substituto não foi sorteado, a marcação pode ser desfeita.
6. Ao final, **Baixar CSV** ou **Imprimir ata** (pode salvar como PDF).

## Telão (2ª tela)
Clique em **Telão** para abrir uma janela que mostra só o palco do sorteio. Arraste essa janela para o projetor ou a segunda tela e clique nela uma vez para entrar em tela cheia e ativar o som. Os sorteios feitos na janela principal aparecem no telão automaticamente. O ponto verde no botão indica que o telão está conectado; nesse caso o som toca só no telão. Também dá para abrir direto pelo endereço `.../?telao=1`.

## Regras de imparcialidade
- Números aleatórios de `crypto.getRandomValues` (gerador criptográfico), com amostragem por rejeição, de modo que todos têm exatamente a mesma chance.
- Sem reposição: quem foi sorteado (inclusive quem foi marcado como ausente) não volta para a lista.
- A lista é lacrada no primeiro sorteio e recebe um código SHA-256 que aparece na ata.
- O resultado é gravado antes da animação, então recarregar a página não refaz o sorteio.
- O estado fica salvo no navegador (`localStorage`); **Novo sorteio** apaga tudo, depois de pedir confirmação.

## Publicar no GitHub Pages
Settings → Pages → *Deploy from a branch* → `main` / root.

## Imagens
- `assets/fundo.jpg`: fundo da página.
- `assets/logo-ejud.png`: logo da EJUD.
- `assets/fundo-celular.jpg`: fundo vertical para celular (versão clara da ilustração).
