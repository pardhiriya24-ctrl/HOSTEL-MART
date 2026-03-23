<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Hostel Mart</title>

<style>

*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:'Segoe UI', sans-serif;
}

body{
background:#eef2f7;
}

/* HEADER */
header{
background:linear-gradient(90deg,#2c7be5,#00c6ff);
color:white;
padding:20px;
text-align:center;
box-shadow:0 2px 10px rgba(0,0,0,0.1);
}

header h1{
font-size:32px;
}

/* MAIN */
.main-container{
display:flex;
}

/* CONTENT */
.content{
flex:1;
padding:30px;
}

/* CART */
.cart-panel{
width:300px;
background:white;
padding:20px;
box-shadow:-3px 0 10px rgba(0,0,0,0.1);
border-left:4px solid #2c7be5;
}

.cart-panel h2{
margin-bottom:15px;
}

/* LOGIN */
.login-box{
max-width:400px;
margin:auto;
background:white;
padding:30px;
border-radius:10px;
box-shadow:0 5px 15px rgba(0,0,0,0.1);
}

.login-box input{
width:100%;
padding:10px;
margin-top:10px;
margin-bottom:15px;
border:1px solid #ccc;
border-radius:5px;
}

/* BUTTON */
button{
background:#2c7be5;
color:white;
border:none;
padding:10px 15px;
border-radius:6px;
cursor:pointer;
transition:0.3s;
}

button:hover{
background:#1f5fb8;
transform:scale(1.05);
}

/* PRODUCTS */
.products{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(200px,1fr));
gap:20px;
margin-top:20px;
}

.product-card{
background:white;
padding:15px;
border-radius:10px;
box-shadow:0 5px 15px rgba(0,0,0,0.1);
text-align:center;
transition:0.3s;
}

.product-card:hover{
transform:translateY(-5px);
}

.product-card img{
width:100%;
height:140px;
object-fit:cover;
border-radius:8px;
margin-bottom:10px;
}

.product-card p{
font-weight:bold;
}

/* PAYMENT */
#paymentSection{
background:white;
padding:20px;
border-radius:10px;
box-shadow:0 5px 15px rgba(0,0,0,0.1);
margin-top:20px;
}

.checkout-btn{
margin-top:20px;
width:100%;
}

</style>
</head>

<body>

<header>
<h1>Hostel Mart</h1>
<p>Fast & Easy Hostel Shopping</p>
</header>

<div class="main-container">

<div class="content">

<!-- LOGIN -->
<div id="loginSection" class="login-box">
<h2>Login</h2>
<input type="text" placeholder="Enter Hostel ID">
<input type="password" placeholder="Password">
<button onclick="login()">Login</button>
</div>

<!-- STORE -->
<div id="storeSection" style="display:none">

<h2>Browse Products</h2>

<div class="products">

<div class="product-card">
<img src="https://images.unsplash.com/photo-1692273212247-f5efb3fc9b87?q=80&w=870&auto=format&fit=crop&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D">
<h3>Maggi</h3>
<p>₹20</p>
<button onclick="addToCart('Maggi',20)">Add to Cart</button>
</div>

<div class="product-card">
<img src="https://images.unsplash.com/photo-1621447504864-d8686e12698c?q=80&w=769&auto=format&fit=crop&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D">
<h3>Chips</h3>
<p>₹30</p>
<button onclick="addToCart('Chips',30)">Add to Cart</button>
</div>

<div class="product-card">
<img src="https://images.unsplash.com/photo-1600271886742-f049cd451bba">
<h3>Drinks</h3>
<p>₹40</p>
<button onclick="addToCart('Drinks',40)">Add to Cart</button>
</div>

<div class="product-card">
<img src="https://images.unsplash.com/photo-1516414447565-b14be0adf13e?q=80&w=773&auto=format&fit=crop&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D">
<h3>Notebook</h3>
<p>₹50</p>
<button onclick="addToCart('Notebook',50)">Add to Cart</button>
</div>

<div class="product-card">
<img src="https://images.unsplash.com/photo-1584308666744-24d5c474f2ae?q=80&w=830&auto=format&fit=crop&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D">
<h3>Dolo</h3>
<p>₹90</p>
<button onclick="addToCart('Dolo',90)">Add to Cart</button>
</div>

<div class="product-card">
<img src="https://images.unsplash.com/photo-1589395937921-fddc324ccdd2?q=80&w=813&auto=format&fit=crop&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D">
<h3>Sanitary Pads</h3>
<p>₹50</p>
<button onclick="addToCart('Sanitary Pads',50)">Add to Cart</button>
</div>

<div class="product-card">
<img src="https://images.unsplash.com/photo-1773739687401-32e6fc57774c?q=80&w=870&auto=format&fit=crop&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D">
<h3>Biscuits</h3>
<p>₹25</p>
<button onclick="addToCart('Biscuits',25)">Add to Cart</button>
</div>

<div class="product-card">
<img src="https://images.unsplash.com/photo-1628610688436-e635552020fc?q=80&w=870&auto=format&fit=crop&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D">
<h3>Instant Noodles</h3>
<p>₹60</p>
<button onclick="addToCart('Instant Noodles',60)">Add to Cart</button>
</div>

<div class="product-card">
<img src="https://images.unsplash.com/photo-1605641987825-c1664626d79f?q=80&w=870&auto=format&fit=crop&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D">
<h3>Pen</h3>
<p>₹20</p>
<button onclick="addToCart('Pen',20)">Add to Cart</button>
</div>

<div class="product-card">
<img src="https://images.unsplash.com/photo-1568205612837-017257d2310a?q=80&w=580&auto=format&fit=crop&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D">
<h3>Pencil</h3>
<p>₹10</p>
<button onclick="addToCart('Pencil',10)">Add to Cart</button>
</div>

</div>

<button class="checkout-btn" onclick="checkout()">Proceed to Checkout</button>

<!-- PAYMENT -->
<div id="paymentSection" style="display:none">

<h2>Select Payment Method</h2>

<label><input type="radio" name="payment" value="UPI"> UPI</label><br><br>
<label><input type="radio" name="payment" value="Card"> Card</label><br><br>
<label><input type="radio" name="payment" value="COD"> Cash on Delivery</label><br><br>

<button onclick="confirmPayment()">Confirm Payment</button>

</div>

</div>

</div>

<!-- CART -->
<div class="cart-panel">
<h2>Cart</h2>
<ul id="cartItems"></ul>
<h3 id="total">Total: ₹0</h3>
</div>

</div>

<script>

let cart=[]
let total=0

function login(){
document.getElementById("loginSection").style.display="none"
document.getElementById("storeSection").style.display="block"
}

function addToCart(item,price){
cart.push({item,price})
total+=price
updateCart()
}

function updateCart(){
let cartList=document.getElementById("cartItems")
cartList.innerHTML=""

cart.forEach(product=>{
let li=document.createElement("li")
li.textContent=product.item+" - ₹"+product.price
cartList.appendChild(li)
})

document.getElementById("total").textContent="Total: ₹"+total
}

function checkout(){
if(cart.length===0){
alert("Your cart is empty!")
return
}
document.getElementById("paymentSection").style.display="block"
}

function confirmPayment(){
let paymentMethod=document.querySelector('input[name="payment"]:checked')

if(!paymentMethod){
alert("Please select a payment method")
return
}

alert("Payment successful using "+paymentMethod.value+"! Order placed.")

cart=[]
total=0
updateCart()

document.getElementById("paymentSection").style.display="none"
}

</script>

</body>
</html>
