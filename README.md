# Ex.07 Restaurant Website
# Date:5.10.2025
# AIM:
To develop a static Restaurant website to display the food items and services provided by them.

# DESIGN STEPS:
## Step 1:
Requirement collection.

## Step 2:
Creating the layout using HTML and CSS.

## Step 3:
Updating the sample content.

## Step 4:
Choose the appropriate style and color scheme.

## Step 5:
Validate the layout in various browsers.

## Step 6:
Validate the HTML code.

## Step 7:
Publish the website in the given URL.

# PROGRAM:
```
home.html
{% load static %}
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Delicious Food</title>
    <link rel="stylesheet" href="{% static 'sty.css' %}">
    <style>
        .section {
            display: flex;
            flex-direction: row;
            gap: 20px;
        }
        .img {
            display: flex;
            flex-direction: row;
            gap: 20px;
        }
        nav ul {
            display: flex;
            list-style: none;
            justify-content: center;
            gap: 20px;
            padding: 0;
        }
        nav a {
            text-decoration: none;
            font-weight: bold;
            color: black;
        }
        nav a:hover {
            color: red;
        }
        .info {
            display: flex;
            justify-content: center;
            gap: 30px;
            margin-top: 20px;
        }
        .info-card {
            text-align: center;
            background-color: white;
            padding: 10px;
            border-radius: 10px;
            width: 300px;
        }
        .banner-text {
            text-align: center;
            font-size: 18px;
            margin-top: 20px;
        }
    </style>
</head>

<body bgcolor="yellow">
    <header>
        <h1 align="center">DELICIOUS FOOD</h1>
        <nav>
            <ul>
                <li><a href="{% url 'home' %}">HOME</a></li>
                <li><a href="{% url 'rest' %}">MENU</a></li>
                <li><a href="{% url 'admins' %}">ADMIN</a></li>
                <li><a href="{% url 'contact' %}">CONTACT</a></li>
            </ul>
        </nav>
    </header>

    <section class="banner">
        <div class="banner-text">
            <p>ENJOY DELICIOUS FOOD. LIMITED OFFER</p>
        </div>
    </section>

    <section class="info">
        <div class="info-card">
            <img src="{% static 'table.png' %}" height="200" width="200" alt="Menu">
            <h3>MENU</h3>
            <p>Our new menu is updated with full of tasty dishes for you.</p>
            <a href="{% url 'rest' %}">View Menu</a>
        </div>

        <div class="info-card">
            <img src="{% static 'book.png' %}" height="200" width="200" alt="Booking">
            <h3>BOOKING</h3>
            <p>Reserve your table in advance.</p>
            <a href="{% url 'contact' %}">Book Now</a>
        </div>

        <div class="info-card">
            <img src="{% static 'new restaurant.png' %}" height="200" width="200" alt="Timings">
            <h3>Opening Time</h3>
            <p>
                MON–FRI: 1PM–9:30PM<br>
                SAT: 12PM–10PM<br>
                SUN: 10AM–9PM
            </p>
        </div>
    </section>
</body>
</html>

rest.html
{% load static %}
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<style>
    .container{
        display:flex;
        flex-direction:column;
        height:auto;
        width:300px;
        border-radius: 20px;
        align-items: center;
        background-color:goldenrod;
        gap: 20px;
        margin-bottom: 20px;
    }
    .container img{
        height:200px;
        width:200px;
    }
    .container p{
        text-align: center;
        padding: 20px;
    }
    .container1{
        display:flex;
        flex-direction:row;
        gap: 20px;

    }
    .container2{
        display:flex;
        flex-direction:row;
        gap: 30px;

    }
</style>
<body>
    <div class="container1">
       <div class="container">
          <h1 align="center">FRIED RICE</h1>
          <img src="{% static 'fried rice.png' %}">
          <p> Fried rice is a popular and flavorful dish made by stir-frying cooked rice with vegetables, eggs, sauces, and often meat or seafood. It’s enjoyed all over the world and is especially famous in Chinese, Thai, and Indo-Chinese cuisines.</p>
          </div>
        <div class="container">
          <h1 align="center">NOODLES</h1>
          <img src="{% static 'noodles.png' %}">
          <p>Hakka Noodles (Indo-Chinese) - Stir-fried with veggies and soy sauce; mild and flavorful.Chow Mein – Crispy or soft noodles tossed with veggies, meat, and sauces.
Ramen - Japanese noodles usually served in a rich, flavorful broth.
Rice Noodles - Light and gluten-free; often used in Thai or Vietnamese dishes.
Instant Noodles -Quick and easy.</p>
       </div>
       <div class="container">
          <h1 align="center">CHICKEN PASTA</h1>
          <img src="{% static 'pasta.png' %}">
          <p>White Sauce Chicken Pasta (Alfredo) - Creamy and cheesy.
Tomato Chicken Pasta -Tangy and flavorful with tomato sauce.
Spicy Chicken Pasta - Uses chili flakes or hot sauce for a kick.
Chicken Pesto Pasta -Tossed with basil pesto and grilled chicken.</p>
       </div>
       <div class="container">
          <h1 align="center">BIRIYANI</h1>
          <img src="{% static 'biriyani.png' %}">
          <p>Popular Types of Biryani:
Hyderabadi Biryani - Known for strong spices and dum cooking.Lucknowi (Awadhi) Biryani - Mild, fragrant, and made in layers with cooked meat.
Chicken Biryani - Most popular, flavorful, and quick to make.
Mutton Biryani - Rich and royal in taste.
Veg Biryani - Made with vegetables, paneer, and spices for vegetarians.
Egg Biryani - Simple and tasty variation with boiled or fried eggs.

         </div>
         <div class="container">
          <h1 align="center">SANDWICH</h1>
          <img src="{% static 'sandwich.png' %}">
          <p>Popular Types of Sandwiches:
Vegetable Sandwich -Fresh veggies with chutney or butter.
Grilled Cheese Sandwich - Melty cheese toasted to perfection.
Egg Sandwich - Boiled or scrambled eggs with mayo or seasoning.
Chicken Sandwich - Cooked or shredded chicken with sauces and veggies.
Club Sandwich - Multi-layered with meat, eggs, lettuce, and sauces.
Paneer Sandwich - Indian-style with spiced paneer filling.</p>
         </div>
    </div>
    <div class="container2">
        <div class="container">
          <h1 align="center">SHAWARMA</h1>
          <img src="{% static 'shawarma.png' %}">
          <p>Chicken Shawarma -Tender and mildly spiced, the most common version.
 Beef/Lamb Shawarma - Rich and flavorful with deep spices.
 Falafel Shawarma - Vegetarian option made with fried chickpea balls.
 Spicy Shawarma - Uses hot sauce or chili flakes for extra heat.
Cheese Shawarma - Modern twist with melted cheese inside the wrap.</p>
         </div>
         
        <div class="container">
          <h1 align="center">BURGER</h1>
          <img src="{% static 'burger.png' %}">
          <p>Cheeseburger - with melted cheese on the patty.
Chicken burger - grilled or crispy chicken.
Veggie burger - made from vegetables, paneer, or soya.
Double burger - two patties stacked.
Fish burger - with breaded fish fillet.</p>
        </div>
        <div class="container">
          <h1 align="center">CHICKEN POPCORN</h1>
          <img src="{% static 'chicken popcorn.png' %}">
          <p>Chicken Popcorn is a popular crunchy and juicy snack made with bite-sized pieces of chicken that are seasoned, coated in flour or breadcrumbs, and deep-fried until golden and crispy.
            Serve hot with mayonnaise, tomato ketchup, garlic sauce, or spicy dips.</p>
         </div>
         <div class="container">
          <h1 align="center">PIZZA</h1>
          <img src="{% static 'pizza.png' %}">
          <p>Margherita Pizza - Classic with tomato sauce, mozzarella cheese, and basil.
Veggie Delight - Loaded with onions, capsicum, tomatoes, sweet corn, and olives.Paneer Tikka Pizza - Indian twist with marinated paneer, onions, and spicy sauce.
Farmhouse Pizza - Topped with fresh veggies like mushrooms, capsicum, tomatoes, and onions.
Cheese Pizza - Simple and super cheesy, for cheese lovers.
Spinach & Corn Pizza - Creamy sauce base with spinach and sweet corn.</p>
          </div>
          <div class="container">
          <h1 align="center">THANDOORI CHICKEN</h1>
          <img src="{% static 'tandoori.png' %}">
          <p>Tandoori Chicken Tikka
Boneless cubes on skewers, often served as starters. Tender and smoky.
Tandoori Chicken Wings- Wings marinated in tandoori masala and grilled/fried — popular party snack.
Stuffed Tandoori Chicken Whole chicken stuffed with spiced rice or minced meat before roasting — often made for special occasions.
Tandoori Chicken Pizza
Fusion of Indian flavors with Italian base — topped with tandoori chicken chunks, cheese, and sauce.</p>
           </div>
    </div>    
    
    
</body>
</html>

contact.html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="sty.css">
</head>
<body bgcolor="plum">
    <header>
        <h1 align="center">Delicious Food</h1>
    </header>
    <section>
        <h2 align="center"> CONTACT US :</h2>
        <p style="text-align: center;">
            <h1 align= "center" >ADDRESS: Blue FOOD strt,Thanjavur,TamilNadu.<br></h1>
            <h1 align="center">PHONE NO:+91 5647388589 <br></h1>
            <h1 align= "center">EMAIL: blueinfo1199@gmail.com</h1>      
         </p>
    </section>
    
</body>
</html>

admin.html
{% load static %}
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Administration</title>
    <link rel="stylesheet" href="{% static 'sty.css' %}">
    <style>
        body {
            background-color: pink;
            font-family: Arial, sans-serif;
        }
        header h1 {
            text-align: center;
        }
        nav ul {
            display: flex;
            list-style: none;
            justify-content: center;
            gap: 20px;
            padding: 0;
        }
        nav a {
            text-decoration: none;
            font-weight: bold;
            color: black;
        }
        nav a:hover {
            color: red;
        }
        .admin-grid {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 30px;
            margin-top: 20px;
        }
        .admin-item {
            text-align: center;
            width: 200px;
        }
        .admin-item img {
            width: 150px;
            height: 150px;
            border-radius: 50%;
        }
        .admin-item p {
            margin-top: 10px;
            font-weight: bold;
        }
    </style>
</head>
<body>
    <header>
       <h1>Delicious Food</h1>
       <nav>
            <ul>
                <li><a href="{% url 'home' %}">HOME</a></li>
                <li><a href="{% url 'rest' %}">MENU</a></li>
                <li><a href="{% url 'admins' %}">ADMIN</a></li>
                <li><a href="{% url 'contact' %}">CONTACT</a></li>
            </ul>
       </nav>
    </header>

    <section>
        <h2 style="text-align:center;">ADMINISTRATION</h2>
        <div class="admin-grid">
            <div class="admin-item">
                <img src="{% static 'ceo.png' %}" alt="CEO">
                <p>MS. DIYA</p>
            </div>
            <div class="admin-item">
                <img src="{% static 'supervisor.png' %}" alt="SUPERVISOR">
                <p>MR. ARJUN</p>
            </div>
            <div class="admin-item">
                <img src="{% static 'receptionist.png' %}" alt="RECEPTIONIST">
                <p>MRS. JEEVITHA</p>
            </div>
            <div class="admin-item">
                <img src="{% static 'manager.png' %}" alt="HR">
                <p>MRS. LIYA</p>
            </div>
        </div>
    </section>
</body>
</html>




```
# OUTPUT:
![alt text](<Screenshot 2025-10-05 213210.png>)
![alt text](<Screenshot 2025-10-04 184732.png>)
![alt text](<Screenshot 2025-10-05 213229.png>)
![alt text](<Screenshot 2025-10-05 200312.png>)
# RESULT:
The program for designing software company website using HTML and CSS is completed successfully.
