<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<title>DigiCarta - Menú de prueba</title>
<meta name="viewport" content="width=device-width, initial-scale=1">
<style>
  body { font-family: Inter, sans-serif; background: #f9f9f9; color: #333; padding: 20px; }
  h1 { color: #7B2CBF; }
  .plate { border-bottom: 1px solid #ddd; padding: 10px 0; }
  .name { font-weight: bold; }
  .price { float: right; }
  button { margin-top: 5px; background: #FDB500; border: none; padding: 8px 12px; color: white; cursor: pointer; font-weight: bold; }
</style>
</head>
<body>
<h1>DigiCarta – Menú</h1>

<div class="plate">
  <div class="name">Ensalada César <span class="price">8 €</span></div>
  <button onclick="pedido('Ensalada César', 8)">Pedir</button>
</div>
<div class="plate">
  <div class="name">Hamburguesa clásica <span class="price">12 €</span></div>
  <button onclick="pedido('Hamburguesa clásica', 12)">Pedir</button>
</div>
<div class="plate">
  <div class="name">Tarta de queso <span class="price">6 €</span></div>
  <button onclick="pedido('Tarta de queso', 6)">Pedir</button>
</div>

<div id="cart" style="margin-top:20px;">
  <h2>Pedido:</h2>
  <ul id="items"></ul>
  <div>Total: <span id="total">0</span> €</div>
  <button onclick="alert('Aquí se integrará el pago 👍')">Pagar</button>
</div>

<script>
let total = 0;
function pedido(nombre, precio) {
  total += precio;
  const li = document.createElement('li');
  li.textContent = nombre + " — " + precio + " €";
  document.getElementById('items').appendChild(li);
  document.getElementById('total').textContent = total;
}
</script>
</body>
</html>
