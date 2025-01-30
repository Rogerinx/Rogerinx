

## O iHungry :
- I hungry é um aplicativo de delivery de alimentos que conecta usuários a uma ampla variedade de restaurantes locais. Com uma interface intuitiva e amigável, os usuários podem navegar por menus, fazer pedidos e acompanhar o status de suas entregas em tempo real. O objetivo é proporcionar uma experiência de pedido de comida rápida, conveniente e confiável.

## Arquitetura e Stack :

- A aplicação foi desenvolvida utilizando a linguagem de programação Java para a lógica de negócios e HTML/CSS para a interface do usuário. A arquitetura segue o padrão MVC (Model-View-Controller), que separa a aplicação em três componentes principais:

## PM canvas :
![17382575686427903356188637539706](https://github.com/user-attachments/assets/1a6380eb-ed03-4dec-a396-98f9698c1bec)

## model protopersona 
![17382567469526788531823060687017](https://github.com/user-attachments/assets/3d68b23a-da57-40ff-abcf-94fa77a95e26)


## requisitos:

- usuários : Pessoas entregadoras parceiras I’m hungry, de todas as modalidades de entrega — Nuvem Fixo em Restaurante e Operador Logístico. Cliente comun.

## carrinho :

- dentro do carrinho, o usuário poderá se aproveitar de: verificar os itens que escolheu, junto de seus atributos utilizar-se de cupons caso possua escolher a forma de pagamento verificar o local de entrega do pedido escolher a forma de entrega


## produtos : 

- usuário vera oque ele irá comprar 

## pratos : 

- Pratos culinários saborosos e baratos, atrativos para clientes: Cada restaurante parceiro pode colocar a descrição de seus pratos nome do prato fotos ingredientes Os restaurantes e pratos serão classificados para facilitar a busca do usuario final

## preco :

- o cliente verá o preço de cada produto cujo ele pretende comprar o preço do pedido final pode ser visto no carrinho descontos podem ser oferecidos pelos restaurantes e pela plataforma I’m hungry

## formas de pagamento : 

- Formas de pagamento que o cliente pode optar, dentre elas estão: pix, cartão(débito e crédito) dinheiro.

## protótipo: 
![1738257516919833142101723902201](https://github.com/user-attachments/assets/127a7e67-92de-4ea0-b233-9f6fe9f1f1d7)


## criação do BMC

https://www.canva.com/design/DAGdsbdsuWA/KIsYB697U7SwdW7UBbAYCQ/edit?utm_content=DAGdsbdsuWA&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton


## codigo html : <!DOCTYPE html>
- <html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Restaurante ParaDS</title>
    <link rel="stylesheet" href="styles.css">
    <script defer src="script.js"></script>
</head>
<body>
    <header>
        <h1>Restaurante ParaDS</h1>
        <nav>
            <button id="menu-btn">☰</button>
            <ul id="menu">
                <li><a href="cardapio.html">Cardápio</a></li>
                <li><a href="contato.html">Contato</a></li>
                <li><a href="sobre-nos.html">Sobre</a></li>
            </ul>
        </nav>
    </header>
    
    <section>
        <h2>Bem-vindo ao Restaurante ParaDS</h2>
        <p>Descubra mais sobre nossos pratos e nossa história visitando as páginas do menu.</p>
    </section>
    
    <footer>
        <p>&copy; 2025 Restaurante ParaDS - Todos os direitos reservados.</p>
    </footer>
</body>
</html>

## codigo css :
- /* Resetando margens e paddings padrão */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

/* Estilos para o corpo */
body {
    font-family: Arial, sans-serif;
    line-height: 1.6;
    background-color: #f4f4f4;
    color: #333;
}

/* Estilos do cabeçalho */
header {
    background-color: #eb1717;
    color: white;
    padding: 10px 20px;
    text-align: center;
}

header h1 {
    margin: 0;
}

/* Estilos de navegação */
nav {
    margin-top: 10px;
}

#menu {
    list-style: none;
    display: flex;
    justify-content: center;
    gap: 20px;
}

#menu li {
    display: inline;
}

#menu li a {
    text-decoration: none;
    color: white;
    font-weight: bold;
    transition: color 0.3s ease;
}

#menu li a:hover {
    color: #0e0d0d;
}

/* Estilos do botão de menu */
#menu-btn {
    display: none;
    background-color: #0c0b0b;
    color: white;
    border: none;
    padding: 10px;
    cursor: pointer;
}

#menu-btn:hover {
    background-color: #f4a261;
}

