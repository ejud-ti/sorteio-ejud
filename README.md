# Sorteio EJUD/TJAM — Encerramento do Ano Letivo 2026

Página de sorteio por **número** ou por **nome** para a palestra *“O Mérito de Servir”*.
É um site estático (HTML + CSS + JS, sem dependências): basta abrir o `index.html` ou publicar no GitHub Pages.

## Como usar
1. Escolha **Por número** (intervalo + números excluídos) ou **Por nome** (um nome por linha, ou importe um `.txt`/`.csv`).
2. Defina a **quantidade por sorteio**.
3. Clique em **Sortear** (ou tecle `Espaço`/`Enter`). `F` abre o modo apresentação em tela cheia.
4. Se a pessoa sorteada não estiver presente, clique em **Ausente** e sorteie de novo.
5. Ao final, **Baixar CSV** ou **Imprimir ata** (pode salvar como PDF).

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
- `assets/fundo-celular.jpg` (opcional): fundo vertical para celular. Se o arquivo não existir, a página usa o `fundo.jpg`.
