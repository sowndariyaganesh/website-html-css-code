# website-html-css-code


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Donuts</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="header">
        <h1>DIPPN'<br>DONUTS</h1>
        <ul>
            <li >ABOUT US</li>
            <li id="orderBtn" >ORDER ONLINE</li></a>
            <li>MENU</li>
            <li>LOCATION</li>
            <li>CONTACT US</li>
        </ul>
    </div>
    <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Libero, possimus cupiditate <br>repudiandae eligendi vero recusandae explicabo iste placeat.</p>
    <button>Start Dippin</button>
    <hr>
    <div class="main">
        <div class="item">
            <img src="pexels-cottonbro-4686959.jpg" alt="Donut Comb">
            <h2>DONUT COMB</h2>
            <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Placeat, veniam.</p>
        </div>
        <div class="item">
            <img src="pexels-mccutcheon-3779937.jpg" alt="Adventure Dips">
            <h2>ADVENTURE DIPS</h2>
            <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Placeat, veniam.</p>
        </div>
        <div class="item">
            <img src="pexels-ravikant-913816.jpg" alt="Chocolate Donut">
            <h2>CHOCOLATE DONUT</h2>
            <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Placeat, veniam.</p>
        </div>
    </div>
    <hr>
    <div class="end">
        <h1>Build Your Own</h1>
        <div class="card3">
            <button>Lorem ipsum dolor sit amet.</button>
            <button>Lorem ipsum dolor sit amet.</button>
            <button>Lorem ipsum dolor sit amet.</button>
            <button>Lorem ipsum dolor sit amet.</button>
        </div>
    </div>
<script>
  document.getElementById("orderBtn").addEventListener("click", function () {
    window.location.href = "order.html";
  });
</script>

</body>
</html>
body {
  font-family: 'Segoe UI', sans-serif;
  background-color: #fff0f5;
  color: #b30059;
  padding: 40px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.order-container {
  background-color: #ffe6f0;
  padding: 30px;
  border-radius: 25px;
  box-shadow: 0 8px 16px rgba(255, 105, 180, 0.2);
  width: 100%;
  max-width: 400px;
  text-align: center;
}

h1 {
  margin-bottom: 25px;
  color: #a0005c;
}

form {
  display: flex;
  flex-direction: column;
  gap: 15px;
}

label {
  text-align: left;
  font-weight: bold;
  color: #800040;
}

input, select, textarea {
  padding: 10px;
  border: 1px solid #ffb6c1;
  border-radius: 10px;
  font-size: 14px;
  background-color: #fff0f5;
  color: #4d0039;
}

input:focus, select:focus, textarea:focus {
  outline: none;
  border-color: #ff69b4;
  background-color: #fffafc;
}

button {
  background-color: #ff69b4;
  color: white;
  padding: 12px;
  font-size: 16px;
  border: none;
  border-radius: 30px;
  cursor: pointer;
  transition: background-color 0.3s;
}

button:hover {
  background-color: #e75494;
}

#confirmation {
  margin-top: 20px;
  font-weight: bold;
  color: #cc0066;
}
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Order Donuts</title>
  <link rel="stylesheet" href="order.css">
</head>
<body>

  <div class="order-container">
    <h1>Order Your Donuts 🍩</h1>
    <form id="orderForm">
      <label for="name">Your Name:</label>
      <input type="text" id="name" required placeholder="Enter your name">
      <label for="type">Donut Type:</label>
      <select id="type" required>
        <option value="">-- Select a Donut --</option>
        <option value="classic">Classic Dip</option>
        <option value="chocolate">Chocolate Donut</option>
        <option value="adventure">Adventure Dip</option>
        <option value="combo">Donut Combo</option>
      </select>
      <label for="quantity">Quantity:</label>
      <input type="number" id="quantity" min="1" value="1" required>
      <label for="note">Special Instructions:</label>
      <textarea id="note" rows="3" placeholder="Any preferences? (Optional)"></textarea>
      <button type="submit">Place Order</button>
    </form>
    <p id="confirmation"></p>
  </div>
  <script>
    // JS: Form submission handler
    document.getElementById("orderForm").addEventListener("submit", function (e) {
      e.preventDefault();
      const name = document.getElementById("name").value;
      const type = document.getElementById("type").value;
      const quantity = document.getElementById("quantity").value;
      document.getElementById("confirmation").innerText = 
        `Thanks, ${name}! Your ${quantity} ${type}(s) will be ready shortly! 🍩💖`;
    });
  </script>

