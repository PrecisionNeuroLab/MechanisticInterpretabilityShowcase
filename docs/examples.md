# Examples

This document provides examples of how to extend the Mechanistic Interpretability Showcase.

## Adding New Research Cards

To showcase a new research topic, add a card to the research section:

```html
<div class="research-card">
    <h3>Attention Head Analysis</h3>
    <p>Methods for understanding and visualizing attention mechanisms in transformer models.</p>
</div>
```

## Creating Interactive Demos

### Example 1: Simple Visualization Demo

Create a new HTML file `demos/attention-viz.html`:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Attention Visualization Demo</title>
    <link rel="stylesheet" href="../styles.css">
</head>
<body>
    <header>
        <nav class="navbar">
            <div class="container">
                <h1 class="logo">MI Showcase</h1>
                <a href="../index.html" class="btn btn-secondary">Back to Home</a>
            </div>
        </nav>
    </header>
    
    <main>
        <section class="container">
            <h1>Attention Visualization Demo</h1>
            <div id="demo-container">
                <!-- Your visualization code here -->
            </div>
        </section>
    </main>
    
    <script src="attention-viz.js"></script>
</body>
</html>
```

### Example 2: Adding External Libraries

To use visualization libraries like D3.js:

```html
<!-- Add to the <head> section -->
<script src="https://d3js.org/d3.v7.min.js"></script>

<!-- In your JavaScript -->
<script>
    // Create a simple D3 visualization
    const svg = d3.select("#demo-container")
        .append("svg")
        .attr("width", 600)
        .attr("height", 400);
    
    // Add your visualization code here
</script>
```

### Example 3: Jupyter Notebook Integration

To embed Jupyter notebooks:

1. Export your notebook as HTML:
   ```bash
   jupyter nbconvert --to html your_notebook.ipynb
   ```

2. Add a link in the demos section:
   ```html
   <div class="demo-card">
       <h3>Circuit Analysis Notebook</h3>
       <p>Interactive Python notebook exploring circuit analysis techniques.</p>
       <a href="notebooks/circuit-analysis.html" class="btn btn-primary">Open Notebook</a>
   </div>
   ```

## Styling Examples

### Custom Color Scheme

Update CSS variables in `styles.css`:

```css
:root {
    --primary-color: #10b981;  /* Green theme */
    --secondary-color: #3b82f6; /* Blue accent */
    --dark-bg: #111827;
}
```

### Adding Animations

Add custom animations:

```css
@keyframes fadeInUp {
    from {
        opacity: 0;
        transform: translateY(30px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}

.research-card {
    animation: fadeInUp 0.6s ease-out;
}
```

## JavaScript Examples

### Example 1: Dynamic Content Loading

```javascript
// Load research papers dynamically
async function loadResearchPapers() {
    const response = await fetch('data/papers.json');
    const papers = await response.json();
    
    const container = document.querySelector('.research-grid');
    papers.forEach(paper => {
        const card = document.createElement('div');
        card.className = 'research-card';
        card.innerHTML = `
            <h3>${paper.title}</h3>
            <p>${paper.description}</p>
            <a href="${paper.link}" target="_blank">Read More</a>
        `;
        container.appendChild(card);
    });
}
```

### Example 2: Interactive Filters

```javascript
// Add filtering functionality
function setupFilters() {
    const filterButtons = document.querySelectorAll('.filter-btn');
    const cards = document.querySelectorAll('.research-card');
    
    filterButtons.forEach(button => {
        button.addEventListener('click', () => {
            const category = button.dataset.category;
            
            cards.forEach(card => {
                if (category === 'all' || card.dataset.category === category) {
                    card.style.display = 'block';
                } else {
                    card.style.display = 'none';
                }
            });
        });
    });
}
```

## Common Patterns

### Responsive Images

```html
<img src="image.jpg" 
     srcset="image-small.jpg 400w, image-medium.jpg 800w, image-large.jpg 1200w"
     sizes="(max-width: 400px) 100vw, (max-width: 800px) 80vw, 1200px"
     alt="Descriptive text">
```

### Modal Dialogs

```javascript
function createModal(title, content) {
    const modal = document.createElement('div');
    modal.className = 'modal';
    modal.innerHTML = `
        <div class="modal-content">
            <span class="close">&times;</span>
            <h2>${title}</h2>
            <div>${content}</div>
        </div>
    `;
    document.body.appendChild(modal);
    
    modal.querySelector('.close').onclick = () => modal.remove();
}
```

## Best Practices

1. **Keep it Simple**: Start with simple examples and add complexity gradually
2. **Mobile First**: Design for mobile devices first, then enhance for desktop
3. **Accessibility**: Use semantic HTML and ARIA labels
4. **Performance**: Optimize images and minimize JavaScript
5. **Documentation**: Comment your code and update docs when adding features

## Additional Resources

- [MDN Web Docs](https://developer.mozilla.org/) - Web development reference
- [D3.js Gallery](https://observablehq.com/@d3/gallery) - Visualization examples
- [Three.js Examples](https://threejs.org/examples/) - 3D visualization examples
