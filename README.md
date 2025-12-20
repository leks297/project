# EX 09 Pharmacy Website using BOOTSRAP
# Date:19-12-25
# AIM:
To create a simplified clone of Dribbble (https://dribbble.com/) landing page.

# DESIGN STEPS:
## Step 1:
Clone the repository from GitHub.

## Step 2:
Create Django Admin project.

## Step 3:
Create a New App under the Django Admin project.

## Step 4:
Insert the necessary CSS and JavaScript files as external in order to use Bootstrap.

## Step 5:
Create a HTML file and include the needed Bootstrap components.

## Step 6:
Publish the website in the LocalHost.

# PROGRAM :
```
index.html
{% load static %}
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Products | HealthPlus Pharmacy</title>
    <meta name="viewport" content="width=device-width, initial-scale=1">

    <!-- Bootstrap CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet">

    <!-- Custom CSS -->
    <link rel="stylesheet" href="{% static 'css/style.css' %}">
</head>
<body>

<!-- Navbar -->
<nav class="navbar navbar-expand-lg navbar-dark bg-success">
    <div class="container">
        <a class="navbar-brand" href="/">💊 HealthPlus</a>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navMenu">
            <span class="navbar-toggler-icon"></span>
        </button>

        <div class="collapse navbar-collapse" id="navMenu">
            <ul class="navbar-nav ms-auto">
                <li class="nav-item"><a class="nav-link" href="/">Home</a></li>
                <li class="nav-item"><a class="nav-link active" href="/products/">Products</a></li>
                <li class="nav-item"><a class="nav-link" href="/about/">About</a></li>
                <li class="nav-item"><a class="nav-link" href="/contact/">Contact</a></li>
            </ul>
        </div>
    </div>
</nav>

<!-- Page Heading -->
<section class="py-5 text-center bg-light">
    <div class="container">
        <h2 class="fw-bold">Our Products</h2>
        <p class="text-muted">Quality medicines at affordable prices</p>
    </div>
</section>

<!-- Products Section -->
<section class="container my-5">
    <div class="row g-4">

        <!-- Product 1 -->
        <div class="col-md-3">
            <div class="card product-card h-100">
                <img src="{% static 'images/paracetamol.jpg' %}" class="card-img-top" alt="Paracetamol">
                <div class="card-body text-center">
                    <h6 class="card-title">Paracetamol</h6>
                    <p class="text-success fw-bold">₹30</p>
                    <button class="btn btn-success btn-sm">Buy</button>
                </div>
            </div>
        </div>

        <!-- Product 2 -->
        <div class="col-md-3">
            <div class="card product-card h-100">
                <img src="{% static 'images/vitaminc.jpg' %}" class="card-img-top" alt="Vitamin C">
                <div class="card-body text-center">
                    <h6 class="card-title">Vitamin C</h6>
                    <p class="text-success fw-bold">₹120</p>
                    <button class="btn btn-success btn-sm">Buy</button>
                </div>
            </div>
        </div>

        <!-- Product 3 -->
        <div class="col-md-3">
            <div class="card product-card h-100">
                <img src="{% static 'images/coughsyrup.jpg' %}" class="card-img-top" alt="Cough Syrup">
                <div class="card-body text-center">
                    <h6 class="card-title">Cough Syrup</h6>
                    <p class="text-success fw-bold">₹90</p>
                    <button class="btn btn-success btn-sm">Buy</button>
                </div>
            </div>
        </div>

        <!-- Product 4 -->
        <div class="col-md-3">
            <div class="card product-card h-100">
                <img src="{% static 'images/sanitizer.png' %}" class="card-img-top" alt="Hand Sanitizer">
                <div class="card-body text-center">
                    <h6 class="card-title">Hand Sanitizer</h6>
                    <p class="text-success fw-bold">₹60</p>
                    <button class="btn btn-success btn-sm">Buy</button>
                </div>
            </div>
        </div>

    </div>
</section>

<!-- Footer -->
<footer class="bg-success text-white text-center py-3">
    © 2025 HealthPlus Pharmacy. Designed by Lekha Shree R D
</footer>

<!-- Bootstrap JS -->
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/js/bootstrap.bundle.min.js"></script>

</body>
</html>

about.html
<h1 class="text-center mt-5">About Our Pharmacy</h1>
<p class="text-center">We provide trusted medicines since 2020.</p>

products.html
<h1 class="text-center mt-5">All Products</h1>
<p class="text-center">Medicine catalog coming soon.</p>

contact.html
<h1 class="text-center mt-5">Contact Us</h1>
<p class="text-center">Email: support@healthplus.com</p>

style.css
body {
    background: linear-gradient(to right, #ecfeff, #f0fdf4);
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    margin: 0;
    padding: 0;
}

.navbar {
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
}

.navbar-brand {
    font-weight: 600;
    font-size: 20px;
}



.product-card {
    border-radius: 15px;
    overflow: hidden;
    background-color: #ffffff;
    box-shadow: 0 8px 20px rgba(0, 0, 0, 0.08);
    transition: transform 0.3s ease, box-shadow 0.3s ease;
}


.product-card:hover {
    transform: translateY(-8px);
    box-shadow: 0 12px 25px rgba(0, 0, 0, 0.15);
}



.product-card img {
    height: 200px;
    width: 100%;
    object-fit: cover;
    padding: 15px;
    background-color: #f0fdf4;
    border-bottom: 1px solid #e5e7eb;
}


.card-title,
.product-card h6 {
    font-weight: 600;
    color: #064e3b;
}

.product-card p {
    font-size: 15px;
    margin-bottom: 10px;
}



.btn-success {
    background-color: #15803d;
    border: none;
    border-radius: 20px;
    padding: 6px 18px;
    font-size: 14px;
}

.btn-success:hover {
    background-color: #166534;
}


section {
    margin-bottom: 40px;
}


footer {
    font-size: 14px;
}

script.js
function showAlert() {
  alert("Thank you for choosing HealthPlus Pharmacy!");
}

views.py
from django.shortcuts import render

def home(request):
    return render(request, 'index.html')

def about(request):
    return render(request, 'about.html')

def products(request):
    return render(request, 'products.html')

def contact(request):
    return render(request, 'contact.html')

urls.py
from django.contrib import admin
from django.urls import path
from pharmapp import views

urlpatterns = [
    path('admin/', admin.site.urls),
    path('', views.home, name='home'),
    path('about/', views.about, name='about'),
    path('products/', views.products, name='products'),
    path('contact/', views.contact, name='contact'),
]
```

# OUTPUT:
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/a9d2fd42-7107-4a0d-b7ff-b9906973836a" />

# RESULT:
The Project for responsive web design using Bootstrap is completed successfully.
