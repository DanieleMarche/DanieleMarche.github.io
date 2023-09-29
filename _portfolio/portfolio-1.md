---
title: "Bomberman-like game"
excerpt: "This was my end of course project for my Methodoligies of programming course.<br/><img src='/images/bomberman-01.png'>"
collection: portfolio
---

<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bootstrap Carousel with Equal Size Images</title>
    <!-- Bootstrap CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet">
    <style>
        .carousel-item {
            height: 300px; /* Set your desired height */
        }

        .carousel-item img {
            object-fit: cover;
            width: 100%; /* Make sure the image covers the entire slide */
            height: 100%; /* Ensure the image fills the slide vertically */
        }
    </style>
</head>


<p>We were required to recreate a Bomberman game using Java and Java Swing or JavaFx as graphic libraries. My project in particular uses Java Swing.
<p>To mantain the data of the user and the statistics all of these data were stored inside a .json file to be parsed at the start of the desktop application and updated when the "save" button was pressed. 
<p>This project alone was vaued as 27/30, as the italian grade is in thirtieths. 
<p>The requirements of the projects were to have 2 different levels, 2 different enemies, to use streams and to implement MVC pattern and other design patterns. 
<p>This project do not implements correctly MVC, though. The game's entities' models store the images of the entities, which should not happen in MVC. 

<p>
  Below are left some pictures of the project and the database.
</p>

<div id="carouselExample" class="carousel slide">
    <div class="carousel-inner">
      <div class="carousel-item active">
        <img src="/images/bomberman-01.png" class="d-block w-100" alt="...">
      </div>
      <div class="carousel-item">
        <img src="/images/500x300.png" class="d-block w-100" alt="...">
      </div>
      <div class="carousel-item">
        <img src="/images/500x300.png" class="d-block w-100" alt="...">
      </div>
    </div>
    <button class="carousel-control-prev" type="button" data-bs-target="#carouselExample" data-bs-slide="prev">
      <span class="carousel-control-prev-icon" aria-hidden="true"></span>
      <span class="visually-hidden">Previous</span>
    </button>
    <button class="carousel-control-next" type="button" data-bs-target="#carouselExample" data-bs-slide="next">
      <span class="carousel-control-next-icon" aria-hidden="true"></span>
      <span class="visually-hidden">Next</span>
    </button>
  </div>

<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-T3c6CoIi6uLrA9TneNEoa7RxnatzjcDSCmG1MXxSR1GAsXEV/Dwwykc2MPK8M2HN" crossorigin="anonymous">
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/js/bootstrap.bundle.min.js" integrity="sha384-C6RzsynM9kWDrMNeT87bh95OGNyZPhcTNXj1NW7RuBCsyN/o0jlpcV8Qyq46cDfL" crossorigin="anonymous"></script>

<hr> 

<h3>
  Technologies used:
</h3>

  Programming language/es: 
  <ul>
    <li>Java.</li>
  </ul>
  Library/ies and framework/s: 
  <ul>
    <li>Java Swing;</li>
    <li>Java's JSON Library;</li>
  </ul>
  External imports:
  <ul>
    <li>The sprites where imported form various open-source websites</li>
  </ul>