</body>
</html>
/* Reset and base styles */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    background-color: #fff0f5; /* Light pink background */
    color: #4d0039;
    line-height: 1.6;
    padding: 20px;
}

/* Header Section */
.header {
    background-color: #ffb6c1; /* Baby pink */
    padding: 20px;
    text-align: center;
    border-radius: 20px;
    margin-bottom: 30px;
    box-shadow: 0 4px 10px rgba(255, 105, 180, 0.3);
}

.header h1 {
    font-size: 48px;
    color: #a0005c;
    margin-bottom: 15px;
    line-height: 1.2;
}

.header ul {
    list-style: none;
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    gap: 20px;
    margin-top: 10px;
}

.header ul li {
    cursor: pointer;
    font-weight: bold;
    color: #800040;
    transition: color 0.3s;
}

.header ul li:hover {
    color: #fff;
}

/* Intro Paragraph and Button */
p {
    margin: 20px auto;
    max-width: 700px;
    text-align: center;
    font-size: 18px;
    color: #80204d;
}

button {
    background-color: #ff69b4; /* Hot pink */
    color: white;
    padding: 12px 25px;
    border: none;
    border-radius: 30px;
    cursor: pointer;
    font-size: 16px;
    display: block;
    margin: 10px auto 30px auto;
    transition: background-color 0.3s;
    box-shadow: 0 4px 8px rgba(255, 105, 180, 0.3);
}

button:hover {
    background-color: #e75494;
}

/* Main Product Section - Horizontal Cards */
.main {
    display: flex;
    justify-content: center;
    gap: 30px;
    padding: 20px 0;
    flex-wrap: wrap;
}

/* Donut Card Style */
.item {
    background-color: #ffcce0; /* soft pink */
    border-radius: 30px;
    padding: 20px;
    text-align: center;
    box-shadow: 0 6px 15px rgba(255, 105, 180, 0.2);
    max-width: 280px;
    transition: transform 0.3s ease;
    border: 2px solid #ff99cc;
}

.item:hover {
    transform: scale(1.05);
}

/* Image with Zoom */
.item img {
    width: 100%;
    height: auto;
    border-radius: 20px;
    object-fit: cover;
    transition: transform 0.4s ease-in-out;
    box-shadow: 0 4px 8px rgba(255, 105, 180, 0.1);
    cursor: pointer;
}

.item img:hover {
    transform: scale(1.1);
}

/* Title */
.item h2 {
    font-size: 20px;
    color: #b30059;
    margin: 15px 0 10px;
}

/* Description */
.item p {
    font-size: 16px;
    color: #66334d;
}

/* Build Your Own Section */
.end {
    background-color: #ffe6f0; /* very light pink */
    padding: 30px 20px;
    border-radius: 20px;
    text-align: center;
    margin-top: 40px;
    box-shadow: 0 4px 10px rgba(255, 105, 180, 0.2);
}

.end h1 {
    font-size: 32px;
    color: #a0005c;
    margin-bottom: 20px;
}

.card3 {
    display: flex;
    flex-wrap: wrap;
    gap: 15px;
    justify-content: center;
}

.card3 button {
    background-color: #ff99cc;
    font-size: 14px;
    padding: 10px 20px;
    margin: 5px;
    border-radius: 20px;
    border: none;
    cursor: pointer;
    transition: background-color 0.3s;
    color: white;
}

.card3 button:hover {
    background-color: #ff66a3;
}

/* Divider style */
hr {
    border: none;
    height: 2px;
    background-color: #ffb6c1;
    margin: 40px auto;
    width: 80%;
    border-radius: 5px;
}

/* Responsive Design */
@media (max-width: 768px) {
    .header h1 {
        font-size: 36px;
    }
    .header ul {
        flex-direction: column;
        gap: 10px;
    }
    .main {
        flex-direction: column;
        align-items: center;
  }
}
ul li a {
  text-decoration: none;
  color: #800040;
  font-weight: bold;
  transition: color 0.3s ease;
}

ul li a:hover {
  color: white;
}


