# responsive-grid-layout
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Grid Showcase</title>
    <style>
        :root {
            --primary-color: #2d3436;
            --secondary-color: #636e72;
            --accent-color: #00b894;
            --background-color: #f5f6fa;
            --grid-gap: 1.5rem;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', sans-serif;
            line-height: 1.6;
            background-color: var(--background-color);
            color: var(--primary-color);
            padding: 2rem;
        }

        .grid-container {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: var(--grid-gap);
            max-width: 1200px;
            margin: 0 auto;
            transition: all 0.3s ease;
        }

        .grid-item {
            background: white;
            padding: 1.5rem;
            border-radius: 8px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            transition: transform 0.3s ease;
        }

        .grid-item:hover {
            transform: translateY(-5px);
        }

        .featured {
            grid-column: span 2;
            grid-row: span 2;
        }

        .wide {
            grid-column: span 2;
        }

        .tall {
            grid-row: span 2;
        }

        h1 {
            text-align: center;
            margin-bottom: 2rem;
            color: var(--primary-color);
        }

        h2 {
            color: var(--accent-color);
            margin-bottom: 1rem;
        }

        p {
            color: var(--secondary-color);
        }

        @media (max-width: 1024px) {
            .grid-container {
                grid-template-columns: repeat(3, 1fr);
            }
        }

        @media (max-width: 768px) {
            .grid-container {
                grid-template-columns: repeat(2, 1fr);
            }
            
            .featured {
                grid-column: span 2;
                grid-row: span 1;
            }
        }

        @media (max-width: 480px) {
            .grid-container {
                grid-template-columns: 1fr;
            }

            .grid-item, .featured, .wide {
                grid-column: span 1;
            }

            body {
                padding: 1rem;
            }
        }
    </style>
</head>
<body>
    <h1>CSS Grid Showcase</h1>
    
    <div class="grid-container">
        <div class="grid-item featured">
            <h2>Featured Content</h2>
            <p>This is a featured section that spans multiple grid cells to create visual hierarchy. It demonstrates how CSS Grid can be used to create dynamic layouts.</p>
        </div>
        
        <div class="grid-item">
            <h2>Standard Item</h2>
            <p>A regular grid item showing basic grid cell usage.</p>
        </div>
        
        <div class="grid-item">
            <h2>Grid Element</h2>
            <p>Another standard item in the grid layout.</p>
        </div>
        
        <div class="grid-item tall">
            <h2>Tall Content</h2>
            <p>This item spans multiple rows to show vertical expansion capabilities.</p>
        </div>
        
        <div class="grid-item wide">
            <h2>Wide Section</h2>
            <p>A horizontally expanded section showing how items can span multiple columns.</p>
        </div>
        
        <div class="grid-item">
            <h2>Flexible Item</h2>
            <p>Demonstrates the grid's ability to maintain consistent spacing.</p>
        </div>
        
        <div class="grid-item">
            <h2>Grid Box</h2>
            <p>Shows how items automatically flow into available grid spaces.</p>
        </div>
        
        <div class="grid-item">
            <h2>Dynamic Item</h2>
            <p>Part of the responsive layout that adjusts based on screen size.</p>
        </div>
    </div>
</body>
</html>
