<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Delicious Restaurant</title>
<link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">
<style>
/* ===== GLOBAL ===== */
*{margin:0;padding:0;box-sizing:border-box;font-family:'Roboto',Arial,sans-serif;}
body{background:#f8f8f8;color:#333;scroll-behavior:smooth;}
a{text-decoration:none;}
section{padding:70px 10%; text-align:center;}
h2{margin-bottom:30px; font-size:32px;}
.container{width:90%; max-width:1100px; margin:auto; display:flex; justify-content:space-between; align-items:center; flex-wrap:wrap;}

/* ===== HEADER ===== */
header{background:white; box-shadow:0 2px 10px rgba(0,0,0,0.1); position:sticky; top:0; z-index:1000;}
.logo{font-size:26px; font-weight:700; color:#ff6b35;}
nav{display:flex; gap:25px;}
nav a{color:#333; font-weight:500; transition:0.3s;}
nav a:hover{color:#ff6b35;}

/* ===== HAMBURGER MENU ===== */
#menu-toggle{display:none;}
.hamburger{display:none; flex-direction:column; cursor:pointer; gap:4px;}
.hamburger span{height:3px; width:25px; background:#333; border-radius:2px; transition:0.3s;}

/* ===== HERO ===== */
.hero{
  height:75vh;
  background-image:url("restaurant-table-many-different-dishes-delicious-healthy-fresh-food-246859761.jpg");
  background-size:cover;
  background-position:center;
  display:flex;
  align-items:center;
  justify-content:center;
  position:relative;
  color:white;
  text-align:center;
}
.hero::before{
  content:"";
  position:absolute;
  top:0; left:0; width:100%; height:100%;
  background:rgba(0,0,0,0.5);
}
.hero-content{position:relative; z-index:1;}
.hero-content h2{font-size:45px; margin-bottom:10px;}
.hero-content p{font-size:18px; margin-bottom:15px;}
.hero-content button{
  padding:12px 28px; border:none; background:#ff6b35; color:white; font-size:16px; border-radius:5px; cursor:pointer; transition:0.3s;
}
.hero-content button:hover{background:#e85a2a;}

/* ===== ABOUT ===== */
.about p{max-width:700px; margin:auto; font-size:16px; color:#555;}

/* ===== MENU ===== */
.menu-grid{display:grid; grid-template-columns:repeat(auto-fit,minmax(250px,1fr)); gap:25px; margin-top:30px;}
.menu-card{background:white; border-radius:10px; box-shadow:0 5px 15px rgba(0,0,0,0.1); transition:0.3s;}
.menu-card:hover{transform:translateY(-8px); box-shadow:0 10px 25px rgba(0,0,0,0.15);}
.menu-card img{width:100%; height:200px; object-fit:cover; border-radius:10px; transition:0.3s;}
.menu-card h3{margin:12px 0 5px;}
.menu-card p{color:#ff6b35; font-weight:700;}

/* ===== GALLERY ===== */
.gallery-grid{display:grid; grid-template-columns:repeat(auto-fit,minmax(200px,1fr)); gap:20px; margin-top:30px;}
.gallery-grid img{width:100%; border-radius:10px; object-fit:cover; transition:0.3s;}
.gallery-grid img:hover{transform:scale(1.05);}

/* ===== RESERVATION ===== */
.reservation-form{display:flex; flex-direction:column; gap:15px; max-width:400px; margin:auto;}
.reservation-form input, .reservation-form button{padding:12px; border-radius:5px; border:1px solid #ddd;}
.reservation-form button{border:none; background:#ff6b35; color:white; cursor:pointer; transition:0.3s;}
.reservation-form button:hover{background:#e85a2a;}

/* ===== REVIEWS ===== */
.review-grid{display:grid; grid-template-columns:repeat(auto-fit,minmax(250px,1fr)); gap:25px; margin-top:30px;}
.review-card{background:white; padding:15px; border-radius:10px; box-shadow:0 5px 15px rgba(0,0,0,0.1); transition:0.3s;}
.review-card:hover{transform:translateY(-8px); box-shadow:0 10px 25px rgba(0,0,0,0.15);}
.review-card h4{margin-top:10px; color:#ff6b35; font-weight:700;}

/* ===== CONTACT ===== */
.contact{background:#333; color:white; padding:50px 10px;}
.contact p{margin:5px 0; font-size:16px;}

/* ===== FOOTER ===== */
footer{background:#111; color:white; padding:20px; font-size:14px; text-align:center;}

/* ===== RESPONSIVE ===== */
@media(max-width:768px){
  .hamburger{display:flex;}
  nav{display:none; flex-direction:column; position:absolute; top:60px; right:0; background:white; width:200px; padding:20px; box-shadow:0 5px 15px rgba(0,0,0,0.2); gap:15px;}
  #menu-toggle:checked + .hamburger + nav{display:flex;}
  #menu-toggle:checked + .hamburger span:nth-child(1){transform:rotate(45deg) translate(5px,5px);}
  #menu-toggle:checked + .hamburger span:nth-child(2){opacity:0;}
  #menu-toggle:checked + .hamburger span:nth-child(3){transform:rotate(-45deg) translate(5px,-5px);}
  .hero-content h2{font-size:32px;}
  .hero-content p{font-size:16px;}
}
</style>
</head>

<body>

<header>
  <div class="container">
    <h1 class="logo">Delicious</h1>
    <input type="checkbox" id="menu-toggle">
    <label for="menu-toggle" class="hamburger">
      <span></span><span></span><span></span>
    </label>
    <nav>
      <a href="#home">Home</a>
      <a href="#about">About</a>
      <a href="#menu">Menu</a>
      <a href="#contact">Contact</a>
    </nav>
  </div>
</header>

<section class="hero" id="home">
  <div class="hero-content">
    <h2>Fresh & Delicious Food</h2>
    <p>Experience the best taste from our chefs</p>
    <button>View Menu</button>
  </div>
</section>

<section class="about container" id="about">
  <h2>About Our Restaurant</h2>
  <p>We serve high quality food made from fresh ingredients. Our chefs create amazing dishes that bring happiness to every customer.</p>
</section>

<section class="menu container" id="menu">
  <h2>Popular Dishes</h2>
  <div class="menu-grid">
    <div class="menu-card"><img src="images.jpeg" alt="Grilled Steak"><h3>Grilled Steak</h3><p>$18</p></div>
    <div class="menu-card"><img src="Crispiest-buttermilk-fried-chicken-burgers-90854e5.jpg" alt="Chicken Burger"><h3>Chicken Burger</h3><p>$10</p></div>
    <div class="menu-card"><img src="Authentic-Neapolitan-Pizza-Dough-Recipe-45.jpg" alt="Italian Pizza"><h3>Italian Pizza</h3><p>$14</p></div>
  </div>
</section>

<section class="gallery container" id="gallery">
  <h2>Food Gallery</h2>
  <div class="gallery-grid">
    <img src="images.jpeg" alt="Food">
    <img src="Authentic-Neapolitan-Pizza-Dough-Recipe-45.jpg" alt="Pizza">
    <img src="Crispiest-buttermilk-fried-chicken-burgers-90854e5.jpg" alt="Burger">
    <img src="restaurant-table-many-different-dishes-delicious-healthy-fresh-food-246859761.jpg" alt="Restaurant Food">
  </div>
</section>

<section class="reservation" id="reservation">
  <h2>Reserve a Table</h2>
  <form class="reservation-form">
    <input type="text" placeholder="Your Name">
    <input type="email" placeholder="Email">
    <input type="date">
    <input type="number" placeholder="Guests">
    <button>Book Table</button>
  </form>
</section>

<section class="reviews container">
  <h2>Customer Reviews</h2>
  <div class="review-grid">
    <div class="review-card"><p>"Amazing food and great service!"</p><h4>- John</h4></div>
    <div class="review-card"><p>"Best pizza I have ever tasted."</p><h4>- Sarah</h4></div>
    <div class="review-card"><p>"Beautiful atmosphere and delicious meals."</p><h4>- David</h4></div>
  </div>
</section>

<section class="contact" id="contact">
  <h2>Contact Us</h2>
  <p>Email: restaurant@email.com</p>
  <p>Phone: +123 456 789</p>
</section>

<footer>
  <p>© 2026 Delicious Restaurant</p>
</footer>

</body>
</html>
