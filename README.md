# Eliminando barreira - Prática 01

Hoje iremos testar o uso de um Leitor de tela; para facilitar o uso em sala de aula, vamos começar pelo plugin Screen Reader `[ChromeVox]` instalado no navegador `Chrome`.

## Steps
### Step 01 - Configuração do ambiente
1. Instale o `Google Chrome`, caso não o tenha instalado, você o encontrará neste [link](https://www.google.com/intl/pt-BR/chrome/).
2. Instale o plugin acessando este [link](https://chrome.google.com/webstore/detail/screen-reader/kgejglhpjiefppelpmljglcjbhoiplfn/related).
3. Certifique-se que o plugin esteja ativo, no `Chrome`, ao lado da foto de perfil, clique no botão extensões e ative ou desative o SwitchButton do `Screen reader`; detalhe, voce pode desabilitá-lo enquanto estiver codificando e ativá-lo quando for realizar os testes.
4. Acesse o repositório com as instruções neste [link](https://github.com/f290SI/acsb-eliminando-barreiras-01).
5. Se preferir, clone este projeto utilizando o `GitDesktop` ou `GitBash`ou o proprio shell de seu sistema operacional utilizado com o comando abaixo, pois novas instruções serão disponibilizadas em outros **commits**:
```shell
git clone https://github.com/f290SI/acsb-eliminando-barreiras-01.git
```
### Step 02 - Criação de página web sem HTML5
1. Criar uma página web (HTML e CSS) que descreva um de seus locais favoritos para comer e contenha uma imagem do seu prato favorito, assim como sua opinião sobre este prato e as informações de localização deste local. Utilize o `HTML 4` para criá-lo, sem as tags semanticas.

### Step 03 - Validação com Screen Reader
1. Ao conluir a codificação, ativo o `Screen reader` e faça com que ele realize a leituta do site.
2. Como ainda não configuramos os atalhos de teclado no plugin, clique sobre os elementos para que ocorra a leitura.
3. Faça uma reflexão e questionamento sobre o a leitura do conteúdo, e anote no bloco de notas suas considerações sobre esta leitura.

### Step 4 - Ouvir o conteúdo de um site que você não desenvolveu
1. Combine com algum dos demais alunos o envio da página criada para que você possa ouvi-la.
2. Faça a leitura do conteúdo com o `Screen Reader`, mas sem **você** o ler contéudo e sem observar as imagens; contenha-se a clicar sobre o elemento `olhando o mínimo possível` e sem obserar, afinal nós olhamos tudo por que temos a visão perfeita, mas observamos apenas o que nos é de interesse, você entenderam! O foco deve ser o audio.
3. Faça uma reflexão e questionamento sobre o a leitura do conteúdo, e anote no bloco de notas suas considerações sobre esta leitura.

### Step 5 - Refatoração do seu conteúdo com HTML 5
Com base nos possíveis gaps semanticos, utilize a estrutura discutida em sala com o HTML 5.

1. Adapte seu contéudo para a a estrutura abaixo.
```html
<!DOCTYPE html>
<!-- declaração da linguagem principal -->
<html lang="pt-br">

<head>
    <!--  declaração codificação de caracteres utilizada -->
    <meta charset="utf-8">
    <!--  declaração de viewport que não bloqueia o zoom -->
    <meta name="viewport" content="width=device-width, initial- scale=1.0">
    <link rel="stylesheet" href="css/main.css">
    </noscript>
    <!-- descrição significativa para a página -->
    <title>Favorite Food | Principal </title>
</head>

<body>
    <!-- skip link manual para usurios que utilizam teclado -->
    <!-- <a href="#main">atalho teclado para conteúdo principal</a> -->
    <a href="#main" aria-label="Saltar para conteúdo principal">skip to main content</a>
    <!-- logo / navegação, etc. estarão aqui -->
    <main id="main">
        <!-- conteúdo único e significativo estará aqui -->
    </main>
    <!-- rodapé estará aqui -->
    <footer></footer>
    <!-- recurso não bloqueante de javascript-->
    <script src="scripts.js"></script>
</body>

</html>
```
2. Utilize as TAGs semanticas `main`, `nav`, `aside`, `section`, `article`, `header`, `address`, `strong`, `em` e demais tags que possam melhorar a leitura.  
3. Adicione o CSS do skip link:
```css
[href="#main"] {
    position: absolute;
    top: 0;
    left: 100%;
}

[href="#main"]:focus {
    right: auto;
}
```
4. Pesquise as TAGs semanticas que possam identificar melhor os dados apresentados, acesse esta referência da Mozilla [elementos semanticos textuais inline](https://developer.mozilla.org/pt-BR/docs/Web/HTML/Element#sem%C3%A2nticas_textuais_inline).
5. Conheça e compare algumas TAGs da versão **4** e **5** do HTML neste [link](https://diegomariano.com/tags-html/).
6. Utilize a maior quantidade possível de tags semanticas, dê uma força para o `Leitor de Telas` e ganhe muitos pontos de **XP** em Acessibilidade!

### Step 06 - [Re]Validação com Screen Reader
Idem `Step 04`.