/* Estilos das seções */
section {
    padding: 20px;
    margin: 20px 0;
    background-color: white;
    border-radius: 8px;
}

h2 {
    margin-bottom: 10px;
    color: #161616;
}

ul {
    list-style: none;
    margin: 0;
    padding: 0;
}

ul li {
    margin-bottom: 10px;
}

footer {
    background-color: #0e0d0d;
    color: white;
    padding: 10px;
    text-align: center;
}

/* Estilos para telas pequenas */
@media (max-width: 768px) {
    #menu {
        display: none;
        flex-direction: column;
        align-items: center;
    }

    #menu li {
        margin-bottom: 10px;
    }

    #menu-btn {
        display: block;
    }

    #menu.active {
        display: flex;
    }
}
/* Estilos específicos para o cardápio */
#cardapio {
    max-width: 2000px;
    margin: 0 auto;
    padding: 20px;
    background-color: #fff;
    border-radius: 8px;
}

.category {
    margin-bottom: 30px;
    padding: 10px;
    background-color: #f9f9f9;
    border-radius: 8px;
}

.category h3 {
    font-size: 1.8rem;
    color: #333;
    border-bottom: 2px solid #0c0c0c;
    padding-bottom: 5px;
    margin-bottom: 15px;
}

.category ul {
    list-style: none;
    padding-left: 0;
}

.category ul li {
    margin-bottom: 20px;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.category ul li strong {
    font-size: 1.1rem;
    color: #333;
}

.category ul li p {
    font-size: 1rem;
    color: #666;
}

#cardapio {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
    gap: 20px;
}

footer {
    background-color: #333;
    color: white;
    padding: 10px;
    text-align: center;
}
/* Definir a imagem de fundo para o cardápio (segundo contêiner) */
#cardapio {
    max-width: 1800px;
    margin: 20px auto;
    padding: 20px;
    background-image: url('bandeira-do-para.jpg'); /* Altere o caminho para a imagem */
    background-size: cover; /* Faz a imagem cobrir toda a seção */
    background-position: center; /* Centraliza a imagem */
    background-attachment: scroll; /* A imagem rola com o conteúdo */
    border-radius: 8px;
    color: white; /* Mudando a cor do texto para branco para garantir boa legibilidade sobre o fundo */
}

/* Outras personalizações, se necessário */
header {
    padding: 20px;
    background-color: rgb(219, 15, 15); /* Fundo branco com opacidade */
    border-bottom: 2px solid #0c0c0c;
    position: relative;
}

footer {
    background-color: rgba(0, 0, 0, 0.7); /* Fundo escuro com opacidade */
    color: white;
    padding: 10px;
    text-align: center;
}
## sobre
- <!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sobre Nós - Restaurante ParaDS</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Restaurante ParaDS</h1>
        <nav>
            <button id="menu-btn">☰</button>
            <ul id="menu">
                <li><a href="index.html">inicio</a></li>
                <li><a href="cardapio.html">Cardápio</a></li>
                <li><a href="contato.html">Contato</a></li>
            </ul>
        </nav>
    </header>
    
    <section id="sobre">
        <h2>Sobre Nós</h2>
        <p>Bem-vindo ao ParaDS, um restaurante dedicado a oferecer experiências gastronômicas inesquecíveis. Estamos no coração da cidade, servindo pratos preparados com ingredientes frescos e de alta qualidade, em um ambiente acolhedor.</p>
    </section>

    <footer>
        <p>&copy; 2025 Restaurante ParaDS - Todos os direitos reservados.</p>
    </footer>
</body>
</html>

## contato :
- <!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Contato - Restaurante ParaDS</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Restaurante ParaDS</h1>
        <nav>
            <button id="menu-btn">☰</button>
            <ul id="menu">
                <li><a href="index.html">inicio</a></li>
                <li><a href="cardapio.html">Cardápio</a></li>
                <li><a href="sobre-nos.html">Sobre</a></li>
            </ul>
        </nav>
    </header>
    
    <section id="contato">
        <h2>Contato</h2>
        <p>Endereço: Rua das Delícias, 123 - Centro</p>
        <p>Telefone: (11) 98765-4321</p>
        <p>Envie-nos um e-mail para <a href="mailto:contato@saborearte.com">contato@saborearte.com</a></p>
    </section>

    <footer>
        <p>&copy; 2025 Restaurante ParaDS - Todos os direitos reservados.</p>
    </footer>
</body>
</html>



## feito por :

- Roger f. cardoso
- Matheus silva
- José Eduardo
- Eduardo Araujo
- Alisson Dantas
  
