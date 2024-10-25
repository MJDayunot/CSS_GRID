# CSS_GRID

## What is CSS Grid?
CSS Grid Layout is a powerful layout system designed to create complex web layouts using a grid-based approach. It allows developers to arrange elements in rows and columns, making it easy to create responsive designs that adapt to various screen sizes. With CSS Grid, you can control the position and size of items within a container, resulting in flexible and efficient layouts.

## Key Grid Properties

| Property                     | Description                                                                                          |
|------------------------------|------------------------------------------------------------------------------------------------------|
| `display: grid`             | Enables Grid for the container, making it a grid container.                                         |
| `grid-template-columns`      | Defines the number and size of columns in the grid layout.                                          |
| `grid-template-rows`         | Defines the number and size of rows in the grid layout.                                             |
| `gap`                        | Specifies the spacing between grid items.                                                            |
| `justify-items`             | Aligns grid items along the inline (row) axis. Common values: `start`, `end`, `center`, `stretch`. |
| `align-items`               | Aligns grid items along the block (column) axis. Common values: `start`, `end`, `center`, `stretch`. |


## HTML Code 

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>List of Products</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
<h1>Product List</h1>
<div class="container">
    <div class="item product-item">
        <h2>Product 1</h2>
        <p>Description: High-quality leather wallet</p>
        <p>Price: $25</p>
    </div>
    <div class="item product-item">
        <h2>Product 2</h2>
        <p>Description: Wireless headphones with noise cancellation</p>
        <p>Price: $80</p>
    </div>
    <div class="item product-item">
        <h2>Product 3</h2>
        <p>Description: Stainless steel water bottle (1L)</p>
        <p>Price: $18</p>
    </div>
</div>
</body>
</html>


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>List of Employees</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
<h1>Employee List</h1>
<div class="container">
    <div class="item employee-item">
        <h2>Employee 1</h2>
        <p>Name: John Doe</p>
        <p>Position: Software Engineer</p>
    </div>
    <div class="item employee-item">
        <h2>Employee 2</h2>
        <p>Name: Jane Smith</p>
        <p>Position: Project Manager</p>
    </div>
    <div class="item employee-item">
        <h2>Employee 3</h2>
        <p>Name: Emily Davis</p>
        <p>Position: UX Designer</p>
    </div>    
</div>
</body>
</html>


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>List of Students</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
<h1>Student List</h1>
<div class="container">
    <div class="item student-item">
        <h2>Student 1</h2>
        <p>Name: Michael Lee</p>
        <p>Grade: 10</p>
        <p>Major: STEM</p>
    </div>
    <div class="item student-item">
        <h2>Student 2</h2>
        <p>Name: Sarah Johnson</p>
        <p>Grade: 10</p>
        <p>Major: Humanities</p>
    </div>
    <div class="item student-item">
        <h2>Student 3</h2>
        <p>Name: Daniel Kim</p>
        <p>Grade: 10</p>
        <p>Major: Business</p>
    </div>
</div>
</body>
</html>


<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link rel="stylesheet" href="style.css">
  <title>Book List</title>
</head>
<body>
<h1>Book List</h1>
<div class="container">
  <div class="item book-item">
    <h2>Book 1</h2>
    <p>Title: To Kill a Mockingbird</p>
    <p>Author: Harper Lee</p>
  </div>
  <div class="item book-item">
    <h2>Book 2</h2>
    <p>Title: 1984</p>
    <p>Author: George Orwell</p>
  </div>
  <div class="item book-item">
    <h2>Book 3</h2>
    <p>Title: Pride and Prejudice</p>
    <p>Author: Jane Austen</p>
  </div>
</div>
</body>
</html>


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>List of Fruits</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
<h1>Fruit List</h1>
<div class="container">
    <div class="item fruit-item">
        <h2>Fruit 1</h2>
        <p>Name: Apple</p>
        <p>Description: Crisp and juicy red apples</p>
    </div>
    <div class="item fruit-item">
        <h2>Fruit 2</h2>
        <p>Name: Banana</p>
        <p>Description: Sweet bananas, rich in potassium</p>
    </div>
    <div class="item fruit-item">
        <h2>Fruit 3</h2>
        <p>Name: Mango</p>
        <p>Description: Fresh, ripe mangoes, perfect for smoothies</p>
    </div>
</div>
</body>
</html>


CSS STYLES


body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f5f5f5;
}

h1 {
    text-align: center;
    margin: 20px 0;
    color: #333;
}

.container {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 20px;
    max-width: 1200px;
    margin: 0 auto;
    padding: 20px;
    justify-content: center;
}

.item {
    background-color: #fff;
    padding: 20px;
    border: 1px solid #ddd;
    border-radius: 8px;
    text-align: center;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
    transition: transform 0.2s ease-in-out;
    min-height: 200px;
}

.item:hover {
    transform: scale(1.05);
}

h2 {
    font-size: 1.5em;
    margin-bottom: 10px;
    color: #333;
}

p {
    font-size: 1em;
    color: #666;
}


.product-item {
    background-color: #e3f2fd;
}

.employee-item {
    background-color: #ffe0b2;
}

.student-item {
    background-color: #c8e6c9;
}

.fruit-item {
    background-color: #fff9c4;
}

.book-item {
    background-color: #f3e5f5;
}

