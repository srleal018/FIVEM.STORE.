
<html lang="pt-BR">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>FIVEM STORE</title>
<link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&display=swap" rel="stylesheet" />
<style>
* { margin: 0; padding: 0; box-sizing: border-box; }
body, html { height: 100%; font-family: 'Montserrat', sans-serif; color: #fff; overflow-x: hidden; }
body { background: url('https://upload.wikimedia.org/wikipedia/commons/7/7e/1_rocinha_favela_closeup.JPG') center/cover no-repeat fixed; position: relative; }
body::before { content: ""; position: fixed; top:0; left:0; width:100%; height:100%; background: rgba(0,0,0,0.6); z-index: 0; }
body::after { content:""; position: fixed; width: 200%; height: 200%; top: -50%; left: -50%; background: radial-gradient(rgba(255,255,255,0.05), transparent 70%); animation: moveBackground 30s linear infinite; z-index: 0; }
@keyframes moveBackground { 0% { transform: rotate(0deg) translate(0,0); } 50% { transform: rotate(15deg) translate(50px,50px); } 100% { transform: rotate(0deg) translate(0,0); } }
.content { position: relative; z-index: 1; max-width: 1300px; margin: auto; padding: 40px 20px; }
h1 { text-align: center; font-size: 3rem; margin-bottom: 10px; background: linear-gradient(90deg, red, orange, yellow, green, blue, indigo, violet); background-size: 600% 100%; -webkit-background-clip: text; -webkit-text-fill-color: transparent; animation: rainbowText 3s linear infinite; }
@keyframes rainbowText { 0% { background-position:0% 50%; } 50% { background-position:100% 50%; } 100% { background-position:0% 50%; } }
p.subtitle { text-align: center; font-size: 1.2rem; margin-bottom: 40px; color: #ddd; opacity:0; animation: fadeIn 1.5s 0.5s forwards; }
h2 { font-size: 2rem; margin-bottom: 20px; border-left: 6px solid #ff4c4c; padding-left: 10px; text-shadow: 1px 1px 3px black; opacity:0; animation: slideFromLeft 1s ease forwards; }
.category { display: grid; grid-template-columns: repeat(auto-fill, minmax(220px, 1fr)); gap: 25px; margin-bottom: 50px; }
.item { background: rgba(255, 255, 255, 0.05); border-radius: 15px; overflow: hidden; backdrop-filter: blur(10px); box-shadow: 0 10px 25px rgba(0,0,0,0.5); transition: transform 0.5s, box-shadow 0.5s; text-align: center; opacity: 0; transform: translateY(30px); animation: fadeInUp 0.8s forwards, float 4s ease-in-out infinite; }
@keyframes float { 0%, 100% { transform: translateY(0); } 50% { transform: translateY(-10px); } }
.item img { width: 100%; height: 150px; object-fit: cover; }
.item p { font-size: 1.1rem; font-weight: 600; margin: 15px 0; }
.item button { margin-bottom: 15px; padding: 10px 20px; border: none; border-radius: 8px; background: linear-gradient(90deg, #ff4c4c, #ff8a4c, #ff1f1f); background-size: 200% 100%; color: white; font-weight: 700; cursor: pointer; transition: transform 0.3s; animation: gradientBG 3s linear infinite; }
@keyframes gradientBG { 0% { background-position: 0% 50%; } 50% { background-position: 100% 50%; } 100% { background-position: 0% 50%; } }
.item:hover { transform: translateY(-15px) rotate(-2deg); box-shadow: 0 15px 35px rgba(0,0,0,0.7); }
.item button:hover { transform: scale(1.1); }
@keyframes fadeInUp { 0% { opacity: 0; transform: translateY(30px); } 100% { opacity: 1; transform: translateY(0); } }
@keyframes fadeIn { 0% { opacity:0; } 100% { opacity:1; } }
@keyframes slideFromLeft { 0% { opacity:0; transform: translateX(-50px); } 100% { opacity:1; transform: translateX(0); } }
.cart { position: fixed; top: 50px; right: 20px; width: 300px; background: rgba(0,0,0,0.8); padding: 15px; border-radius: 12px; box-shadow: 0 10px 25px rgba(0,0,0,0.7); cursor: move; z-index: 999; }
.cart h3 { text-align: center; margin-bottom: 10px; }
.cart ul { list-style: none; max-height: 300px; overflow-y: auto; margin-bottom: 10px; }
.cart li { display: flex; justify-content: space-between; padding: 5px 0; border-bottom: 1px solid rgba(255,255,255,0.2); }
.cart button { padding: 5px 10px; border:none; border-radius:6px; cursor:pointer; background: linear-gradient(90deg, #4caf50, #81c784); color:white; font-weight:600; transition:0.3s; }
.cart button:hover { transform: scale(1.1); }
#checkout-modal { position: fixed; top:0; left:0; width:100%; height:100%; background: rgba(0,0,0,0.8); display:none; justify-content:center; align-items:center; z-index:1000; }
#checkout-modal > div { background: rgba(0,0,0,0.9); padding:30px; border-radius:15px; text-align:center; }
#checkout-modal button { padding:10px 20px; font-size:1rem; font-weight:700; border:none; border-radius:10px; cursor:pointer; background: linear-gradient(90deg, #ff4c4c, #ff8a4c, #ff1f1f); background-size:200% 100%; color:white; animation: gradientBG 3s linear infinite; }
#checkout-modal button:hover { transform: scale(1.1); }
@media (max-width: 600px) { h1 { font-size: 2.2rem; } h2 { font-size: 1.5rem; } .cart { width: 90%; right: 5%; top: 20px; } }
</style>
</head>
<body>
<div class="content">
    <h1>FIVEM STORE</h1>
    <p class="subtitle">ENCONTRE OS MELHORES PREÇOS AQUI!!!</p>
    <!-- ITENS -->
    <h2>ITENS</h2>
    <div class="category">
        <div class="item" style="animation-delay:0.2s;">
            <img src="https://media.discordapp.net/attachments/1441877569506119681/1442046584001925210/1.png?ex=69240209&is=6922b089&hm=bf0ed131c896338c5e8a6386bdcbb31b34422a92434aaa05db32a928fe41f7cb&=&format=webp&quality=lossless&width=626&height=626" alt="Lock Pick" />
            <p>Lock Pick</p>
            <button data-name="Lock Pick" data-price="0.45">Comprar</button>
        </div>
    </div>
    <!-- MUNIÇÃO -->
    <h2>MUNIÇÃO</h2>
    <div class="category">
        <div class="item" style="animation-delay:0.3s;">
            <img src="https://media.discordapp.net/attachments/1441877569506119681/1442046641363226787/12.png?ex=69240217&is=6922b097&hm=2876528cf9def92f3fb330d38405316db84484f1f8904612f37f79749aac2c27&=&format=webp&quality=lossless&width=626&height=626" alt="Munição Pistola" />
            <p>Munição Pistola</p>
            <button data-name="Munição Pistola" data-price="0.30">Comprar</button>
        </div>
        <div class="item" style="animation-delay:0.4s;">
            <img src="https://media.discordapp.net/attachments/1441877569506119681/1442046640163782656/9.png?ex=69240216&is=6922b096&hm=68fc79a83f785e091ca89fca06fbd2bdaae7dace82c28fbfa12920625072c551&=&format=webp&quality=lossless&width=626&height=626" alt="Munição Fuzil" />
            <p>Munição Fuzil</p>
            <button data-name="Munição Fuzil" data-price="0.40">Comprar</button>
        </div>
    </div>
    <!-- ARMAS -->
    <h2>ARMAS</h2>
    <div class="category">
        <div class="item" style="animation-delay:0.5s;">
            <img src="https://media.discordapp.net/attachments/1441877569506119681/1442046584895311872/4.png?ex=69240209&is=6922b089&hm=866da0c43fa5f067d8a3256b09f90e8d2276e8d95e79e6fc6bd0774e17c4ceec&=&format=webp&quality=lossless&width=626&height=626" alt="AKM" />
            <p>AKM</p>
            <button data-name="AKM" data-price="1.25">Comprar</button>
        </div>
        <div class="item" style="animation-delay:0.6s;">
            <img src="https://media.discordapp.net/attachments/1441877569506119681/1442046585205821502/5.png?ex=69240209&is=6922b089&hm=0ede7c80ffc6b737666e27f18844c36ae6972ec9a402cf86eb9921204a46a3bf&=&format=webp&quality=lossless&width=626&height=626" alt="FAL" />
            <p>FAL</p>
            <button data-name="FAL" data-price="1.50">Comprar</button>
        </div>
        <div class="item" style="animation-delay:0.7s;">
            <img src="https://media.discordapp.net/attachments/1441877569506119681/1442046585533108235/6.png?ex=69240209&is=6922b089&hm=520d250e48319cbc4535a3b717fb168fa837c1d9560dac0e1b61f8b9a93d3d9a&=&format=webp&quality=lossless&width=626&height=626" alt="G17" />
            <p>G17</p>
            <button data-name="G17" data-price="0.89">Comprar</button>
        </div>
        <div class="item" style="animation-delay:0.8s;">
            <img src="https://media.discordapp.net/attachments/1441877569506119681/1442046585809670184/7.png?ex=69240209&is=6922b089&hm=81fac10d68bc25d6b3405f4871fdf59747bb7361092e41f228190b6ed7db2915&=&format=webp&quality=lossless&width=626&height=626" alt="MK" />
            <p>MK</p>
            <button data-name="MK" data-price="1.70">Comprar</button>
        </div>
        <div class="item" style="animation-delay:0.9s;">
            <img src="https://media.discordapp.net/attachments/1441877569506119681/1442046698925854791/Design_sem_nome.png?ex=69240224&is=6922b0a4&hm=3a50ef7d0c2960f50a4872ab565f278e4e3e483b5e15d7601061b90a7aae29ac&=&format=webp&quality=lossless&width=750&height=750" alt="HK" />
            <p>HK</p>
            <button data-name="HK" data-price="1.60">Comprar</button>
        </div>
    </div>
</div>

<!-- CARRINHO -->
<div class="cart" id="cart">
    <h3>Carrinho</h3>
    <ul id="cart-items"></ul>
    <button id="finalize-btn">Finalizar Compra</button>
</div>

<!-- MODAL DE FINALIZAÇÃO -->
<div id="checkout-modal">
  <div>
    <h2>Finalize sua Compra</h2>
    <p id="checkout-details" style="margin:20px 0;"></p>
    <p>PIX: <b>04347085265</b></p>
    <button id="close-modal">Ir para o Discord</button>
  </div>
</div>

<script>
let cart = {};

// Adicionar item
document.querySelectorAll('.item button').forEach(btn=>{
    btn.addEventListener('click', ()=>{
        const name = btn.dataset.name;
        const price = parseFloat(btn.dataset.price);
        if(cart[name]) cart[name].qty++;
        else cart[name] = {name, price, qty:1};
        renderCart();
    });
});

// Renderizar carrinho
function renderCart(){
    const cartItems = document.getElementById('cart-items');
    cartItems.innerHTML='';
    for(const key in cart){
        const li = document.createElement('li');
        li.innerHTML = `${cart[key].name} x${cart[key].qty} - R$${cart[key].price * cart[key].qty} <button onclick="removeItem('${key}')">-</button>`;
        cartItems.appendChild(li);
    }
}

// Remover item 1 por 1
function removeItem(name){
    if(cart[name]){
        cart[name].qty--;
        if(cart[name].qty<=0) delete cart[name];
        renderCart();
    }
}

// Finalizar Compra
document.getElementById('finalize-btn').addEventListener('click', () => {
    let total = 0;
    for(const key in cart) total += cart[key].price * cart[key].qty;
    const details = Object.values(cart).map(item=>`${item.name} x${item.qty} - R$${item.price * item.qty}`).join('<br>');
    document.getElementById('checkout-details').innerHTML = `${details}<br><b>Total: R$${total}</b>`;
    document.getElementById('checkout-modal').style.display='flex';
});

// Ir para Discord
document.getElementById('close-modal').addEventListener('click', ()=>{
    window.open("https://discord.gg/UduJqBwEf", "_blank");
});

// Tornar carrinho movível
dragElement(document.getElementById("cart"));
function dragElement(elmnt) {
  let pos1 = 0, pos2 = 0, pos3 = 0, pos4 = 0;
  elmnt.onmousedown = dragMouseDown;
  function dragMouseDown(e) {
    e = e || window.event;
    e.preventDefault();
    pos3 = e.clientX; pos4 = e.clientY;
    document.onmouseup = closeDragElement;
    document.onmousemove = elementDrag;
  }
  function elementDrag(e) {
    e = e || window.event; e.preventDefault();
    pos1 = pos3 - e.clientX; pos2 = pos4 - e.clientY;
    pos3 = e.clientX; pos4 = e.clientY;
    elmnt.style.top = (elmnt.offsetTop - pos2) + "px";
    elmnt.style.left = (elmnt.offsetLeft - pos1) + "px";
  }
  function closeDragElement() { document.onmouseup = null; document.onmousemove = null; }
}
</script>

</body>

<!DOCTYPE html>
<html>
<head>
  <title>Ticket de Vendas</title>
</head>
<body>

<h2>Login por Email</h2>
<input type="email" id="emailInput" placeholder="Digite seu email" />
<button onclick="login()">Entrar</button>

<div id="ticketArea" style="display:none;">
  <h3>Criar Ticket</h3>
  <textarea id="message" placeholder="Descreva seu problema ou pedido"></textarea><br>
  <button onclick="criarTicket()">Abrir Ticket</button>

  <h3>Tickets</h3>
  <div id="ticketsList"></div>
</div>

<script>
let userEmail = '';
let isStaff = false;
let tickets = [];

function login() {
  const email = document.getElementById('emailInput').value;
  fetch('/login', {
    method: 'POST',
    headers: {'Content-Type': 'application/json'},
    body: JSON.stringify({email})
  })
  .then(res => res.json())
  .then(data => {
    userEmail = data.email;
    isStaff = data.isStaff;
    alert(`Logado como ${userEmail}. Staff: ${isStaff}`);
    document.getElementById('ticketArea').style.display = 'block';
    carregarTickets();
  });
}

function carregarTickets() {
  const list = tickets.map(t => `
    <div style="border:1px solid #000; margin:5px; padding:5px;">
      <p><b>ID:</b> ${t.id} | <b>Status:</b> ${t.status}</p>
      <p><b>Email:</b> ${t.email}</p>
      <p><b>Mensagem:</b> ${t.message}</p>
      ${t.status === 'fechado' ? `
        <p><b>Avaliação:</b> ${t.avaliacao || '-'} </p>
        <button onclick="avaliarTicket(${t.id})">Avaliar</button>
      ` : `
        <button onclick="mudarStatus(${t.id}, 'aberto')">Abrir</button>
        <button onclick="mudarStatus(${t.id}, 'fechado')">Fechar</button>
      `}
    </div>
  `).join('');
  document.getElementById('ticketsList').innerHTML = list;
}

function criarTicket() {
  const message = document.getElementById('message').value;
  fetch('/ticket/create', {
    method: 'POST',
    headers: {'Content-Type': 'application/json'},
    body: JSON.stringify({email: userEmail, message})
  })
  .then(res => res.json())
  .then(ticket => {
    tickets.push(ticket);
    carregarTickets();
    document.getElementById('message').value = '';
  });
}

function mudarStatus(id, status) {
  fetch('/ticket/status', {
    method: 'POST',
    headers: {'Content-Type': 'application/json'},
    body: JSON.stringify({id, status})
  })
  .then(res => res.json())
  .then(ticket => {
    const index = tickets.findIndex(t => t.id === id);
    if(index > -1) {
      tickets[index] = ticket;
      carregarTickets();
    }
  });
}

function avaliarTicket(id) {
  const avaliacao = prompt('Por favor, avalie este ticket (1 a 5):');
  if (avaliacao) {
    fetch('/ticket/avaliar', {
      method: 'POST',
      headers: {'Content-Type': 'application/json'},
      body: JSON.stringify({id, avaliacao})
    })
    .then(res => res.json())
    .then(resp => {
      const index = tickets.findIndex(t => t.id === id);
      if(index > -1) {
        tickets[index] = resp.ticket;
        carregarTickets();
        alert('Avaliação enviada com sucesso!');
      }
    });
  }
}
</script>

</body>
</html>





