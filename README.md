# CSS Layouts and Responsive Design

## Objectives

Implement Flexbox and Grid for layout design.
Make the webpage responsive using media queries.
Ensure proper alignment and spacing.

## Instructions

- use Flexbox or CSS Grid.
- Add a navigation bar and structure the content.
- Use media queries to adjust layout for mobile, tablet, and desktop.

>[!NOTE]
>  - Include at least:
>  - navigation bar
>  - media queries

# Tasks

- Apply Flexbox or Grid for layout.
- Make the page responsive.
- Test across different screen sizes.


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Responsive Webpage with Flexbox and Grid</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>

    <!-- Navigation Bar -->
    <header>
        <nav>
            <ul>
                <li><a href="#">Home</a></li>
                <li><a href="#">About</a></li>
                <li><a href="#">Services</a></li>
                <li><a href="#">Contact</a></li>
            </ul>
        </nav>
    </header>

    <!-- Main Content Section -->
    <main class="content">
        <section class="hero">
            <h1>Welcome to Our Website</h1>
            <p>Your success starts here. Let us help you grow!</p>
        </section>
        
        <section class="grid-layout">
            <div class="grid-item">Item 1</div>
            <div class="grid-item">Item 2</div>
            <div class="grid-item">Item 3</div>
            <div class="grid-item">Item 4</div>
        </section>
    </main>

    <!-- Footer Section -->
    <footer>
        <p>© 2025 Your Company. All rights reserved.</p>
    </footer>

</body>
</html>


/* General Styles */
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    background-color: #f4f4f4;
}

header {
    background-color: #333;
    padding: 1rem;
}

nav ul {
    list-style-type: none;
    margin: 0;
    padding: 0;
    display: flex;
    justify-content: center;
}

nav ul li {
    margin: 0 1rem;
}

nav ul li a {
    color: #fff;
    text-decoration: none;
    font-size: 1.2rem;
}

main {
    padding: 2rem;
}

.hero {
    text-align: center;
    margin-bottom: 2rem;
}

.hero h1 {
    font-size: 2.5rem;
    margin-bottom: 1rem;
}

.hero p {
    font-size: 1.2rem;
}

.grid-layout {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 1rem;
}

.grid-item {
    background-color: #fff;
    padding: 2rem;
    text-align: center;
    border-radius: 8px;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}

footer {
    text-align: center;
    background-color: #333;
    color: #fff;
    padding: 1rem;
}

/* Media Queries */

/* Mobile: Stack navigation vertically, grid items in one column */
@media (max-width: 767px) {
    nav ul {
        flex-direction: column;
        align-items: center;
    }
    
    .grid-layout {
        grid-template-columns: 1fr;
    }

    .hero h1 {
        font-size: 2rem;
    }

    .hero p {
        font-size: 1rem;
    }
}

/* Tablet: Use two columns in grid */
@media (min-width: 768px) and (max-width: 1024px) {
    .grid-layout {
        grid-template-columns: repeat(2, 1fr);
    }

    .hero h1 {
        font-size: 2.2rem;
    }

    .hero p {
        font-size: 1.1rem;
    }
}

/* Desktop: Use four columns in grid */
@media (min-width: 1025px) {
    .grid-layout {
        grid-template-columns: repeat(4, 1fr);
    }

    .hero h1 {
        font-size: 2.5rem;
    }

    .hero p {
        font-size: 1.2rem;
    }
}

Happy Coding! 💻✨
